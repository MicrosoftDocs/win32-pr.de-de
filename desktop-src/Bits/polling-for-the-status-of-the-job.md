---
title: Abruf des Status des Auftrags
description: Standardmäßig muss eine Anwendung Änderungen am Status eines Auftrags überprüfen.
ms.assetid: b12ee1e0-d3d9-4d31-b2af-7491480968f0
keywords:
- BITS des Übertragungsauftrags , Abruf
- Abruf von Auftragsstatus BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7f1f47a891968e686ae1ffc083bfa9b00d79c8bdc22e2c78ea523ef7ec707e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701720"
---
# <a name="polling-for-the-status-of-the-job"></a>Abruf des Status des Auftrags

Standardmäßig muss eine Anwendung Änderungen am Status eines Auftrags überprüfen. Um Änderungen im Zustand des Auftrags zu erfassen, rufen Sie die [**IBackgroundCopyJob::GetState-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) auf. Um Änderungen an der Anzahl der übertragenen Bytes und Dateien zu erfassen, rufen Sie die [**IBackgroundCopyJob::GetProgress-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) auf. Um Statusinformationen zum Antwortteil eines Upload-Antwort-Auftrags abzurufen, rufen Sie die [**IBackgroundCopyJob2::GetReplyProgress-Methode**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) auf. Ein Beispiel, in dem die Statusinformationen verwendet werden, finden Sie unter [Bestimmen des Fortschritts eines Auftrags.](determining-the-progress-of-a-job.md)

Die [**BG \_ JOB \_ STATE-Enumeration**](/windows/desktop/api/Bits/ne-bits-bg_job_state) definiert die Status eines Auftrags, und die [**BG JOB \_ \_ PROGRESS-Struktur**](/windows/desktop/api/Bits/ns-bits-bg_job_progress) enthält Informationen zur Anzahl der übertragenen Bytes und Dateien.

Um Abrufe zu verwenden, müssen Sie einen Mechanismus zum Initiieren von Abrufen erstellen. Erstellen Sie beispielsweise einen Timer, oder verwenden Sie die Schaltfläche "Aktualisieren" auf der Benutzeroberfläche. Es kann jedoch einfacher sein, sich für Ereignisbenachrichtigungen zu registrieren und Ereignisse zu empfangen, wenn sich der Status oder fortschritt ändert. Informationen zur Ereignisbenachrichtigung finden Sie unter [Registrieren eines COM-Rückrufs.](registering-a-com-callback.md)

Im folgenden Beispiel wird ein Timer verwendet, um den Status eines Auftrags zu fragen. Im Beispiel wird davon ausgegangen, dass [**der IBackgroundCopyJob-Schnittstellenzeiger**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) gültig ist.


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
BG_JOB_STATE State;
HANDLE hTimer = NULL;
LARGE_INTEGER liDueTime;
//IBackgroundCopyError* pError = NULL;
//BG_JOB_PROGRESS Progress;
//WCHAR *JobStates[] = { L"Queued", L"Connecting", L"Transferring",
//                       L"Suspended", L"Error", L"Transient Error",
//                       L"Transferred", L"Acknowledged", L"Canceled"
//                     };

liDueTime.QuadPart = -10000000;  //Poll every 1 second
hTimer = CreateWaitableTimer(NULL, FALSE, L"MyTimer");
SetWaitableTimer(hTimer, &liDueTime, 1000, NULL, NULL, 0);

do
{
  WaitForSingleObject(hTimer, INFINITE);

  //Use JobStates[State] to set the window text in a user interface.
  hr = pJob->GetState(&State);
  if (FAILED(hr))
  {
    //Handle error
  }

  if (BG_JOB_STATE_TRANSFERRED == State)
    //Call pJob->Complete(); to acknowledge that the transfer is complete
    //and make the file available to the client.
  else if (BG_JOB_STATE_ERROR == State || BG_JOB_STATE_TRANSIENT_ERROR == State)
    //Call pJob->GetError(&pError); to retrieve an IBackgroundCopyError interface 
    //pointer which you use to determine the cause of the error.
  else if (BG_JOB_STATE_TRANSFERRING == State)
    //Call pJob->GetProgress(&Progress); to determine the number of bytes 
    //and files transferred.
} while (BG_JOB_STATE_TRANSFERRED != State && 
         BG_JOB_STATE_ERROR != State &&
         BG_JOB_STATE_TRANSIENT_ERROR != State);
CancelWaitableTimer(hTimer);
CloseHandle(hTimer);
```



 

 




