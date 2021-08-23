---
title: Behandeln von Fehlern (BITS)
description: Es gibt zwei Arten von Fehlern, die in Ihrer Anwendung behandelt werden müssen.
ms.assetid: cbc182ce-c853-492e-8953-21c54500875b
keywords:
- Behandeln von Fehlern BITS
- BITS- und Fehlerübertragungsauftrag
- Fehler BITS
- Fehler BITS , Behandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1b0f389b6f0bdeefdfd5868b444384af26027b9b688a8fb83ba89ea370b9360
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528810"
---
# <a name="handling-errors-bits"></a>Behandeln von Fehlern (BITS)

Es gibt zwei Arten von Fehlern, die in Ihrer Anwendung behandelt werden müssen. Der erste Fehler ist ein fehlgeschlagener Methodenaufruf. Jede Methode gibt einen **HRESULT-Wert** zurück. Die Referenzseite für jede Methode identifiziert die Rückgabewerte, die sie am wahrscheinlichsten generiert. Weitere Rückgabewerte finden Sie unter [BITS-Rückgabewerte.](bits-return-values.md) Um den dem Rückgabewert zugeordneten Meldungstext abzurufen, rufen Sie die [**IBackgroundCopyManager::GetErrorDescription-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) auf.

Der zweite zu behandelnde Fehlertyp [](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) ist ein Auftrag, dessen Status in [BG JOB \_ STATE \_ \_ ERROR](/windows/desktop/api/Bits/ne-bits-bg_job_state) oder **BG JOB STATE TRANSIENT ERROR \_ \_ \_ \_ übergegangen ist.** Um Informationen zu diesen Fehlertypen abzurufen, rufen Sie die [**IBackgroundCopyJob::GetError-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) des Auftrags auf. Die -Methode gibt einen [**IBackgroundCopyError-Schnittstellenzeiger**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) zurück, der Informationen enthält, mit denen Sie die Ursache des Fehlers bestimmen. Sie können auch eine Fehlerbenachrichtigung erhalten, indem Sie sich für den Empfang von Ereignisbenachrichtigungen registrieren. Weitere Informationen finden Sie unter [Registrieren eines COM-Rückrufs.](registering-a-com-callback.md)

BITS betrachtet jeden Auftrag als atomar. Wenn eine der Dateien im Auftrag einen Fehler generiert, verbleibt der Auftrag in einem Fehlerzustand, bis der Fehler behoben ist. Daher können Sie die Datei, die den Fehler verursacht, nicht aus dem Auftrag löschen. Wenn der Fehler jedoch dadurch verursacht wird, dass der Server nicht verfügbar ist oder eine ungültige Remotedatei vorhanden ist, können Sie die [**IBackgroundCopyJob3::ReplaceRemotePrefix-**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) oder [**IBackgroundCopyFile2::SetRemoteName-Methode**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) aufrufen, um einen neuen Server- oder Dateinamen zu identifizieren.

Nachdem Sie die Ursache des Fehlers bestimmt haben, führen Sie eine der folgenden Optionen aus:

-   Brechen Sie den Auftrag ab, indem Sie [**die IBackgroundCopyJob::Cancel-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) aufrufen.
-   Rufen Sie für einen Downloadauftrag die [**IBackgroundCopyJob::Complete-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) auf, um die Dateien zu speichern, die vor dem Fehler erfolgreich übertragen wurden.
-   Beheben Sie den Fehler, und rufen Sie die [**IBackgroundCopyJob::Resume-Methode auf,**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) um den Auftrag zu beenden.

Überprüfen Sie bei einem Upload-Antwort-Auftrag den Wert des **BytesTotal-Mitglieds** der [**BG JOB REPLY \_ \_ \_ PROGRESS-Struktur,**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) um zu ermitteln, ob der Fehler im Upload- oder Antwortteil des Auftrags aufgetreten ist. Der Fehler ist beim Upload aufgetreten, wenn der Wert BG \_ SIZE \_ UNKNOWN ist.

Das folgende Beispiel zeigt, wie ein [**IBackgroundCopyError-Schnittstellenzeiger**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) abgerufen wird. Im Beispiel wird davon ausgegangen, dass [**der IBackgroundCopyJob-Schnittstellenzeiger**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) gültig ist.


```C++
HRESULT hr = 0;
HRESULT hrError = 0;
IBackgroundCopyJob* pJob;
IBackgroundCopyError* pError = NULL;
IBackgroundCopyFile* pFile = NULL;
WCHAR* pszDescription = NULL;
WCHAR* pszRemoteName = NULL;
BG_ERROR_CONTEXT Context;

hr = pJob->GetError(&pError);
if (SUCCEEDED(hr))
{
  //Retrieve the HRESULT associated with the error. The context tells you
  //where the error occurred, for example, in the transport, queue manager, the 
  //local file, or the remote file.
  pError->GetError(&Context, &hrError);  

  //Retrieve a description associated with the HRESULT value.
  hr = pError->GetErrorDescription(LANGIDFROMLCID(GetThreadLocale()), &pszDescription);
  if (SUCCEEDED(hr))
  {
    if (BG_ERROR_CONTEXT_REMOTE_FILE == Context)
    {
      hr = pError->GetFile(&pFile);  
      if (SUCCEEDED(hr))
      {
        hr = pFile->GetRemoteName(&pszRemoteName);
        if (SUCCEEDED(hr))
        {
          //Do something with the information.
          CoTaskMemFree(pszRemoteName);
        }
        pFile->Release();
      }
    }
    CoTaskMemFree(pszDescription);
  }
  pError->Release();
}
else
{
  //Error information is not available.
}
```



 

 




