---
description: Erfahren Sie, wie Sie die CreateThread-Funktion verwenden, um einen neuen Thread für einen Prozess zu erstellen. Debugger müssen in der Regel den Inhalt der Register eines Threads überprüfen oder ändern.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Threadfunktionen für das Debuggen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46e9c94ef776cd14bc76afb2c824f2150a1e7c0eb8c94176b237e1c6d54430f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655220"
---
# <a name="thread-functions-for-debugging"></a>Threadfunktionen für das Debuggen

Die [**CreateThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) erstellt einen neuen Thread für einen Prozess. Debugger müssen in der Regel den Inhalt der Register eines Threads überprüfen oder ändern. Dazu muss ein Debugger ein Handle für den Thread abrufen, indem er die [**DuplicateHandle-Funktion**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) verwendet und den entsprechenden Zugriff auf den Thread (THREAD \_ GET \_ CONTEXT, THREAD \_ SET CONTEXT \_ oder beides) angibt. Mit der [**OpenThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) kann ein Debugger den Bezeichner eines vorhandenen Threads abrufen.

Ein Prozess mit entsprechendem Zugriff auf einen Thread kann die Register des Threads mithilfe der [**GetThreadContext-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) untersuchen und den Inhalt der Register des Threads mithilfe der [**SetThreadContext-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) festlegen.

Ein Prozess kann auch THREAD \_ SUSPEND \_ RESUME-Zugriff auf einen Thread erhalten. Dieser Zugriffstyp ermöglicht es einem Debugger, die Ausführung eines Threads mit den Funktionen [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) und [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) zu steuern. Weitere Informationen zu Threads finden Sie unter [Prozesse und Threads.](../procthread/processes-and-threads.md)

 

 
