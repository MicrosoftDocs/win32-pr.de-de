---
title: Steuern eines Bits-Downloads über eine teure Verbindung
description: Blockieren Sie das Herunterladen über eine teure Verbindung, z. b. eine Roaming-Verbindung.
ms.assetid: 66C20B32-1348-44D9-81F3-43CCED0CEA34
keywords:
- Herunterladen von Bits, Vorgehensweise
- Herunterladen von Bits, kostenaufwendig vermeiden
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 6326838f08f1879929d9a6be67ef94c4aa035e00
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "103857867"
---
# <a name="control-a-bits-download-over-an-expensive-connection"></a>Steuern eines Bits-Downloads über eine teure Verbindung

In diesem Thema wird gezeigt, wie Sie das Herunterladen eines Bits-Auftrags über eine teure Verbindung blockieren, z. b. eine Roaming-Verbindung. Bits ist eine asynchrone API, in der die Anwendung einen Auftrag erstellt, URLs zu diesem Auftrag hinzufügt und die Funktion zum fort [**setzen des Auftrags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) Objekts aufruft. Ab diesem Punkt wählt Bits aus, wann der Auftrag basierend auf Faktoren wie der Auftrags Priorität und der Übertragungs Richtlinie heruntergeladen wird. Nachdem der Auftrag abgeschlossen ist, wird die Anwendung von Bits benachrichtigt, dass die URL heruntergeladen wurde (sofern die Anwendung für die Abschluss Benachrichtigung registriert wurde). Wenn während der Lebensdauer des Vorgangs das Netzwerk des Endbenutzers geändert wird – z. b. wenn der Benutzer unterwegs ist und aktuell Roaminggebühren anfallen –, hält Bits den Auftrag an, bis die Netzwerkbedingungen optimal sind. Die folgenden schrittweisen Anleitungen zeigen, wie Sie den Auftrag erstellen und die entsprechenden Übertragungs Richtlinien Einstellungen angeben.

### <a name="prerequisites"></a>Voraussetzungen

-   Microsoft Visual Studio

## <a name="instructions"></a>Anweisungen

### <a name="step-1-include-the-required-bits-header-files"></a>Schritt 1: einschließen der erforderlichen Bits-Header Dateien

Fügen Sie die folgenden Header Direktiven am Anfang der Quelldatei ein.


```C++
#include <bits.h>
#include <bits5_0.h>
```



### <a name="step-2-initialize-com"></a>Schritt 2: Initialisieren von com

Vor dem Instanziieren der [**ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) -Schnittstelle (die zum Erstellen eines Bits-Auftrags verwendet wird) müssen Sie com initialisieren, das COM-Threading Modell festlegen und eine Identitätswechsel Ebene von mindestens RPC- \_ C \_ IMP- \_ Ebenen annehmen \_ .


```C++
// Initialize COM and specify the COM threading model.
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
if (SUCCEEDED(hr))
{
 // Specify an impersonation level of at least RPC_C_IMP_LEVEL_IMPERSONATE.
 hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                           RPC_C_AUTHN_LEVEL_CONNECT,
                           RPC_C_IMP_LEVEL_IMPERSONATE,
                           NULL, EOAC_NONE, 0);
 if (SUCCEEDED(hr))
 {
  ...
```



### <a name="step-3-instantiate-the-ibackgroundcopymanager-interface"></a>Schritt 3: Instanziieren der ibackgroundcopymanager-Schnittstelle

Verwenden Sie die [**ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) -Schnittstelle zum Erstellen von Übertragungs Aufträgen, rufen Sie ein Enumeratorobjekt ab, das die Aufträge in der Warteschlange enthält, und rufen Sie einzelne Aufträge aus der Warteschlange ab.


```C++
IBackgroundCopyManager* pQueueMgr;

hr = CoCreateInstance(__uuidof(BackgroundCopyManager),
                      NULL,
                      CLSCTX_LOCAL_SERVER,
                      __uuidof(IBackgroundCopyManager),
                      (void **)&pQueueMgr);
```



### <a name="step-4-create-the-bits-job"></a>Schritt 4: Erstellen des Bits-Auftrags

Nur der Benutzer, der den Auftrag erstellt, oder ein Benutzer mit Administratorrechten kann dem Auftrag Dateien hinzufügen und die Eigenschaften des Auftrags ändern.


```C++
GUID guidJob;
IBackgroundCopyJob* pBackgroundCopyJob;

hr = pQueueMgr->CreateJob(L"TransferPolicy",
                          BG_JOB_TYPE_DOWNLOAD,
                          &guidJob,
                          (IBackgroundCopyJob **)&pBackgroundCopyJob);
```



### <a name="step-5-specify-the-transfer-policy-setting-for-the-job"></a>Schritt 5: Angeben der Übertragungs Richtlinien Einstellung für den Auftrag

