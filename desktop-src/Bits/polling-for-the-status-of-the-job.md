---
title: Abrufen des Auftrags Status
description: Standardmäßig muss eine Anwendung Änderungen im Status eines Auftrags Abfragen.
ms.assetid: b12ee1e0-d3d9-4d31-b2af-7491480968f0
keywords:
- Übertragen von Auftrags Bits, Abrufen
- Abrufen von Auftragsstatus Bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df7fcde49d7359ff8cfa38326eba1e1e0bfeac5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855531"
---
# <a name="polling-for-the-status-of-the-job"></a>Abrufen des Auftrags Status

Standardmäßig muss eine Anwendung Änderungen im Status eines Auftrags Abfragen. Um Änderungen im Status des Auftrags aufzuzeichnen, müssen Sie die [**ibackgroundcopyjob:: GetState**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) -Methode aufrufen. Um Änderungen in der Anzahl der übertragenen Bytes und Dateien aufzuzeichnen, müssen Sie die [**ibackgroundcopyjob:: GetProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) -Methode aufrufen. Rufen Sie die [**IBackgroundCopyJob2:: getreplyprogress**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) -Methode auf, um Statusinformationen über den Antwort Teil eines Upload-Antwort-Auftrags abzurufen. Ein Beispiel, in dem die Fortschrittsinformationen verwendet werden, finden Sie unter [bestimmen des Fortschritts eines Auftrags](determining-the-progress-of-a-job.md).

Die [**BG- \_ Auftrags \_ Status**](/windows/desktop/api/Bits/ne-bits-bg_job_state) -Enumeration definiert die Zustände eines Auftrags, und die Status Struktur der [**BG- \_ Aufträge \_**](/windows/desktop/api/Bits/ns-bits-bg_job_progress) enthält Informationen zur Anzahl von Bytes und übertragenen Dateien.

Zum Verwenden von Abruf müssen Sie einen Mechanismus zum Initiieren des Abruf Vorgangs erstellen. Erstellen Sie z. b. einen Timer, oder verwenden Sie die Schaltfläche "Aktualisieren" auf der Benutzeroberfläche. Allerdings ist es möglicherweise einfacher, sich für Ereignis Benachrichtigungen zu registrieren und Ereignisse zu empfangen, wenn sich der Status oder der Fortschritt ändert. Weitere Informationen zur Ereignis Benachrichtigung finden Sie unter [Registrieren eines com-Rückrufs](registering-a-com-callback.md).

Im folgenden Beispiel wird ein Timer verwendet, um den Status eines Auftrags abzurufen. Im Beispiel wird davon ausgegangen, dass der [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstellen Zeiger gültig ist.


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



 

 




