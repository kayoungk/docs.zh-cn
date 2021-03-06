---
title: Order By 子句
ms.date: 07/20/2015
f1_keywords:
- vb.QueryOrderBy
- vb.QueryAscending
- vb.QueryDescending
helpviewer_keywords:
- queries [Visual Basic], Order By
- Order By clause [Visual Basic]
- Order By statement [Visual Basic]
ms.assetid: fa911282-6b81-44c7-acfa-46b5bb93df75
ms.openlocfilehash: a7104e3dd82ff2dde2911861ce98a7367faf3b25
ms.sourcegitcommit: 17ee6605e01ef32506f8fdc686954244ba6911de
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/22/2019
ms.locfileid: "74350419"
---
# <a name="order-by-clause-visual-basic"></a>Order By 子句 (Visual Basic)
指定查询结果的排序顺序。  
  
## <a name="syntax"></a>语法  
  
```vb  
Order By orderExp1 [ Ascending | Descending ] [, orderExp2 [...] ]  
```  
  
## <a name="parts"></a>部件  
 `orderExp1`  
 必需。 当前查询结果中的一个或多个字段，用于确定如何对返回的值进行排序。 字段名称必须用逗号（，）分隔。 您可以通过使用 `Ascending` 或 `Descending` 关键字，按升序或降序来识别每个字段。 如果未指定 `Ascending` 或 `Descending` 关键字，则默认排序顺序为升序。 排序顺序字段的优先级从左到右。  
  
## <a name="remarks"></a>备注  
 您可以使用 `Order By` 子句对查询结果进行排序。 `Order By` 子句只能根据当前作用域的范围变量对结果进行排序。 例如，`Select` 子句在查询表达式中引入了新的作用域，该作用域具有新的迭代变量。 在查询中的 `Select` 子句之前定义的范围变量在 `Select` 子句之后不可用。 因此，如果要按 `Select` 子句中不存在的字段对结果进行排序，则必须将 `Order By` 子句置于 `Select` 子句之前。 需要执行此操作的一个示例是，如果要按不作为结果的一部分返回的字段对查询进行排序。  
  
 字段的升序和降序由字段的数据类型的 <xref:System.IComparable> 接口的实现确定。 如果数据类型未实现 <xref:System.IComparable> 接口，则忽略排序顺序。  
  
## <a name="example"></a>示例  
 下面的查询表达式使用 `From` 子句为 `books` 集合声明范围变量 `book`。 `Order By` 子句按价格升序对查询结果进行排序（默认值）。 价格相同的书籍按标题的升序排序。 `Select` 子句选择 `Title` 并将 `Price` 属性作为查询返回的值。  
  
 [!code-vb[VbSimpleQuerySamples#24](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#24)]  
  
## <a name="example"></a>示例  
 下面的查询表达式使用 `Order By` 子句按照价格以降序对查询结果进行排序。 价格相同的书籍按标题的升序排序。  
  
 [!code-vb[VbSimpleQuerySamples#25](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#25)]  
  
## <a name="example"></a>示例  
 下面的查询表达式使用 `Select` 子句来选择书名、价格、发布日期和作者。 然后，它将填充新范围的范围变量的 `Title`、`Price`、`PublishDate`和 `Author` 字段。 `Order By` 子句按作者姓名、书籍标题和价格对新范围变量进行排序。 每列按默认顺序（升序）排序。  
  
 [!code-vb[VbSimpleQuerySamples#26](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#26)]  
  
## <a name="see-also"></a>另请参阅

- [Visual Basic 中的 LINQ 简介](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [查询](../../../visual-basic/language-reference/queries/index.md)
- [Select 子句](../../../visual-basic/language-reference/queries/select-clause.md)
- [From 子句](../../../visual-basic/language-reference/queries/from-clause.md)
