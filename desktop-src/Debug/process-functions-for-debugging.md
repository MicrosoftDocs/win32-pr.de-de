---
description: Die Funktion "deateprocess" ermöglicht einem Debugger, einen Prozess zu starten und zu debuggen.
ms.assetid: 7056e181-9bc5-4530-a7b8-d5ff1e345eef
title: Verarbeitungsfunktionen für das Debuggen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31378a4115acfdd5a4a1836199b7387adeb6e3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958300"
---
# <a name="process-functions-for-debugging"></a>Verarbeitungsfunktionen für das Debuggen

Die Funktion " [**deateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) " ermöglicht einem Debugger, einen Prozess zu starten und zu debuggen. Der *fdwcreate* -Parameter von " **kreateprocess** " wird verwendet, um den Typ des Debugvorgangs anzugeben. Wenn das \_ debugprozessflag für den-Parameter angegeben wird, debuggt ein Debugger den neuen Prozess und alle Nachfolger des Prozesses, vorausgesetzt, dass die Nachfolger ohne das \_ debugprozessflag erstellt werden.

Wenn der \_ Debugprozess und das Debuggen \_ nur \_ diese \_ prozessflags für " *f" erstellt* werden, debuggt der Debugger den neuen Prozess, aber keinen seiner Nachfolger.

Ein Debugger kann eine andere Debuggen, indem er einen Prozess mit dem \_ debugprozessflag erstellt. Der neue Prozess (der Debugger, der debuggt wird) muss dann einen Prozess mit dem \_ debugprozessflag erstellen.

Die [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) -Funktion ermöglicht einem Debugger das Abrufen des Bezeichners eines vorhandenen Prozesses. (Die [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) -Funktion verwendet diesen Bezeichner, um den Debugger an den Prozess anzufügen.) In der Regel öffnen debuggger einen Prozess mit den \_ \_ Schreib-und Prozess-VM-Schreib Flags der Prozess-VM \_ \_ . Die Verwendung dieser Flags ermöglicht dem Debugger das Lesen und Schreiben in den virtuellen Arbeitsspeicher des Prozesses mithilfe der Funktionen " [**leseprocessmemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) " und " [**schreiteprocessmemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) ". Weitere Informationen finden Sie unter [**Prozesse und Threads**](../procthread/processes-and-threads.md).

 

 
