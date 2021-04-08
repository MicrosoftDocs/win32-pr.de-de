---
title: Auflisten von Dateien in einem Auftrag
description: Um Dateien in einem Auftrag aufzuzählen, können Sie die ibackgroundcopyjob-EnumFiles-Methode abrufen. Die-Methode gibt einen ienumbackgroundcopyfiles-Schnittstellen Zeiger zurück, mit dem Sie die Dateien aufzählen.
ms.assetid: 0e1fa024-4576-434c-bc5f-518d246b5faa
keywords:
- Übertragen von Auftrags Bits, Auflisten von Dateien
- Auflisten von Datei Bits
- Auflisten von Bits, Dateien
- Datei Übertragungs Bits, auflisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0db704e47a0e075801de2434ed30ba6fb8d8c91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708136"
---
# <a name="enumerating-files-in-a-job"></a>Auflisten von Dateien in einem Auftrag

Um Dateien in einem Auftrag aufzulisten, müssen Sie die [**ibackgroundcopyjob:: EnumFiles**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) -Methode aufzurufen. Die-Methode gibt einen [**ienumbackgroundcopyfiles**](/windows/desktop/api/Bits/nn-bits-ienumbackgroundcopyfiles) -Schnittstellen Zeiger zurück, mit dem Sie die Dateien aufzählen.

Beachten Sie, dass es sich bei der aufgelisteten Liste um eine Momentaufnahme der Dateien im Auftrag handelt, wenn Sie die [**EnumFiles**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles) -Methode aufgerufen haben. Die Eigenschaftswerte dieser Datei Objekte entsprechen jedoch den aktuellen Werten der Datei.

Im folgenden Beispiel wird gezeigt, wie Sie Dateien in einem Auftrag aufzählen und deren Eigenschaften abrufen. Im Beispiel wird davon ausgegangen, dass der [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstellen Zeiger gültig ist.


```C++
HRESULT hr = 0;
IBackgroundCopyJob* pJob;
IEnumBackgroundCopyFiles* pFiles = NULL;
IBackgroundCopyFile* pFile = NULL;
IBackgroundCopyFile3* pFile3 = NULL;
WCHAR* pLocalFileName = NULL;
ULONG cFileCount = 0;
ULONG idx = 0;

hr = pJob->EnumFiles(&pFiles);
if (SUCCEEDED(hr))
{
  //Get the count of files in the job. 
  pFiles->GetCount(&cFileCount);

  //Enumerate the files in the job.
  for (idx=0; idx<cFileCount; idx++)
  {
    hr = pFiles->Next(1, &pFile, NULL);
    if (S_OK == hr)
    {
      // Query for the latest file interface.
      hr = pFile->QueryInterface(__uuidof(IBackgroundCopyFile3), (void**)&pFile3);
      pFile->Release();
      if (FAILED(hr))
      {
        wprintf(L"pFile->QueryInterface failed with 0x%x.\n", hr);
        goto cleanup;
      }

      // You can use the interface to retrieve the local and remote file
      // names, get the ranges to download if only part of the file content
      // is requested, determine the progress of the transfer, change the remote file
      // name, get the name of the temporary file that BITS uses to download
      // the file, determine if the file is downloaded from a peer, and set
      // the validation state of the file so it can be shared with peers.

      //Get the local name of the file.
      hr = pFile3->GetLocalName(&pLocalFileName);
      if (SUCCEEDED(hr))
      {
        //Do something with the file information.
      }

      CoTaskMemFree(pLocalFileName); 
      pFile3->Release();
      pFile3 = NULL;
    }
    else
    {
      //Handle error
      break;
    }
  }

  pFiles->Release();
  pFiles = NULL;
}
```



 

 




