---
title: 如何：从任务中返回值
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- tasks, how to return a value
ms.assetid: c4bc0f44-eba2-4e96-9e03-1cc787461e61
ms.openlocfilehash: 495f68114bfe960b8182be4ab76b72043b2d0cc7
ms.sourcegitcommit: 7588136e355e10cbc2582f389c90c127363c02a5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/15/2020
ms.locfileid: "73141669"
---
# <a name="how-to-return-a-value-from-a-task"></a>如何：从任务中返回值
此示例演示如何使用 <xref:System.Threading.Tasks.Task%601?displayProperty=nameWithType> 类型，以返回 <xref:System.Threading.Tasks.Task%601.Result%2A> 属性的值。 它要求 C:\Users\Public\Pictures\Sample Pictures\ 目录存在，并且该目录包含文件。  
  
## <a name="example"></a>示例  
 [!code-csharp[TPL#10](../../../samples/snippets/csharp/VS_Snippets_Misc/tpl/cs/returnavalue10.cs#10)]
 [!code-vb[TPL#10](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpl/vb/10_returnavalue.vb#10)]  
  
 <xref:System.Threading.Tasks.Task%601.Result%2A> 属性将阻塞调用线程，直到任务完成。  
  
 若要了解如何将一个 <xref:System.Threading.Tasks.Task%601?displayProperty=nameWithType> 的结果传递到延续任务，请参阅[使用延续任务链接任务](../../../docs/standard/parallel-programming/chaining-tasks-by-using-continuation-tasks.md)。  
  
## <a name="see-also"></a>另请参阅

- [基于任务的异步编程](../../../docs/standard/parallel-programming/task-based-asynchronous-programming.md)
- [PLINQ 和 TPL 中的 Lambda 表达式](../../../docs/standard/parallel-programming/lambda-expressions-in-plinq-and-tpl.md)
