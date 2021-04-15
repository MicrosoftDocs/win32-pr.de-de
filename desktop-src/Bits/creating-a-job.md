---
title: Erstellen eines Auftrags
description: Um einen Übertragungs Auftrag zu erstellen, rufen Sie die Methode ibackgroundcopymanager kreatejob auf.
ms.assetid: a7d9feef-4beb-4ae5-9453-9157ee3ec0e8
keywords:
- Übertragen von Auftrags Bits
- Übertragen von Auftrags Bits, erstellen
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 8dddb2427fde43014a31e81f72711ca74e69de34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470997"
---
# <a name="creating-a-job"></a>Erstellen eines Auftrags

Um einen Übertragungs Auftrag zu erstellen, rufen Sie die [**ibackgroundcopymanager:: kreatejob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) -Methode auf. Nachdem Bits den Auftrag erstellt hat, [fügen Sie dem Auftrag Dateien hinzu](adding-files-to-a-job.md) , und [Ändern Sie die Auftrags Eigenschaften](setting-and-retrieving-the-properties-of-a-job.md) entsprechend Ihrer Anwendung. Um den Auftrag in der Warteschlange zu aktivieren, müssen Sie die [**ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) -Methode abrufen.

Die Methode " [**kreatejob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) " erstellt eine GUID, die den Auftrag eindeutig identifiziert. Verwenden Sie die GUID, um [den Auftrag aus der Übertragungs Warteschlange abzurufen](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob). Der Anzeige Name, den Sie beim Erstellen des Auftrags angeben, ist nicht eindeutig. mehrere Aufträge können denselben Namen verwenden.

Bits schränkt die Anzahl der Aufträge in der Warteschlange auf 300 Aufträge und die Anzahl der Aufträge ein, die ein Benutzer in 60 Auftrag erstellen kann. Diese Grenzwerte gelten nicht für Administratoren oder Dienste. Informationen zum Ändern dieser Standard Limits finden Sie unter [Gruppenrichtlinien](group-policies.md).

Im folgenden Beispiel wird gezeigt, wie ein Download Auftrag erstellt wird. Im Beispiel wird davon ausgegangen, dass die g \_ pbcm-Variable ein gültiger [**ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) -Schnittstellen Zeiger ist. Ausführliche Informationen zum Erstellen des **ibackgroundcopymanager** -Schnittstellen Zeigers finden Sie unter [Herstellen einer Verbindung mit dem BITS-Dienst](connecting-to-the-bits-service.md).


```C++
HRESULT hr;
GUID JobId;
IBackgroundCopyJob* pJob = NULL;

//To create an upload job, replace BG_JOB_TYPE_DOWNLOAD with 
//BG_JOB_TYPE_UPLOAD or BG_JOB_TYPE_UPLOAD_REPLY.
hr = g_pbcm->CreateJob(L"MyJobName", BG_JOB_TYPE_DOWNLOAD, &JobId, &pJob);
if (SUCCEEDED(hr))
{
  //Save the JobId for later reference. 
  //Modify the job's property values.
  //Add files to the job.
  //Activate (resume) the job in the transfer queue.
}
```



Um die aktuelle [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstelle abzurufen, nennen Sie die **ibackgroundcopyjob:: QueryInterface** -Methode. Im folgenden Beispiel wird gezeigt, wie Sie die [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) -Schnittstelle erhalten.


```C++
  HRESULT hr = S_OK;
  IBackgroundCopyJob* pJob = NULL;
  IBackgroundCopyJob5* pJob5 = NULL;

  hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob5), (void**)&pJob5);
  pJob->Release();
  if (FAILED(hr))
  {
    wprintf(L"pJob->QueryInterface failed with 0x%x.\n", hr);
    goto cleanup;
  }
```



 

 




