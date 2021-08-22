---
title: Erstellen eines Auftrags
description: Rufen Sie zum Erstellen eines Übertragungsauftrags die CreateJob-Methode IBackgroundCopyManager auf.
ms.assetid: a7d9feef-4beb-4ae5-9453-9157ee3ec0e8
keywords:
- Bits für Übertragungsauftrag
- BITS des Übertragungsauftrags , erstellen
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 0241d855d60178e87f28820f14b39e497f200fe5770933f293257e62b2d1b601
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528889"
---
# <a name="creating-a-job"></a>Erstellen eines Auftrags

Rufen Sie zum Erstellen eines Übertragungsauftrags die [**IBackgroundCopyManager::CreateJob-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) auf. Nachdem BITS den Auftrag erstellt hat, [](setting-and-retrieving-the-properties-of-a-job.md) fügen Sie dem Auftrag Dateien [hinzu,](adding-files-to-a-job.md) und ändern Sie die Eigenschaften des Auftrags entsprechend Ihrer Anwendung. Um den Auftrag in der Warteschlange zu aktivieren, rufen Sie die [**IBackgroundCopyJob::Resume-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) auf.

Die [**CreateJob-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-createjob) erstellt eine GUID, die den Auftrag eindeutig identifiziert. Sie verwenden die GUID, um [den Auftrag aus der Übertragungswarteschlange abzurufen.](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) Der Anzeigename, den Sie beim Erstellen des Auftrags angeben, ist nicht eindeutig. mehr als ein Auftrag kann denselben Namen verwenden.

BITS beschränkt die Anzahl der Aufträge in der Warteschlange auf 300 Aufträge und die Anzahl der Aufträge, die ein Benutzer erstellen kann, auf 60 Aufträge. Diese Grenzwerte gelten nicht für Administratoren oder Dienste. Informationen zum Ändern dieser Standardgrenzwerte finden Sie unter [Gruppenrichtlinien.](group-policies.md)

Das folgende Beispiel zeigt, wie Sie einen Downloadauftrag erstellen. Im Beispiel wird davon ausgegangen, dass die Variable g \_ pbcm ein gültiger [**IBackgroundCopyManager-Schnittstellenzeiger**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) ist. Weitere Informationen zum Erstellen des **IBackgroundCopyManager-Schnittstellenzeigers** finden Sie unter Herstellen einer Verbindung [mit dem BITS-Dienst.](connecting-to-the-bits-service.md)


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



Um die neueste [**IBackgroundCopyJob-Schnittstelle zu**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) erhalten, rufen Sie die **IBackgroundCopyJob::QueryInterface-Methode** auf. Das folgende Beispiel zeigt, wie die [**IBackgroundCopyJob5-Schnittstelle erhalten**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) wird.


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



 

 




