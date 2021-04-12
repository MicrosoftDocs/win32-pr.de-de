---
description: Durch Rückrufe von gehosteten Komponenten wird das Hosting ermöglicht. Es ist jedoch möglich, dass die von Ihnen gehosteten Komponente einen anderen Aktivierungs Kontext aktiviert hat, den Sie für den Zugriff auf Plug-ins oder eigen Komponenten verwendet.
ms.assetid: 794a2e2f-ba1f-48ad-a435-244fc7936097
title: Verwenden von Rückrufen von gehosteten Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef302601985bc7e56a296bc8f494e48e18d785e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128813"
---
# <a name="using-callbacks-from-hosted-components"></a><span data-ttu-id="bc241-104">Verwenden von Rückrufen von gehosteten Komponenten</span><span class="sxs-lookup"><span data-stu-id="bc241-104">Using Callbacks From Hosted Components</span></span>

<span data-ttu-id="bc241-105">Durch Rückrufe von gehosteten Komponenten wird das Hosting ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="bc241-105">Callbacks from hosted components are what make hosting possible.</span></span> <span data-ttu-id="bc241-106">Es ist jedoch möglich, dass die von Ihnen gehosteten Komponente einen anderen Aktivierungs Kontext aktiviert hat, den Sie für den Zugriff auf Plug-ins oder eigen Komponenten verwendet.</span><span class="sxs-lookup"><span data-stu-id="bc241-106">However, it is possible that the component you are hosting has activated another activation context that it uses to access plug-ins or components of its own.</span></span> <span data-ttu-id="bc241-107">Wenn in diesem Fall die gehostete Komponente einen Aktivierungs Kontext auf dem Stapel verlässt, der auf ein eigenes com-Objekt verweist, kann die hostende Anwendung [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufrufen, um ein Objekt abzurufen, das als eigene Implementierung erwartet wird, und stattdessen das Objekt der gehosteten Komponente empfängt.</span><span class="sxs-lookup"><span data-stu-id="bc241-107">In this case, if the hosted component leaves an activation context on the stack that refers to its own COM object, the hosting application might call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get an object that it expects to be its own implementation and instead receive the hosted component's object.</span></span> <span data-ttu-id="bc241-108">Um die Vererbung von Aktivierungs Kontexten zu verhindern, sollten gute Hostinganwendungen den eigenen bekannten Aktivierungs Kontext während eines Rückrufs aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bc241-108">To prevent this inheritance of activation contexts, a good hosting applications should activate its own well-known activation context first during a callback.</span></span>

<span data-ttu-id="bc241-109">Sehen Sie sich das folgende Beispiel an, das den Code der Hostinganwendung schützt:</span><span class="sxs-lookup"><span data-stu-id="bc241-109">Consider the following example that protects the hosting application's code:</span></span>

``` syntax
HRESULT STDCALL 
CHostingAppFirewall::ITheInterface::FunctWrapper()
{
    ULONG_PTR ulpCookie;
    HRESULT hRes = E_FAIL;
    if (!ActivateActCtx(this->m_hHostingAppContext, &ulpCookie))
        return HRESULT_FROM_WIN32(GetLastError());
    __try 
        {
        hRes = this->m_ITheInterface->Funct();
    } 
        __finally 
        {
        if (!DeactivateActCtx(0, ulpCookie))
            hRes = HRESULT_FROM_WIN32(GetLastError());
    }
    return hRes;
}
```

<span data-ttu-id="bc241-110">Dadurch wird sichergestellt, dass ein richtiger Aktivierungs Kontext festgelegt wird, bevor die Anforderung an eine interne Implementierung von **Funct** übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="bc241-110">This ensures that a proper activation context is set before passing the request on to some inner implementation of **Funct**.</span></span> <span data-ttu-id="bc241-111">Ihre eigene Implementierung kann die tatsächliche Implementierung Inline aufweisen, aber die vorhergehende Methode sorgt für eine einfachere Interoperabilität, indem nur Delegierte Wrapper erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bc241-111">Your own implementation can have the actual implementation inline, but the preceding method ensures easier interoperability by just creating delegated wrappers.</span></span> <span data-ttu-id="bc241-112">Es wird empfohlen, eine ähnliche Methode zu verwenden, wenn Sie normale (nicht-com-Rückrufe) verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="bc241-112">It is recommended to use a similar method when exposing normal (non-COM) callbacks.</span></span>

 

 
