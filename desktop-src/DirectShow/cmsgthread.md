---
description: Die cmsgthread-Klasse ist eine Workerthread-Klasse, die Anforderungen asynchron an den Warteschlangen Thread anfügt.
ms.assetid: 57e50abf-c90d-4c8f-afd8-25f29b6a0376
title: Cmsgthread-Klasse
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
ms.openlocfilehash: 307b24e1563fe0545ee6f9405f9fb53e1b6d61b7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747552"
---
# <a name="cmsgthread-class"></a>Cmsgthread-Klasse

`CMsgThread`Bei der-Klasse handelt es sich um eine Workerthread-Klasse, die Anforderungen asynchron an den Warteschlangen Thread anfügt. Um diese Klasse zu verwenden, leiten Sie Ihre Klasse von der Klasse ab, und überschreiben Sie die [**cmsgthread:: threadmessageproc**](cmsgthread-threadmessageproc.md) -Member-Funktion. Die **Thread MessageProc** -Member-Funktion führt jede Anforderung aus. Die Client Funktionen und die **Thread MessageProc** -Member-Funktion müssen eine gemeinsame Definition der Parameter im [**CMSG**](cmsg.md) -Objekt gemeinsam nutzen.

Ein aushandelter Mechanismus weist den Arbeits Thread an, zu beenden. In der Regel handelt es sich hierbei um einen Wert für den Code der [**CMSG**](cmsg.md) -Klasse der **Umschlag** Nachricht.

Es empfiehlt sich, diese Nachricht vom debugtor ihrer abgeleiteten Klasse zu senden und die Member-Funktion [**cmsgthread:: waitforthreadexit**](cmsgthread-waitforthreadexit.md) aufzurufen, bevor Sie die Zerstörung der abgeleiteten Klasse abschließen.



| Geschützte Datenmember                                    | BESCHREIBUNG                                                                                                                           |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| m \_ hsem                                                   | Gibt ein Handle an, das zur Signalisierung verwendet wird.                                                                                                |
| m- \_ Sperre                                                   | Schützt den Zugriff auf Listen.                                                                                                             |
| m \_ lwarteschlange                                               | Gibt an, dass auf einen freien Thread gewartet wird.                                                                                                  |
| m \_ Thread Warteschlange                                            | Überschreibt die Member-Funktion von [**cmsgthread:: getthreadmsg**](cmsgthread-getthreadmsg.md) und blockiert nicht diese Warteschlange. |
| Elementfunktionen                                          | BESCHREIBUNG                                                                                                                           |
| [**Cmsgthread**](cmsgthread-cmsgthread.md)               | Erstellt ein **cmsgthread** -Objekt.                                                                                                   |
| [**CreateThread**](cmsgthread-createthread.md)           | Erstellt einen Thread.                                                                                                                     |
| [**Getthreadhandle**](cmsgthread-getthreadhandle.md)     | Ruft das Thread Handle ab.                                                                                                          |
| [**Getthreadid**](cmsgthread-getthreadid.md)             | Ruft den Bezeichner des Threads ab.                                                                                               |
| [**GetThreadPriority**](cmsgthread-getthreadpriority.md) | Ruft die aktuelle Thread Priorität ab.                                                                                                |
| [**Putthreadmsg**](cmsgthread-putthreadmsg.md)           | Fügt eine Anforderung zur Ausführung durch den Arbeits Thread in die Warteschlange ein.                                                                                  |
| [**ResumeThread**](cmsgthread-resumethread.md)           | Setzt den Betrieb des Arbeitsthreads fort.                                                                                         |
| [**SetThreadPriority**](cmsgthread-setthreadpriority.md) | Legt die Priorität des Threads auf einen neuen Wert fest.                                                                                       |
| [**SuspendThread**](cmsgthread-suspendthread.md)         | Hält den Vorgang eines laufenden Threads an.                                                                                           |
| [**Waitforthreadexit**](cmsgthread-waitforthreadexit.md) | Blockiert, bis der Thread nach einem Rückruf der [**cmsgthread:: SuspendThread**](cmsgthread-suspendthread.md) -Member-Funktion beendet wurde. |
| Über schreibbare Member-Funktionen                              | BESCHREIBUNG                                                                                                                           |
| [**Getthreadmsg**](cmsgthread-getthreadmsg.md)           | Ruft ein [**CMSG**](cmsg.md) -Objekt in der Warteschlange ab, das eine Anforderung enthält.                                                                  |
| [**Onthreadinit**](cmsgthread-onthreadinit.md)           | Stellt die Initialisierung für einen Thread bereit.                                                                                                  |
| [**Threadmessageproc**](cmsgthread-threadmessageproc.md) | Verarbeitet Anforderungen. Dies ist eine reine virtuelle Member-Funktion.                                                                           |



 

 

 



