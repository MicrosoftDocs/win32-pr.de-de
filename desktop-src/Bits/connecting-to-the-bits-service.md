---
title: Herstellen einer Verbindung mit dem BITS-Dienst
description: Zum Herstellen einer Verbindung mit dem BITS-Dienst erstellen Sie eine Instanz des backgroundcopymanager-Objekts, wie im folgenden Beispiel gezeigt.
ms.assetid: 2fa88277-c7a1-4f1c-a63c-e2d27a163249
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 8146fa0def8c9c7dfd976784a930f35f20c965eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101862"
---
# <a name="connecting-to-the-bits-service"></a>Herstellen einer Verbindung mit dem BITS-Dienst

Zum Herstellen einer Verbindung mit dem Bits-Systemdienst erstellen Sie eine Instanz des backgroundcopymanager-Objekts, wie im folgenden Beispiel gezeigt. Der Bits-Systemdienst ist der Windows-Systemdienst, der auf dem Client Computer ausgeführt wird, der die Hintergrund Übertragungsfunktion implementiert.


```C++
#define WIN32_LEAN_AND_MEAN // Exclude rarely-used stuff from Windows headers
#include <windows.h>
#include <bits.h>

//Global variable that several of the code examples in this document reference.
IBackgroundCopyManager* g_pbcm = NULL;  
HRESULT hr;

//Specify the appropriate COM threading model for your application.
hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
if (SUCCEEDED(hr))
{
  hr = CoCreateInstance(__uuidof(BackgroundCopyManager), NULL,
                        CLSCTX_LOCAL_SERVER,
                        __uuidof(IBackgroundCopyManager),
                        (void**) &g_pbcm);
  if (SUCCEEDED(hr))
  {
    //Use g_pbcm to create, enumerate, or retrieve jobs from the queue.
  }
}
```



Um auf eine bestimmte Version von Bits zu testen, verwenden Sie einen symbolischen Klassen Bezeichner für backgroundcopymanager, der auf der Version basiert, die Sie überprüfen möchten. Wenn Sie z. b. auf Bits 10,2 testen möchten, verwenden Sie CLSID \_ BackgroundCopyManager10 \_ 2.

Im folgenden Beispiel wird gezeigt, wie Sie einen der symbolischen Klassen Bezeichner verwenden.


```C++
  hr = CoCreateInstance(CLSID_BackgroundCopyManager5_0, NULL,
                        CLSCTX_LOCAL_SERVER,
                        IID_IBackgroundCopyManager,
                        (void**) &g_pbcm);
  if (SUCCEEDED(hr))
  {
    //BITS 5.0 is installed.
  }
```



Verwenden Sie die Methoden der [**ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) -Schnittstelle, um [Übertragungs Aufträge zu erstellen](creating-a-job.md), Aufträge in der Warteschlange [aufzuzählen](enumerating-jobs-in-the-transfer-queue.md) und [Aufträge abzurufen](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).



Bits erfordert, dass die Schnittstellen Proxys des Clients entweder den Identitätswechsel oder die Identitätswechsel Ebene des Identitäts Wechsels verwenden. Wenn die Anwendung nicht [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)aufruft, verwendet com standardmäßig die Identifizierung. Bits schlägt mit E \_ AccessDenied fehl, wenn die korrekte Identitätswechsel Ebene nicht festgelegt ist. Wenn Sie eine Bibliothek bereitstellen, die die Bits-Schnittstellen ausführt, und eine Anwendung, die Ihre Bibliothek aufruft, die Identitätswechsel Ebene unter Identifizieren festlegt, müssen Sie [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) aufrufen, um die korrekte Identitätswechsel Ebene für jede von Ihnen aufgerufenen Bits-Schnittstelle festzulegen.

Bevor die Anwendung beendet wird, geben Sie Ihre Kopie des [**ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) -Schnittstellen Zeigers frei, wie im folgenden Beispiel gezeigt.


```C++
if (g_pbcm)
{
  g_pbcm->Release();
  g_pbcm = NULL;
}
CoUninitialize();
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufrufen von Bits aus .net und c#](/windows/desktop/Bits/bits-dot-net) für Bits
</dt> </dl>

 

 