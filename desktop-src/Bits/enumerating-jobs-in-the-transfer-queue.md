---
title: Auflisten von Aufträgen in der Übertragungs Warteschlange
description: Um Aufträge aus der Übertragungs Warteschlange aufzulisten, müssen Sie die ibackgroundcopymanager-EnumJobs-Methode aufzurufen. Die-Methode gibt einen ienumbackgroundcopyjobs-Schnittstellen Zeiger zurück, den Sie zum Auflisten der Aufträge in der Warteschlange verwenden.
ms.assetid: ebeb1670-dedd-4791-914e-d035d3c22c5a
keywords:
- Übertragen von Auftrags Bits, aufzählen
- Auflisten von Aufträgen in den Bits der Übertragungs Warteschlange
- Warteschlangen Bits übertragen, enumerieren
- Auflisten von Bits
- Auflisten von Bits, Aufträgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9360043a9265248001dddb785edab3e8aac70abc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309319"
---
# <a name="enumerating-jobs-in-the-transfer-queue"></a>Auflisten von Aufträgen in der Übertragungs Warteschlange

Um Aufträge aus der Übertragungs Warteschlange aufzulisten, müssen Sie die [**ibackgroundcopymanager:: EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) -Methode aufzurufen. Die-Methode gibt einen [**ienumbackgroundcopyjobs**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyjobs) -Schnittstellen Zeiger zurück, den Sie zum Auflisten der Aufträge in der Warteschlange verwenden.

Legen Sie den ersten Parameter der [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) -Methode auf 0 fest, um die Aufträge des Benutzers abzurufen. Um alle Aufträge in der Warteschlange abzurufen, legen Sie den ersten Parameter der **EnumJobs** -Methode auf BG \_ Job \_ Enum \_ All \_ Users fest. Nur Benutzer mit Administratorrechten können alle Aufträge in der Übertragungs Warteschlange abrufen.

Beachten Sie, dass es sich bei der aufgelisteten Liste um eine Momentaufnahme der Aufträge in der Übertragungs Warteschlange handelt, wenn Sie die [**EnumJobs**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-enumjobs) -Methode aufzurufen. Die Eigenschaftswerte dieser Aufträge entsprechen jedoch den aktuellen Werten des Auftrags.

Wenn Sie einzelne Übertragungs Aufträge abrufen möchten, rufen Sie die [**ibackgroundcopymanager:: GetJob**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob) -Methode auf.

Informationen zum Aufzählen von Dateien in einem Auftrag finden Sie unter Auflisten von [Dateien in einem Auftrag](enumerating-files-in-a-job.md).

Im folgenden Beispiel wird gezeigt, wie Aufträge in der Übertragungs Warteschlange aufgelistet werden. Die \_ Variable g xfermanager im Beispiel ist ein [**ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) -Schnittstellen Zeiger. Ausführliche Informationen zum Erstellen des **ibackgroundcopymanager** -Schnittstellen Zeigers finden Sie unter [Herstellen einer Verbindung mit dem BITS-Dienst](connecting-to-the-bits-service.md).


```C++
HRESULT hr = 0;
IEnumBackgroundCopyJobs* pJobs = NULL;
IBackgroundCopyJob* pJob = NULL;
ULONG cJobCount = 0;
ULONG idx = 0;

//This example enumerates all jobs in the transfer queue. This call fails if the 
//current user does not have administrator privileges. To enumerate jobs for only 
//the current user, replace BG_JOB_ENUM_ALL_USERS with 0.
hr = g_XferManager->EnumJobs(BG_JOB_ENUM_ALL_USERS, &pJobs);
if (SUCCEEDED(hr))
{
  //Get the count of jobs in the queue. 
  pJobs->GetCount(&cJobCount);

  //Enumerate the jobs in the queue.
  for (idx=0; idx<cJobCount; idx++)
  {
    hr = pJobs->Next(1, &pJob, NULL);
    if (S_OK == hr)
    {
      //Retrieve or set job properties.

      pJob->Release();
      pJob = NULL;
    }
    else
    {
      //Handle error
      break;
    }
  }

  pJobs->Release();
  pJobs = NULL;
}
```



 

 




