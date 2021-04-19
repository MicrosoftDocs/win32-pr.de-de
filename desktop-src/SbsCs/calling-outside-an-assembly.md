---
description: Aufrufen außerhalb einer Assembly
ms.assetid: 7a59f707-fb89-4899-891f-4cd556b62b26
title: Aufrufen außerhalb einer Assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed60536c3daa62957929dd1d3f1a850fd551ae9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356227"
---
# <a name="calling-outside-an-assembly"></a><span data-ttu-id="75bde-103">Aufrufen außerhalb einer Assembly</span><span class="sxs-lookup"><span data-stu-id="75bde-103">Calling Outside An Assembly</span></span>

<span data-ttu-id="75bde-104">Gehostete Komponenten sollten sicherstellen, dass der richtige Aktivierungs Kontext aktiv ist, wenn der Aufruf außerhalb der Komponente erfolgt.</span><span class="sxs-lookup"><span data-stu-id="75bde-104">Hosted components should ensure that the correct activation context is active when calling outside the component.</span></span> <span data-ttu-id="75bde-105">Aufrufe von externen Code, der durch Aufrufen von [**createactctx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) und [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)gefunden wurde, sollten mit demselben Kontext aufgerufen werden, der zum Suchen verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="75bde-105">Calls into outside code that was found by calling [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) and then [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), should be called with the same context that was used to find it.</span></span> <span data-ttu-id="75bde-106">Aufrufe von Code, der außerhalb von Aktivierungs Kontexten gefunden wurde, oder Rückrufe in der Host Anwendung sollten mit dem Standard Aktivierungs Kontext der Anwendung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="75bde-106">Calls into code that was found outside of activation contexts, or calls back into the hosting application should be called with the application default activation context.</span></span>

<span data-ttu-id="75bde-107">Die Kompilierung mit aktivierter Isolations Funktion ist \_ \_ möglicherweise nützlich, wenn außerhalb von gehosteten Komponenten aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="75bde-107">Compiling with ISOLATION\_AWARE\_ENABLED defined may be useful when calling outside of hosted components.</span></span> <span data-ttu-id="75bde-108">Dies bedeutet jedoch, dass nur Aufrufe von Windows-APIs in den Aktivierungs Kontext der Komponente isoliert sind.</span><span class="sxs-lookup"><span data-stu-id="75bde-108">However this means that only calls to Windows APIs are isolated to the component's activation context.</span></span> <span data-ttu-id="75bde-109">Dies ist in den meisten Fällen ausreichend, da Aufrufe von Funktionen von Drittanbietern keinen Kontext aktiviert haben, bevor Sie aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="75bde-109">This is sufficient for most cases because calls to third-party functions do not have a context activated before being called.</span></span> <span data-ttu-id="75bde-110">Die Kompilierung mit aktivierter Isolations Funktion \_ \_ ist nicht hilfreich, wenn die Komponente mehrere Aktivierungs Kontexte mit verschiedenen Plattform-APIs verwendet.</span><span class="sxs-lookup"><span data-stu-id="75bde-110">Compiling with ISOLATION\_AWARE\_ENABLED defined does not help if your component uses several activation contexts with various platform APIs.</span></span>

<span data-ttu-id="75bde-111">Um dies zu implementieren, verwenden Sie einen Aktivierungs Kontext Aktivator, wie in dem Beispiel unter [Isolieren von Komponenten](isolating-components.md)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="75bde-111">To implement this, use an activation context activator like the example presented in [Isolating Components](isolating-components.md).</span></span> <span data-ttu-id="75bde-112">Hier ist "Externals. Manifest" der Satz von Abhängigkeiten außerhalb derjenigen, mit denen die Komponente erstellt wurde. Sie enthält möglicherweise eine erweiterbare Liste von Komponenten, die während der Laufzeit geladen und verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="75bde-112">Here externals.manifest is the set of dependencies outside those the component was built with; perhaps it contains some extendable list of components that are to be loaded and used during runtime.</span></span> <span data-ttu-id="75bde-113">Internalcontext. Manifest enthält den Satz von Abhängigkeiten, die von der Komponente während ihrer Lebensdauer sicher verwendet werden, und der in allen entryPoints von außen festgelegt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="75bde-113">The internalcontext.manifest contains the set of dependencies that the component is sure to use during its lifetime, and which should be set in all entrypoints from the outside.</span></span> <span data-ttu-id="75bde-114">Beachten Sie, dass dieser interne Kontext in allen Einstiegspunkten aktiviert ist, während der Kontext Aktivator mit der C++-Bereichs Definition verwendet wird, sodass der richtige Kontext festgelegt wird, wenn der von dieser Komponente verwendete externe Code aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="75bde-114">Notice that this internal context is activated in all entrypoints, while the context activator is used with C++ scoping so that the proper context is set when calling out to the various outside code that this component uses.</span></span>

``` syntax
CActivationContext s_InternalContext;
CActivationContext s_OutboundContext;
CActivationContext s_ExternalContext;

void MyInitializeFunction() 
{
    HANDLE hActCtx;
    ACTCTX actctx = {sizeof(actctx)};

    s_OutboundContext.Set(NULL);

    actctx.lpSource = TEXT("internalcontext.manifest");
    hActCtx = CreateActCtx(&actctx);
    s_InternalActCtx.Set(hActCtx);
    ReleaseActCtx(hActCtx);

    actctx.lpSource = TEXT("externals.manifest");
    hActCtx = CreateActCtx(&actctx);
    s_ExternalContext.Set(hActCtx);
    ReleaseActCtx(hActCtx);
}

void foo() 
{
    // Some code that makes a few calls
    {
        CActCtxActivator CallUnknown(s_OutboundContext);
        pfnUnknownImplementor(...);
    }
    {
        CActCtxActivator CallDependency(s_ExternalContext);
        KnownExternalDependencyPtr->Call();
    }
}

void WINAPI MyEntrypoint() 
{
    CActCtxActivator ContextFirewall(s_InternalContext);
    // Do some work here
    foo();
    // Some more work here
}
```

 

 
