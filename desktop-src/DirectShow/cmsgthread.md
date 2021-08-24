---
description: Die CMsgThread-Klasse ist eine Workerthreadklasse, die Anforderungen zur asynchronen Vervollständigung an den Warteschlangenthread in die Warteschlange einreiht.
ms.assetid: 57e50abf-c90d-4c8f-afd8-25f29b6a0376
title: CMsgThread-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread
api_type:
- COM
api_location: ''
ms.openlocfilehash: 021683808900a7265f4708dae0bb29ff6d07f6619430ed5687eb77d5e2332a3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813700"
---
# <a name="cmsgthread-class"></a>CMsgThread-Klasse

Die `CMsgThread` -Klasse ist eine Workerthreadklasse, die Anforderungen zur asynchronen Vervollständigung an den Warteschlangenthread in die Warteschlange einreiht. Um diese Klasse zu verwenden, leiten Sie Ihre Klasse von ihr ab und überschreiben die [**CMsgThread::ThreadMessageProc-Memberfunktion.**](cmsgthread-threadmessageproc.md) Die **ThreadMessageProc-Memberfunktion** führt jede Anforderung aus. Ihre Clientfunktionen und die **ThreadMessageProc-Memberfunktion** müssen eine gemeinsame Definition der Parameter im [**CMsg-Objekt**](cmsg.md) aufweisen.

Ein ausgehandelter Mechanismus weist den Arbeitsthread an, den Arbeitsthread zu beenden. In der Regel ist dies ein Wert des [**uMsg-Nachrichtencodes**](cmsg.md) der **CMsg-Klasse.**

Es ist eine gute Idee, diese Nachricht vom Destruktor Ihrer abgeleiteten Klasse zu senden und die [**Memberfunktion CMsgThread::WaitForThreadExit**](cmsgthread-waitforthreadexit.md) aufzurufen, bevor Sie die Zerstörung der abgeleiteten Klasse abschließen.



| Geschützte Datenmember                                    | Beschreibung                                                                                                                           |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| m \_ hSem                                                   | Gibt ein Handle an, das für die Signalisierung verwendet wird.                                                                                                |
| m \_ Sperre                                                   | Schützt den Zugriff auf Listen.                                                                                                             |
| m \_ lWaiting                                               | Gibt an, dass auf einen freien Thread gewartet wird.                                                                                                  |
| m \_ ThreadQueue                                            | Überschreibt die [**Memberfunktion CMsgThread::GetThreadMsg**](cmsgthread-getthreadmsg.md) und blockiert andere Dinge als diese Warteschlange. |
| Elementfunktionen                                          | Beschreibung                                                                                                                           |
| [**CMsgThread**](cmsgthread-cmsgthread.md)               | Erstellt ein **CMsgThread-Objekt.**                                                                                                   |
| [**CreateThread**](cmsgthread-createthread.md)           | Erstellt einen Thread.                                                                                                                     |
| [**GetThreadHandle**](cmsgthread-getthreadhandle.md)     | Ruft das Threadhandle ab.                                                                                                          |
| [**GetThreadID**](cmsgthread-getthreadid.md)             | Ruft den Bezeichner des Threads ab.                                                                                               |
| [**GetThreadPriority**](cmsgthread-getthreadpriority.md) | Ruft die aktuelle Threadpriorität ab.                                                                                                |
| [**PutThreadMsg**](cmsgthread-putthreadmsg.md)           | Reiht eine Anforderung zur Ausführung durch den Arbeitsthread in die Warteschlange ein.                                                                                  |
| [**ResumeThread**](cmsgthread-resumethread.md)           | Setzt den Vorgang des Arbeitsthreads fort.                                                                                         |
| [**SetThreadPriority**](cmsgthread-setthreadpriority.md) | Legt die Priorität des Threads auf einen neuen Wert fest.                                                                                       |
| [**SuspendThread**](cmsgthread-suspendthread.md)         | Unterbricht den Vorgang eines ausgeführten Threads.                                                                                           |
| [**WaitForThreadExit**](cmsgthread-waitforthreadexit.md) | Blockiert, bis der Thread nach einem Aufruf der [**CMsgThread::SuspendThread-Memberfunktion**](cmsgthread-suspendthread.md) beendet wurde. |
| Überschreibbare Memberfunktionen                              | Beschreibung                                                                                                                           |
| [**GetThreadMsg**](cmsgthread-getthreadmsg.md)           | Ruft ein [**CMsg-Objekt**](cmsg.md) in der Warteschlange ab, das eine Anforderung enthält.                                                                  |
| [**OnThreadInit**](cmsgthread-onthreadinit.md)           | Stellt die Initialisierung für einen Thread bereit.                                                                                                  |
| [**ThreadMessageProc**](cmsgthread-threadmessageproc.md) | Verarbeitet Anforderungen. Dies ist eine reine virtuelle Memberfunktion.                                                                           |



 

 

 



