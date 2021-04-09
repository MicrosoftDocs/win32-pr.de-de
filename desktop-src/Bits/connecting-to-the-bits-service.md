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
# <a name="connecting-to-the-bits-service"></a><span data-ttu-id="2fb8d-103">Herstellen einer Verbindung mit dem BITS-Dienst</span><span class="sxs-lookup"><span data-stu-id="2fb8d-103">Connecting to the BITS Service</span></span>

<span data-ttu-id="2fb8d-104">Zum Herstellen einer Verbindung mit dem Bits-Systemdienst erstellen Sie eine Instanz des backgroundcopymanager-Objekts, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2fb8d-104">To connect to the BITS system service, create an instance of the BackgroundCopyManager object as shown in the following example.</span></span> <span data-ttu-id="2fb8d-105">Der Bits-Systemdienst ist der Windows-Systemdienst, der auf dem Client Computer ausgeführt wird, der die Hintergrund Übertragungsfunktion implementiert.</span><span class="sxs-lookup"><span data-stu-id="2fb8d-105">The BITS system service is the Windows system service running on the client computer that implements the background transfer capability.</span></span>


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



<span data-ttu-id="2fb8d-106">Um auf eine bestimmte Version von Bits zu testen, verwenden Sie einen symbolischen Klassen Bezeichner für backgroundcopymanager, der auf der Version basiert, die Sie überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="2fb8d-106">To test for a specific version of BITS, use a symbolic class identifier for the BackgroundCopyManager based on the version you want to check.</span></span> <span data-ttu-id="2fb8d-107">Wenn Sie z. b. auf Bits 10,2 testen möchten, verwenden Sie CLSID \_ BackgroundCopyManager10 \_ 2.</span><span class="sxs-lookup"><span data-stu-id="2fb8d-107">For example, to test for BITS 10.2, use CLSID\_BackgroundCopyManager10\_2.</span></span>

<span data-ttu-id="2fb8d-108">Im folgenden Beispiel wird gezeigt, wie Sie einen der symbolischen Klassen Bezeichner verwenden.</span><span class="sxs-lookup"><span data-stu-id="2fb8d-108">The following example shows how to use one of the symbolic class identifiers.</span></span>


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



<span data-ttu-id="2fb8d-109">Verwenden Sie die Methoden der [**ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) -Schnittstelle, um [Übertragungs Aufträge zu erstellen](creating-a-job.md), Aufträge in der Warteschlange [aufzuzählen](enumerating-jobs-in-the-transfer-queue.md) und [Aufträge abzurufen](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span><span class="sxs-lookup"><span data-stu-id="2fb8d-109">Use the methods of the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface to [create transfer jobs](creating-a-job.md), [enumerate jobs](enumerating-jobs-in-the-transfer-queue.md) in the queue, and [retrieve jobs](/windows/desktop/api/Bits/nf-bits-ibackgroundcopymanager-getjob).</span></span>



<span data-ttu-id="2fb8d-110">Bits erfordert, dass die Schnittstellen Proxys des Clients entweder den Identitätswechsel oder die Identitätswechsel Ebene des Identitäts Wechsels verwenden.</span><span class="sxs-lookup"><span data-stu-id="2fb8d-110">BITS requires that the client's interface proxies use either the IDENTIFY or IMPERSONATE level of impersonation.</span></span> <span data-ttu-id="2fb8d-111">Wenn die Anwendung nicht [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)aufruft, verwendet com standardmäßig die Identifizierung.</span><span class="sxs-lookup"><span data-stu-id="2fb8d-111">If the application does not call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), COM uses IDENTIFY by default.</span></span> <span data-ttu-id="2fb8d-112">Bits schlägt mit E \_ AccessDenied fehl, wenn die korrekte Identitätswechsel Ebene nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2fb8d-112">BITS fails with E\_ACCESSDENIED if the correct impersonation level is not set.</span></span> <span data-ttu-id="2fb8d-113">Wenn Sie eine Bibliothek bereitstellen, die die Bits-Schnittstellen ausführt, und eine Anwendung, die Ihre Bibliothek aufruft, die Identitätswechsel Ebene unter Identifizieren festlegt, müssen Sie [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) aufrufen, um die korrekte Identitätswechsel Ebene für jede von Ihnen aufgerufenen Bits-Schnittstelle festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2fb8d-113">If you provide a library that exercises the BITS interfaces, and an application that calls your library sets the impersonation level below IDENTIFY, then you will need to call [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) to set the correct impersonation level for each BITS interface that you call.</span></span>

<span data-ttu-id="2fb8d-114">Bevor die Anwendung beendet wird, geben Sie Ihre Kopie des [**ibackgroundcopymanager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) -Schnittstellen Zeigers frei, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2fb8d-114">Before your application exits, release your copy of the [**IBackgroundCopyManager**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopymanager) interface pointer, as shown in the following example.</span></span>


```C++
if (g_pbcm)
{
  g_pbcm->Release();
  g_pbcm = NULL;
}
CoUninitialize();
```



## <a name="related-topics"></a><span data-ttu-id="2fb8d-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2fb8d-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2fb8d-116">[Aufrufen von Bits aus .net und c#](/windows/desktop/Bits/bits-dot-net) für Bits</span><span class="sxs-lookup"><span data-stu-id="2fb8d-116">[Calling into BITS from .NET and C#](/windows/desktop/Bits/bits-dot-net) for BITS</span></span>
</dt> </dl>

 

 