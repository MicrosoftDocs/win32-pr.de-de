---
title: Behandeln von Fehlern (Bits)
description: Es gibt zwei Arten von Fehlern, die in Ihrer Anwendung behandelt werden müssen.
ms.assetid: cbc182ce-c853-492e-8953-21c54500875b
keywords:
- Behandeln von Fehler Bits
- Übertragen von Auftrags Bits, Fehlern
- Fehler Bits
- Fehler Bits, Behandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1544788192d4bfd778fef83caaca922f1f84c01e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039923"
---
# <a name="handling-errors-bits"></a>Behandeln von Fehlern (Bits)

Es gibt zwei Arten von Fehlern, die in Ihrer Anwendung behandelt werden müssen. Der erste Fehler ist ein fehlerhafter Methoden aufzurufen. Jede Methode gibt einen **HRESULT** -Wert zurück. Die Referenzseite für jede Methode identifiziert die Rückgabewerte, die mit der höchsten Wahrscheinlichkeit generiert werden. Weitere Rückgabewerte finden Sie unter [Bits-Rückgabewerte](bits-return-values.md). Um den Nachrichtentext zu erhalten, der dem Rückgabewert zugeordnet ist, müssen Sie die [**ibackgroundcopymanager:: GetErrorDescription**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-geterrordescription) -Methode aufrufen.

Der zweite zu behandelnde Fehlertyp ist ein Auftrag, dessen [Status](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) in den Status " [BG- \_ Auftrags \_ Status \_](/windows/desktop/api/Bits/ne-bits-bg_job_state) " oder " **BG- \_ Auftrags \_ Status \_ vorübergehender \_ Fehler**" übergeht. Um Informationen zu diesen Arten von Fehlern abzurufen, rufen Sie die [**ibackgroundcopyjob:: getError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror) -Methode des Auftrags auf. Die-Methode gibt einen [**ibackgroundcopyerror**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) -Schnittstellen Zeiger zurück, der Informationen enthält, die Sie verwenden, um die Ursache des Fehlers zu bestimmen. Sie können auch eine Fehler Benachrichtigung erhalten, indem Sie sich für den Empfang von Ereignis Benachrichtigungen registrieren. Weitere Informationen finden Sie unter [Registrieren eines com-Rückrufs](registering-a-com-callback.md).

Bits betrachtet jeden Auftrag als atomarisch. Wenn eine der Dateien im Auftrag einen Fehler generiert, verbleibt der Auftrag in einem Fehlerzustand, bis der Fehler behoben wurde. Daher können Sie die Datei, die den Fehler verursacht, nicht aus dem Auftrag löschen. Wenn der Fehler jedoch dadurch verursacht wird, dass der Server nicht verfügbar oder eine ungültige Remote Datei ist, können Sie die [**IBackgroundCopyJob3:: REPLACEREMOTEPREFIX**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyjob3-replaceremoteprefix) -Methode oder die [**IBackgroundCopyFile2:: Setup Report**](/windows/desktop/api/Bits2_0/nf-bits2_0-ibackgroundcopyfile2-setremotename) Name-Methode zum Identifizieren eines neuen Servers oder Datei namens abrufen.

Nachdem Sie die Ursache des Fehlers bestimmt haben, führen Sie eine der folgenden Optionen aus:

-   Brechen Sie den Auftrag ab, indem Sie die [**ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) -Methode aufrufen.
-   Bei einem Download Auftrag wird die [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode aufgerufen, um die Dateien zu speichern, die vor dem Auftreten des Fehlers erfolgreich übertragen wurden.
-   Beheben Sie den Fehler, und wenden Sie die [**ibackgroundcopyjob:: Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) -Methode an, um den Auftrag abzuschließen.

Überprüfen Sie bei einem Upload-Antwort-Auftrag den Wert des **bytesTotal** -Members der Status Struktur der [**BG- \_ Auftrags \_ Antwort \_**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_job_reply_progress) , um zu ermitteln, ob der Fehler im Upload-oder Reply-Teil des Auftrags aufgetreten ist. Der Fehler ist beim Hochladen aufgetreten, wenn der Wert BG- \_ Größe \_ unbekannt ist.

Im folgenden Beispiel wird gezeigt, wie ein [**ibackgroundcopyerror**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyerror) -Schnittstellen Zeiger abgerufen wird. Im Beispiel wird davon ausgegangen, dass der [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstellen Zeiger gültig ist.


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



 

 




