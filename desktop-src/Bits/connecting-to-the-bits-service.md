---
title: Herstellen einer Verbindung mit dem BITS-Dienst
description: Um eine Verbindung mit dem BITS-Dienst herzustellen, erstellen Sie eine Instanz des BackgroundCopyManager-Objekts, wie im folgenden Beispiel gezeigt.
ms.assetid: 2fa88277-c7a1-4f1c-a63c-e2d27a163249
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 5dacd97b78fa9c5d3a1e410a44e3c376368654e99a6f4ace9161d36b127d9a94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528940"
---
# <a name="connecting-to-the-bits-service"></a>Herstellen einer Verbindung mit dem BITS-Dienst

Um eine Verbindung mit dem BITS-Systemdienst herzustellen, erstellen Sie eine Instanz des BackgroundCopyManager-Objekts, wie im folgenden Beispiel gezeigt. Der BITS-Systemdienst ist der Windows, der auf dem Clientcomputer ausgeführt wird und die Hintergrundübertragungsfunktion implementiert.


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



Um auf eine bestimmte Version von BITS zu testen, verwenden Sie einen symbolischen Klassenbezeichner für BackgroundCopyManager basierend auf der Version, die Sie überprüfen möchten. Verwenden Sie z. B. CLSID \_ BackgroundCopyManager10 2, um auf BITS 10.2 \_ zu testen.

Im folgenden Beispiel wird die Verwendung eines der symbolischen Klassenbezeichner veranschaulicht.


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



Verwenden Sie die Methoden der [**IBackgroundCopyManager-Schnittstelle,**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) um Übertragungsaufträge zu [erstellen,](creating-a-job.md)Aufträge in der [Warteschlange](enumerating-jobs-in-the-transfer-queue.md) aufzählen und [Aufträge abzurufen.](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob)



BITS erfordert, dass die Schnittstellenproxies des Clients entweder die IDENTITÄTSWECHSEL- oder IMPERSONATE-Ebene des Identitätswechsels verwenden. Wenn die Anwendung [**CoInitializeSecurity nicht aufruft,**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)verwendet COM standardmäßig IDENTIFY. BITS schlägt mit E \_ ACCESSDENIED fehl, wenn die richtige Identitätswechselebene nicht festgelegt ist. Wenn Sie eine Bibliothek bereitstellen, die die BITS-Schnittstellen trainiert, und eine Anwendung, die Ihre Bibliothek aufruft, die Identitätswechselebene unter IDENTIFY legt, müssen Sie [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) aufrufen, um die richtige Identitätswechselebene für jede bits-Schnittstelle, die Sie aufrufen, festlegen.

Bevor Ihre Anwendung beendet wird, geben Sie Ihre Kopie des [**IBackgroundCopyManager-Schnittstellenzeigers**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) frei, wie im folgenden Beispiel gezeigt.


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

[Aufrufen von BITS aus .NET und C#](/windows/desktop/Bits/bits-dot-net) für BITS
</dt> </dl>

 

 