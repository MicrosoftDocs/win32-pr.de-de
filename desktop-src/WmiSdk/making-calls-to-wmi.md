---
description: Anbieter können von WMI implementierte Methoden in ihren Methoden Implementierungen abrufen.
ms.assetid: 5bfd9d9b-ffe5-4def-a97d-85c4c01223f0
ms.tgt_platform: multiple
title: Aufrufen von WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 534e478336cdd9675e382ef9b089f2d7bc595b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042305"
---
# <a name="making-calls-to-wmi"></a><span data-ttu-id="55894-103">Aufrufen von WMI</span><span class="sxs-lookup"><span data-stu-id="55894-103">Making Calls to WMI</span></span>

<span data-ttu-id="55894-104">Anbieter können von WMI implementierte Methoden in ihren Methoden Implementierungen abrufen.</span><span class="sxs-lookup"><span data-stu-id="55894-104">Providers can call methods implemented by WMI from within their method implementations.</span></span> <span data-ttu-id="55894-105">Es gibt jedoch besondere Überlegungen, wenn ein Anbieter die WMI-Implementierung einer [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Methode aus einer eigenen Implementierung derselben Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="55894-105">However, there are special considerations when a provider calls the WMI implementation of an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) method from within its own implementation of the same method.</span></span> <span data-ttu-id="55894-106">Diese Überlegungen sind unabhängig davon wichtig, ob der Anbieter die synchrone oder asynchrone Version der Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="55894-106">These considerations are important regardless of whether the provider calls the synchronous or asynchronous version of the method.</span></span>

<span data-ttu-id="55894-107">Jede [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Methode, die ein Anbieter implementieren kann, verfügt über einen *pctX* -Parameter, einen Zeiger auf eine [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Schnittstellen Implementierung.</span><span class="sxs-lookup"><span data-stu-id="55894-107">Each [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) method that a provider can implement has a *pCtx* parameter, a pointer to an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) interface implementation.</span></span> <span data-ttu-id="55894-108">Wenn WMI den Anbieter aufruft, übergibt WMI einen gültigen Zeiger in diesem Parameter.</span><span class="sxs-lookup"><span data-stu-id="55894-108">When WMI calls the provider, WMI passes a valid pointer in this parameter.</span></span> <span data-ttu-id="55894-109">Ein Anbieter muss denselben Zeiger immer bei WMI-aufrufen übergeben, die er während der Wartung von Anforderungen vornimmt.</span><span class="sxs-lookup"><span data-stu-id="55894-109">A provider must always pass this same pointer in any calls to WMI that they make while servicing requests.</span></span> <span data-ttu-id="55894-110">Die angemessene Festlegung von *pctX* kann bewirken, dass WMI eine Endlosschleife startet.</span><span class="sxs-lookup"><span data-stu-id="55894-110">Neglecting to set *pCtx* appropriately can cause WMI to start an infinite loop.</span></span>

<span data-ttu-id="55894-111">Das folgende Codebeispiel zeigt die korrekte Methode zum Aufrufen der WMI-Implementierung von [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) aus einer Implementierung von [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="55894-111">The following code example shows the correct way to call the WMI implementation of [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) from within an implementation of [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>


```C++
STDMETHODIMP CClassProv::GetObjectAsync (BSTR ObjectPath,
    long lFlags, IWbemContext *pCtx,
    IWbemObjectSink *pHandler)
{
  IWbemClassObject *pclObj = NULL;
  IWbemServices* m_pNamespace;
  HRESULT hr = m_pNamespace->GetObject(
      _bstr_t(L"AClass"), 0, pCtx, &pclObj, 
      NULL );
  pclObj->Release();
  return pHandler->SetStatus(0, hr, NULL, NULL);
}
```



<span data-ttu-id="55894-112">Für das C++-Codebeispiel in diesem Thema sind die folgenden Verweise und \# include-Anweisungen erforderlich, um ordnungsgemäß zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="55894-112">The C++ code example in this topic requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="55894-113">Instanzen, Klassen und Eigenschaften Anbieter dürfen keine Aufrufe von WMI ausgeben, die die Änderung von Daten anfordern, während eine Lese Anforderung verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="55894-113">Instance, class, and property providers must not issue any calls to WMI requesting the modification of data while servicing a read request.</span></span> <span data-ttu-id="55894-114">Die einzigen Anbieter, die Ausnahmen für diese Regel sind, sind pushanbieter.</span><span class="sxs-lookup"><span data-stu-id="55894-114">The only providers that are exceptions to this rule are push providers.</span></span> <span data-ttu-id="55894-115">Ein Push-Anbieter ist ein Klassen Anbieter, der Daten im WMI-Repository speichert und von WMI zum Verarbeiten von Anforderungen von Clients abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="55894-115">A push provider is a class provider that stores data in the WMI repository and relies on WMI to handle requests from clients.</span></span> <span data-ttu-id="55894-116">Bei der Verarbeitung einer Lese Anforderung kann ein pushanbieter zwar das WMI-Repository aktualisieren, muss den *lFlags* -Parameter jedoch im entsprechenden [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Befehl auf das **WBEM- \_ Flag " \_ Besitzer \_ Update** " festlegen.</span><span class="sxs-lookup"><span data-stu-id="55894-116">While servicing a read request, a push provider can update the WMI repository, but must set the *lFlags* parameter to **WBEM\_FLAG\_OWNER\_UPDATE** in the appropriate [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) call.</span></span>

<span data-ttu-id="55894-117">Ereignis Anbieter dürfen während der Wartung eines Aufrufes keine Klassenänderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="55894-117">Event providers must not make any class changes while servicing a call.</span></span> <span data-ttu-id="55894-118">Sie können auch keine ereignisbezogenen Aufrufe ausgeben, wie z. b. das Ändern eines Ereignis Filters.</span><span class="sxs-lookup"><span data-stu-id="55894-118">They also cannot issue any event-related calls, such as modifying an event filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55894-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="55894-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55894-120">Entwickeln eines WMI-Anbieters</span><span class="sxs-lookup"><span data-stu-id="55894-120">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="55894-121">Festlegen von namepace-Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="55894-121">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="55894-122">Sichern Ihres Anbieters</span><span class="sxs-lookup"><span data-stu-id="55894-122">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 



