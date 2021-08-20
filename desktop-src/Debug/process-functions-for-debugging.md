---
description: Mit der CreateProcess-Funktion kann ein Debugger einen Prozess starten und debuggen.
ms.assetid: 7056e181-9bc5-4530-a7b8-d5ff1e345eef
title: Prozessfunktionen für das Debuggen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6dec70de05e9b77cd3ff0b2ee8cd01c90ded2987f7ba1cacc3530f040344915
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162631"
---
# <a name="process-functions-for-debugging"></a>Prozessfunktionen für das Debuggen

Mit [**der CreateProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) kann ein Debugger einen Prozess starten und debuggen. Der *fdwCreate-Parameter* von **CreateProcess** wird verwendet, um den Typ des Debugvorgang anzugeben. Wenn das DEBUG PROCESS-Flag für den -Parameter angegeben ist, debuggt ein Debugger den neuen Prozess und alle Nachfolger des Prozesses, vorausgesetzt, die Nachfolger werden ohne das \_ DEBUG \_ PROCESS-Flag erstellt.

Wenn die Flags DEBUG PROCESS und DEBUG ONLY THIS PROCESS für \_ \_ \_ \_ *fdwCreate* angegeben sind, debuggt ein Debugger den neuen Prozess, aber keinen seiner Nachfolger.

Ein Debugger kann einen anderen debuggen, indem er einen Prozess mit dem DEBUG \_ PROCESS-Flag erstellt. Der neue Prozess (der Debugger, der debuggt wird) muss dann einen Prozess mit dem DEBUG \_ PROCESS-Flag erstellen.

Mit [**der OpenProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) kann ein Debugger den Bezeichner eines vorhandenen Prozesses abrufen. (Die [**DebugActiveProcess-Funktion**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) verwendet diesen Bezeichner, um den Debugger an den Prozess anfügen.) In der Regel öffnen Debugger einen Prozess mit den Flags PROCESS \_ VM READ und PROCESS VM \_ \_ \_ WRITE. Mithilfe dieser Flags kann der Debugger mithilfe der [**Funktionen ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) und [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) aus dem virtuellen Arbeitsspeicher des Prozesses lesen und in diesen schreiben. Weitere Informationen finden Sie unter [**Prozesse und Threads**](../procthread/processes-and-threads.md).

 

 
