---
title: Registrieren für die Ausführung eines Programms
description: Sie können sich registrieren, damit BITS ein Programm basierend auf übertragenen Aufträgen und Fehlerereignissen ausführen kann, jedoch nicht auf Auftrags geänderten Ereignissen. BITS führt das Programm im Kontext des Benutzers aus.
ms.assetid: f1996d08-0e35-403b-9cdb-dae9e1c42e05
keywords:
- Ereignisbenachrichtigung BITS , Befehlszeile
- Registrieren für Bits für Befehlszeilenbenachrichtigungen
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: db86f67ad899d190b24d74bfb04c501ca7881351cfb2f37ef53300666622c317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922030"
---
# <a name="registering-to-execute-a-program"></a>Registrieren für die Ausführung eines Programms

Sie können sich registrieren, damit BITS ein Programm basierend auf übertragenen Aufträgen und Fehlerereignissen ausführen kann, jedoch nicht auf Auftrags geänderten Ereignissen. BITS führt das Programm im Kontext des Benutzers aus.

**So registrieren Sie sich zum Ausführen eines Programms**

1.  Rufen Sie die **IBackgroundCopyJob::QueryInterface-Methode auf,** um einen [**IBackgroundCopyJob2-Schnittstellenzeiger**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) abzurufen. Geben \_ \_ Sie uuidof(IBackgroundCopyJob2) als Schnittstellenbezeichner an.
2.  Rufen Sie [**die IBackgroundCopyJob2::SetNotifyCmdLine-Methode**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) auf, um das auszuführende Programm und alle vom Programm benötigten Argumente anzugeben, z. B. den Auftragsbezeichner.

3.  Rufen Sie die [**IBackgroundCopyJob::SetNotifyFlags-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) auf, um anzugeben, wann die Befehlszeile ausgeführt wird.

    Sie können nur die Ereignisflags BG \_ NOTIFY \_ JOB \_ TRANSFERD und BG NOTIFY JOB \_ \_ ERROR \_ angeben. Das BG \_ NOTIFY \_ JOB \_ MODIFICATION-Flag wird ignoriert.

Beachten Sie, dass BITS das [](registering-a-com-callback.md) Programm nicht ausführen wird, wenn Sie sich auch für den Empfang von COM-Rückrufen registriert haben und der Rückrufschnittstellenzeiger gültig ist oder die von BITS aufrufte Benachrichtigungsmethode einen Erfolgscode zurückgibt. Wenn die Benachrichtigungsmethode jedoch einen Fehlercode zurückgibt, z. B. E FAIL, führt \_ BITS die Befehlszeile aus.

BITS ruft die [**CreateProcessAsUser-Funktion auf,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) um das Programm zu starten. Wenn Sie eine Parameterzeichenfolge angeben, muss der erste Parameter der Programmname sein.

Das folgende Beispiel zeigt, wie Sie sich registrieren, um ein Programm auszuführen, wenn das ereignis übertragene Auftrag eintritt. Im Beispiel wird davon ausgegangen, dass [**der IBackgroundCopyJob-Schnittstellenzeiger**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) gültig ist.


```C++
#define MAX_PARAMETER_LEN 4000

HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
WCHAR szJobId[48];
const WCHAR *pProgram = L"c:\\PATHHERE\\PROGRAMNAMEHERE.exe";
WCHAR szParameters[MAX_PARAMETER_LEN+1];
GUID JobId;
int rc;

hr = pJob->GetId(&JobId);
if (SUCCEEDED(hr))
{
  rc = StringFromGUID2(JobId, szJobId, ARRAYSIZE(szJobId));
  if (rc)
  {
    StringCchPrintf(szParameters, MAX_PARAMETER_LEN+1, L"%s %s", pProgram, szJobId);
    pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
    hr = pJob2->SetNotifyCmdLine(pProgram, szParameters);
    if (SUCCEEDED(hr))
    {
      hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED);
    }
    pJob2->Release();
    if (FAILED(hr))
    {
      //Handle error - unable to register for command line notification.
    }
  }
}
```



Wenn der Status des Auftrags BG \_ JOB \_ STATE TRANSFERD wird, führt BITS das in \_ pProgram angegebene Programm aus. Das folgende Beispiel ist eine einfache Implementierung eines Programms, das einen Auftragsbezeichner als Argument verwendet. Das Programm geht davon aus, dass die richtige Anzahl von Argumenten übergeben wird.


```C++
#define WIN32_LEAN_AND_MEAN // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>
#include <strsafe.h>

int wmain(int argc, wchar_t *argv[])
{
 HRESULT hr;
 IBackgroundCopyManager *pManager = NULL;
 IBackgroundCopyJob *pJob = NULL;
 GUID JobId;
 LPWSTR pDisplayName = NULL;
 LPCWSTR pSuccessString = L" completed successfully.";
 LPWSTR pMessage;

 hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
 hr = CoCreateInstance(__uuidof(BackgroundCopyManager),
  NULL, CLSCTX_LOCAL_SERVER,
  __uuidof(IBackgroundCopyManager), (void**)&pManager);

 if (pManager)
 {
  hr = CLSIDFromString(argv[1], &JobId);
  if (SUCCEEDED(hr))
  {
   hr = pManager->GetJob(JobId, &pJob);
   if (SUCCEEDED(hr))
   {
    hr = pJob->GetDisplayName(&pDisplayName);
    if (SUCCEEDED(hr))
    {
     int messageLen = wcslen(pDisplayName) + wcslen(pSuccessString) + 1;
     pMessage = (WCHAR*)malloc(messageLen * sizeof(WCHAR));
     if (pMessage)
     {
      StringCchPrintf(pMessage, messageLen,
       L"%s%s", pDisplayName, pSuccessString);
      MessageBox(HWND_DESKTOP, pMessage, L"MyProgram - Transferred", MB_OK);
      free(pMessage);
     }
     else
     {
      hr = E_OUTOFMEMORY;
     }
     CoTaskMemFree(pDisplayName);
    }
    pJob->Release();
   }
  }
  pManager->Release();
 }

 CoUninitialize();
 return(hr);
}
```



 

 