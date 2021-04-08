---
title: Registrieren zum Ausführen eines Programms
description: Sie können registrieren, damit Bits ein Programm auf der Grundlage von übermittelten Aufträgen und Fehlerereignissen, aber keine Auftrags Änderungs Ereignisse ausführt. Bits führt das Programm im Kontext des Benutzers aus.
ms.assetid: f1996d08-0e35-403b-9cdb-dae9e1c42e05
keywords:
- Ereignis Benachrichtigungs Bits, Befehlszeile
- Registrieren für befehlszeilenbenachrichtigungsbits
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 7831a959a73112b21bdf3e0fbc2b7d3dd4f6a447
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728145"
---
# <a name="registering-to-execute-a-program"></a>Registrieren zum Ausführen eines Programms

Sie können registrieren, damit Bits ein Programm auf der Grundlage von übermittelten Aufträgen und Fehlerereignissen, aber keine Auftrags Änderungs Ereignisse ausführt. Bits führt das Programm im Kontext des Benutzers aus.

**So registrieren Sie sich für die Ausführung eines Programms**

1.  Rufen Sie die **ibackgroundcopyjob:: QueryInterface** -Methode auf, um einen [**IBackgroundCopyJob2**](/windows/desktop/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2) -Schnittstellen Zeiger abzurufen. Geben Sie \_ \_ uuidof (IBackgroundCopyJob2) als Schnittstellen Bezeichner an.
2.  Aufrufen der [**IBackgroundCopyJob2:: setnotifycmdline**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) -Methode, um das auszuführende Programm und alle für das Programm erforderlichen Argumente anzugeben, z. b. den Auftrags Bezeichner.

3.  Aufrufen der [**ibackgroundcopyjob:: setnotifyflags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) -Methode, um anzugeben, wann die Befehlszeile ausgeführt wird.

    Sie können nur die Flags "BG \_ Notify \_ Job überträgt" und " \_ BG \_ Notify \_ Job \_ Error Event" angeben. Das Flag "BG \_ Notify \_ Job-Änderung" \_ wird ignoriert.

Beachten Sie, dass Bits das Programm nicht ausführt, wenn Sie auch [für den Empfang von com](registering-a-com-callback.md) -Rückrufen registriert sind und der Rückruf Schnittstellen Zeiger gültig ist oder die Benachrichtigungs Methode, die Bits aufruft, einen Erfolgs Code zurückgibt. Wenn die Benachrichtigungs Methode jedoch einen Fehlercode zurückgibt, wie z. b. "Fehler" \_ , führt Bits die Befehlszeile aus.

Bits Ruft die [**Funktion "**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) -Funktion" auf, um das Programm zu starten. Wenn Sie eine Parameter Zeichenfolge angeben, muss der erste Parameter der Programmname sein.

Im folgenden Beispiel wird gezeigt, wie Sie sich registrieren, um ein Programm auszuführen, wenn das Auftrags übertragene Ereignis auftritt. Im Beispiel wird davon ausgegangen, dass der [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstellen Zeiger gültig ist.


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



Wenn der Status des Auftrags in den Status der BG- \_ Aufträge \_ \_ übertragen wird, führt Bits das in Pprogram angegebene Programm aus. Das folgende Beispiel ist eine einfache Implementierung eines Programms, das einen Auftrags Bezeichner als Argument annimmt. Das Programm geht davon aus, dass die richtige Anzahl von Argumenten an Sie übermittelt wird.


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



 

 