---
description: Ein Beendigungshandler stellt sicher, dass ein bestimmter Codeblock ausgeführt wird, wenn der Ablauf der Steuerung einen bestimmten geschützten Codekörper verlässt. Ein Beendigungshandler besteht aus den folgenden Elementen.
ms.assetid: 899e2939-e028-4be1-9f08-9a79bf97eb37
title: Beendigungsbehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23e2c81465ab9d469d3d5c503c12f5bf1c7a333507d302f3e5639e0158834e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119292959"
---
# <a name="termination-handling"></a>Beendigungsbehandlung

Ein *Beendigungshandler* stellt sicher, dass ein bestimmter Codeblock ausgeführt wird, wenn der Ablauf der Steuerung einen bestimmten geschützten Codekörper verlässt. Ein Beendigungshandler besteht aus den folgenden Elementen.

-   Ein geschützter Codetext
-   Ein Block des Beendigungscodes, der ausgeführt werden soll, wenn der Ablauf der Steuerung den überwachten Text verlässt.

Beendigungshandler werden in sprachspezifischer Syntax deklariert. Mit dem Microsoft C/C++-Optimierungscompiler werden sie mit **\_ \_ try** und **\_ \_ schließlich** implementiert. Weitere Informationen finden Sie unter [Handlersyntax.](handler-syntax.md)

Der überwachte Codetext kann ein Codeblock, ein Satz geschachtelter Blöcke oder eine gesamte Prozedur oder Funktion sein. Wenn der überwachte Text ausgeführt wird, wird der Beendigungscodeblock ausgeführt. Die einzige Ausnahme besteht darin, dass der Thread während der Ausführung des überwachten Textkörpers beendet wird (z. B. wenn die [**ExitThread-**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) oder [**ExitProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) innerhalb des überwachten Textkörpers aufgerufen wird).

Der Beendigungsblock wird ausgeführt, wenn der Ablauf der Steuerung den überwachten Text verlässt, unabhängig davon, ob der überwachte Text normal oder ungewöhnlich beendet wurde. Der überwachte Text wird als normal beendet betrachtet, wenn die letzte Anweisung im -Block ausgeführt wird und die Steuerung sequenziell in den Beendigungsblock übergeht. Eine ungewöhnliche Beendigung tritt auf, wenn der Ablauf der Steuerung den überwachten Text aufgrund einer Ausnahme verlässt, oder aufgrund einer Steuerungs-Anweisung wie **zurückgeben,** **wechseln Sie zu**, **unterbrechen** oder **fortsetzen.** Die [**AbnormalTermination-Funktion**](abnormaltermination.md) kann innerhalb des Beendigungsblocks aufgerufen werden, um zu bestimmen, ob der überwachte Text normal beendet wurde.

 

 
