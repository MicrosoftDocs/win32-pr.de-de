---
description: Die Funktion "kreatethread" erstellt einen neuen Thread für einen Prozess.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Thread Funktionen für das Debuggen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5ab0865d5585656a5c22c24e2604032de8b888
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523672"
---
# <a name="thread-functions-for-debugging"></a>Thread Funktionen für das Debuggen

Die Funktion " [**kreatethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) " erstellt einen neuen Thread für einen Prozess. Debuggger müssen in der Regel den Inhalt der Register eines Threads überprüfen oder ändern. Um dies zu erreichen, muss ein Debugger ein Handle für den Thread abrufen, indem er die [**duplialisiehandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) -Funktion verwendet und den entsprechenden Zugriff auf den Thread (Thread Abruf \_ \_ Kontext, Thread \_ Satz \_ Kontext oder beides) angibt. Die [**openthread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) -Funktion ermöglicht einem Debugger das Abrufen des Bezeichners eines vorhandenen Threads.

Ein Prozess mit geeigneendem Zugriff auf einen Thread kann die Register des Threads mithilfe der [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) -Funktion untersuchen und den Inhalt der Register des Threads mithilfe der [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) -Funktion festlegen.

Ein Prozess kann auch den Thread \_ Suspend \_ anhaltezugriff auf einen Thread erhalten. Diese Art von Zugriff ermöglicht einem Debugger, die Ausführung eines Threads mit den Funktionen " [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) " und " [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) " zu steuern. Weitere Informationen zu Threads finden Sie unter [Prozesse und Threads](../procthread/processes-and-threads.md).

 

 