An dieser Stelle geben Sie die Datenübertragungs Richtlinie für den Kosten Zustand an. \_ \_ Um die gewünschten Ergebnisse zu erzielen, können Sie mehrere Bits-Cost-State-Flags festlegen, indem Sie eine bitweise **or** -Kombination verwenden.


```C++
BITS_JOB_PROPERTY_VALUE propval;
IBackgroundCopyJob5* pBackgroundCopyJob5;

propval.Dword = BITS_COST_STATE_USAGE_BASED
              | BITS_COST_STATE_OVERCAP_THROTTLED
              | BITS_COST_STATE_BELOW_CAP
              | BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
              | BITS_COST_STATE_UNRESTRICTED;

hr = pBackgroundCopyJob->QueryInterface(__uuidof(IBackgroundCopyJob5),
                                        reinterpret_cast<void**>(&pBackgroundCopyJob5));
if(SUCCEEDED(hr))
{
 pBackgroundCopyJob5->SetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, propval);
}
```



## <a name="example"></a>Beispiel

Im folgenden Codebeispiel wird gezeigt, wie die Übertragungs Richtlinie eines Bits-Auftrags so festgelegt wird, dass die Verarbeitung des Auftrags nicht stattfindet, während bestimmte Bedingungen erfüllt werden – z. b. wenn der Benutzer ein Roaming durchführt oder das monatliche Datenübertragungs Limit überschritten hat.


```C++
//*********************************************************
//
//    Copyright (c) Microsoft. All rights reserved.
//    This code is licensed under the Microsoft Public License.
//    THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF
//    ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY
//    IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR
//    PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.
//
//*********************************************************

#define WIN32_LEAN_AND_MEAN             // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>
#include <stdio.h> // define wprintf


int main()
{
 HRESULT hr = S_OK;
 GUID guidJob;
 IBackgroundCopyJob5* pBackgroundCopyJob5;  
 IBackgroundCopyJob* pBackgroundCopyJob;
 IBackgroundCopyManager* pQueueMgr;
 BITS_JOB_PROPERTY_VALUE propval;

 // Specify the COM threading model.
 hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
 if (SUCCEEDED(hr))
 {
  // The impersonation level must be at least RPC_C_IMP_LEVEL_IMPERSONATE.
  hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                            RPC_C_AUTHN_LEVEL_CONNECT,
                            RPC_C_IMP_LEVEL_IMPERSONATE,
                            NULL, EOAC_NONE, 0);

  if (SUCCEEDED(hr))
  {
   hr = CoCreateInstance(__uuidof(BackgroundCopyManager), 
                         NULL,
                         CLSCTX_LOCAL_SERVER,
                         __uuidof(IBackgroundCopyManager),
                         (void **)&pQueueMgr);

   if (FAILED(hr))
   {
    // Failed to connect to BITS.
    wprintf(L"Failed to connect to BITS with error %x\n",hr);
    goto done;
   }

   // Create a BITS job.
   wprintf(L"Creating Job...\n");

   hr = pQueueMgr->CreateJob(L"TransferPolicy",
                             BG_JOB_TYPE_DOWNLOAD,
                             &guidJob,
                             (IBackgroundCopyJob **)&pBackgroundCopyJob);

   if (FAILED(hr))
   {
    wprintf(L"Failed to Create Job, error = %x\n",hr);
    goto cancel;
   }

   wprintf(L" Job is succesfully created ...\n");

   // Set the Transfer Policy for the job.
   propval.Dword = BITS_COST_STATE_USAGE_BASED 
                 | BITS_COST_STATE_OVERCAP_THROTTLED
                 | BITS_COST_STATE_BELOW_CAP
                 | BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
                 | BITS_COST_STATE_UNRESTRICTED;

   hr = pBackgroundCopyJob->QueryInterface(
         __uuidof(IBackgroundCopyJob5),
         reinterpret_cast<void**>(&pBackgroundCopyJob5)
        );

   if (FAILED(hr))
   {
    wprintf(L"Failed to Create Job, error = %x\n",hr);
    goto cancel;
   }
   pBackgroundCopyJob5->SetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, propval);

   // Get the Transfer Policy for the new job.
   BITS_JOB_PROPERTY_VALUE actual_propval;

   wprintf(L"Getting TransferPolicy Property ...\n");

   hr = pBackgroundCopyJob5->GetProperty(BITS_JOB_PROPERTY_ID_COST_FLAGS, 
                                         &actual_propval);
   if (FAILED(hr))
   {
    // SetSSLSecurityFlags failed.
    wprintf(L"GetProperty failed with error %x\n",hr);
    goto cancel;
   }

   DWORD job_transferpolicy = actual_propval.Dword;
   wprintf(L"get TransferPolicy Property returned %#x\n", job_transferpolicy);
  }
done:
  CoUninitialize();
 }
 return 1;

cancel:
 pBackgroundCopyJob->Cancel(); 
 pBackgroundCopyJob->Release();
 goto done;
}
```



 

 




