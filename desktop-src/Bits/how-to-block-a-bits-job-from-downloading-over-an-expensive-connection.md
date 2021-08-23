---
title: Steuern eines BITS-Downloads über eine teure Verbindung
description: Blockieren Sie das Herunterladen über eine teure Verbindung, z. B. eine Roamingverbindung.
ms.assetid: 66C20B32-1348-44D9-81F3-43CCED0CEA34
keywords:
- Herunterladen von BITS , How to
- lädt BITS herunter und vermeidet teure
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 7cb09dbd277d9ec74ce4988db210bf80c22d97ccaa3054a170fc1c9913282cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959489"
---
# <a name="control-a-bits-download-over-an-expensive-connection"></a>Steuern eines BITS-Downloads über eine teure Verbindung

In diesem Thema wird gezeigt, wie Sie das Herunterladen eines BITS-Auftrags über eine teure Verbindung wie eine Roamingverbindung blockieren. BITS ist eine asynchrone API, bei der die Anwendung einen Auftrag erstellt, diesem Auftrag URLs hinzufügt und die Resume-Funktion des [**Auftragsobjekts**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) aufruft. Ab diesem Punkt wählt BITS aus, wann der Auftrag basierend auf Faktoren wie Auftragspriorität und Übertragungsrichtlinie heruntergeladen wird. Nachdem der Download des Auftrags abgeschlossen ist, benachrichtigt BITS die Anwendung, dass die URL heruntergeladen wurde (wenn die Anwendung für die Abschlussbenachrichtigung registriert wurde). Wenn sich während der Lebensdauer des Auftrags das Netzwerk des Endbenutzers ändert , z. B. wenn der Benutzer unterwegs ist und derzeit Roaminggebühren anfallen, hält BITS den Auftrag an, bis die Netzwerkbedingungen optimal sind. Die folgenden Schritt-für-Schritt-Anweisungen zeigen, wie Sie den Auftrag erstellen und die entsprechenden Übertragungsrichtlinieeinstellungen angeben.

### <a name="prerequisites"></a>Voraussetzungen

-   Microsoft Visual Studio

## <a name="instructions"></a>Anweisungen

### <a name="step-1-include-the-required-bits-header-files"></a>Schritt 1: Hinzufügen der erforderlichen BITS-Headerdateien

Fügen Sie am Anfang der Quelldatei die folgenden Header-Direktiven ein.


```C++
#include <bits.h>
#include <bits5_0.h>
```



### <a name="step-2-initialize-com"></a>Schritt 2: Initialisieren von COM

Vor dem Instanziieren der [**IBackgroundCopyManager-Schnittstelle**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) (die zum Erstellen eines BITS-Auftrags verwendet wird) müssen Sie COM initialisieren, das COM-Threadingmodell festlegen und eine Identitätswechselebene von mindestens RPC \_ C IMP LEVEL \_ \_ \_ IMPERSONATE angeben.


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



### <a name="step-3-instantiate-the-ibackgroundcopymanager-interface"></a>Schritt 3: Instanziieren der IBackgroundCopyManager-Schnittstelle

Verwenden Sie die [**IBackgroundCopyManager-Schnittstelle,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) um Übertragungsaufträge zu erstellen, ein Enumeratorobjekt abzurufen, das die Aufträge in der Warteschlange enthält, und einzelne Aufträge aus der Warteschlange abzurufen.


```C++
IBackgroundCopyManager* pQueueMgr;

hr = CoCreateInstance(__uuidof(BackgroundCopyManager),
                      NULL,
                      CLSCTX_LOCAL_SERVER,
                      __uuidof(IBackgroundCopyManager),
                      (void **)&pQueueMgr);
```



### <a name="step-4-create-the-bits-job"></a>Schritt 4: Erstellen des BITS-Auftrags

Nur der Benutzer, der den Auftrag erstellt, oder ein Benutzer mit Administratorrechten kann dem Auftrag Dateien hinzufügen und die Eigenschaften des Auftrags ändern.


```C++
GUID guidJob;
IBackgroundCopyJob* pBackgroundCopyJob;

hr = pQueueMgr->CreateJob(L"TransferPolicy",
                          BG_JOB_TYPE_DOWNLOAD,
                          &guidJob,
                          (IBackgroundCopyJob **)&pBackgroundCopyJob);
```



### <a name="step-5-specify-the-transfer-policy-setting-for-the-job"></a>Schritt 5: Angeben der Übertragungsrichtlinie für den Auftrag

Hier geben Sie die Richtlinie für die Kostenstatusübertragung an. Sie können mehrere BITS \_ COST \_ STATE-Flags festlegen, indem Sie eine bitweise **OR-Kombination** verwenden, um die gewünschten Ergebnisse zu erzielen.


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

Das folgende Codebeispiel zeigt, wie die Übertragungsrichtlinie eines BITS-Auftrags so festgelegt wird, dass die Verarbeitung des Auftrags nicht erfolgt, während bestimmte Bedingungen erfüllt sind, z. B. wenn der Benutzer roamingt oder sein monatliches Datenübertragungslimit überschritten hat.


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



 

 




