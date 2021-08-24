---
title: Bestimmen des Status eines Auftrags
description: BITS verwaltet Statusinformationen für jeden Auftrag. Verwenden Sie die Statusinformationen, um zu bestimmen, wie viele Bytes und Dateien übertragen wurden.
ms.assetid: 8bac62b3-cb7e-45ba-85f0-95f3a7e8bffd
keywords:
- Übertragungsauftrag BITS , Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09da4791bffd075d1fb0dd5868f0b78c1b949a0384ff9203555bf18c10ff39cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119323250"
---
# <a name="determining-the-progress-of-a-job"></a>Bestimmen des Status eines Auftrags

BITS verwaltet Statusinformationen für jeden Auftrag. Verwenden Sie die Statusinformationen, um zu bestimmen, wie viele Bytes und Dateien übertragen wurden.

Um Statusinformationen für den Auftrag abzurufen, rufen Sie die [**IBackgroundCopyJob::GetProgress-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) auf, wie im folgenden Beispiel gezeigt. Im Beispiel wird davon ausgegangen, dass [**der IBackgroundCopyJob-Schnittstellenzeiger**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) gültig ist.


```C++
#define PROGRESS_COMPLETE_LEN 50

HRESULT hr;
IBackgroundCopyJob* pJob;
WCHAR szProgressComplete[PROGRESS_COMPLETE_LEN+1];
BG_JOB_PROGRESS Progress;

hr = pJob->GetProgress(&Progress); 
if (FAILED(hr))
{
  //Handle error
}

//Because the BytesTotal member can be 0 or BG_SIZE_UNKNOWN, you may not be able 
//to determine a percentage value to display, such as 57%. It is best to display a 
//string that shows the number of bytes transferred. For example, "123456 of 
//999999" or "123456 of Unknown".
if (BG_SIZE_UNKNOWN == Progress.BytesTotal)
{
  StringCchPrintf(szProgressComplete, PROGRESS_COMPLETE_LEN+1, L"%I64d of Unknown", 
     Progress.BytesTransferred);
}
else
{
  StringCchPrintf(szProgressComplete, PROGRESS_COMPLETE_LEN+1, L"%I64d of %I64d", 
     Progress.BytesTransferred, Progress.BytesTotal); 
}
```



Um Statusinformationen zum Antwortteil eines Uploadantwortauftrags abzurufen, rufen Sie die [**IBackgroundCopyJob2::GetReplyProgress-Methode**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) auf, wie im folgenden Beispiel gezeigt. Im Beispiel wird davon ausgegangen, dass [**der IBackgroundCopyJob-Schnittstellenzeiger**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) gültig ist.


```C++
#define REPLY_COMPLETE_LEN 4

HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
WCHAR szReplyComplete[REPLY_COMPLETE_LEN+1];
BG_JOB_REPLY_PROGRESS Progress;

pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
hr = pJob2->GetReplyProgress(&Progress); 
if (SUCCEEDED(hr))
{
  if (0 == Progress.BytesTotal) //The job type is not BG_JOB_TYPE_UPLOAD_REPLY
  {
    //Logic to deal with this case  
  }
  else if (BG_SIZE_UNKNOWN == Progress.BytesTotal) //The reply has not begun
  {
    StringCchPrintf(szReplyComplete, REPLY_COMPLETE_LEN+1, L"0%%");
  }
  else
  {
    StringCchPrintf(szReplyComplete, REPLY_COMPLETE_LEN+1 L"%I64d%%",
       100*Progress.BytesTransferred/Progress.BytesTotal); 
  }
}
```



Dateien enthalten auch Statusinformationen. Verwenden Sie zum Abrufen der Statusinformationen die [**IBackgroundCopyFile::GetProgress-Methode.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyfile-getprogress) Informationen zum Abrufen der Dateien eines Auftrags finden Sie unter [Aufzählen](enumerating-files-in-a-job.md)von Dateien in einem Auftrag.

 

 




