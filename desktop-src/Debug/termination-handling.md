---
description: Ein Beendigungs Handler stellt sicher, dass ein bestimmter Codeblock ausgeführt wird, wenn die Ablauf Steuerung einen bestimmten überwachten Code Körper verlässt. Ein Beendigungs Handler besteht aus den folgenden Elementen.
ms.assetid: 899e2939-e028-4be1-9f08-9a79bf97eb37
title: Abbruch Behandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e926a47a3c0bb4f2cb8a8df350807aee89b49bab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861144"
---
# <a name="termination-handling"></a>Abbruch Behandlung

Ein Beendigungs *Handler* stellt sicher, dass ein bestimmter Codeblock ausgeführt wird, wenn die Ablauf Steuerung einen bestimmten überwachten Code Körper verlässt. Ein Beendigungs Handler besteht aus den folgenden Elementen.

-   Ein überwachter Codetext
-   Ein Block von Beendigungs Code, der ausgeführt werden soll, wenn die Ablauf Steuerung den überwachten Text verlässt.

Beendigungs Handler werden in sprachspezifischer Syntax deklariert. Mithilfe des Microsoft C/C++-Optimierungs Compilers werden Sie mithilfe von **\_ \_ try** und **\_ \_ schließlich** implementiert. Weitere Informationen finden Sie unter [HandlerSyntax](handler-syntax.md).

Der geschützte Textkörper kann ein Codeblock, ein Satz von Blöcke oder eine gesamte Prozedur oder Funktion sein. Wenn der geschützte Text ausgeführt wird, wird der Block des Beendigungs Codes ausgeführt. Die einzige Ausnahme besteht darin, dass der Thread während der Ausführung des geschützten Texts beendet wird (z. b. wenn die [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) -oder [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) -Funktion aus dem überwachten Text aufgerufen wird).

Der Beendigungs Block wird ausgeführt, wenn die Ablauf Steuerung den überwachten Text verlässt, unabhängig davon, ob der geschützte Text normal oder fehlerhaft beendet wurde. Der geschützte Text wird als ordnungsgemäß beendet, wenn die letzte Anweisung im-Block ausgeführt wird und die Steuerung sequenziell in den Beendigungs Block übergeht. Eine ungewöhnliche Beendigung tritt auf, wenn die Ablauf Steuerung den überwachten Text aufgrund einer Ausnahme verlässt, oder aufgrund einer Steuerungs Anweisung wie **Return**, **goto**, **break** oder **Continue**. Die [**Abbruch Funktion kann aus dem**](abnormaltermination.md) Beendigungs Block heraus aufgerufen werden, um zu bestimmen, ob der geschützte Text normal beendet wurde.

 

 
