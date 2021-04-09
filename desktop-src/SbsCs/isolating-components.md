---
description: Ordnungsgemäß erstellte Komponenten machen weder die Umgebung der Host Anwendung noch auch Aktivierungs Kontexte aus.
ms.assetid: cc3e21fd-5fd3-40b6-9218-cb5f47be3567
title: Isolieren von Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e201375f50324209380a4ecef5fa762ae70e56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862339"
---
# <a name="isolating-components"></a><span data-ttu-id="a3677-103">Isolieren von Komponenten</span><span class="sxs-lookup"><span data-stu-id="a3677-103">Isolating Components</span></span>

<span data-ttu-id="a3677-104">Ordnungsgemäß erstellte Komponenten machen weder die Umgebung der Host Anwendung noch auch Aktivierungs Kontexte aus.</span><span class="sxs-lookup"><span data-stu-id="a3677-104">Well-authored components do not perturb the environment of the hosting application, nor do they leak activation contexts.</span></span> <span data-ttu-id="a3677-105">Gut erstellte Komponenten führen eine eigene Kontext Verwaltung aus, anstatt sich auf die Umgebung der Host Anwendung zu verlassen.</span><span class="sxs-lookup"><span data-stu-id="a3677-105">Well-authored components perform their own context management rather than relying on the hosting application's environment.</span></span>

<span data-ttu-id="a3677-106">Der Autor der gehosteten Komponente hat die beste Position, um genau zu wissen, welche anderen Assemblys für die Komponente erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a3677-106">The author of the hosted component is in the best position to know exactly which other assemblies the component requires.</span></span> <span data-ttu-id="a3677-107">Die Verwendung der Host Anwendung, um die richtige Umgebung für die gehostete Komponente bereitzustellen, ist eine wahrscheinliche Fehlerquelle.</span><span class="sxs-lookup"><span data-stu-id="a3677-107">Relying on the host application to provide the correct environment for your hosted component is a probable source of errors.</span></span> <span data-ttu-id="a3677-108">Erstellen Sie stattdessen ein Manifest für die gehostete Komponente, das alle Abhängigkeiten angibt, und kompilieren Sie dann mit aktivierter Isolations Unterstützung \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a3677-108">Instead, create a manifest for your hosted component that specifies all its dependencies, and then compile using ISOLATION\_AWARE\_ENABLED.</span></span> <span data-ttu-id="a3677-109">Dadurch wird sichergestellt, dass externe Aufrufe von Ihrer Komponente isoliert sind und die richtigen Versionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="a3677-109">This ensures that outside calls made by your component are isolated and use the correct versions.</span></span> <span data-ttu-id="a3677-110">Da der Aktivierungs Kontext, den Isolations \_ \_ fähig ist, pro-dll verwendet, ist es sicher, in mehreren DLLs zu verwenden, die jeweils über ein eigenes Manifest verfügen, das Abhängigkeiten aufruft.</span><span class="sxs-lookup"><span data-stu-id="a3677-110">Because the activation context that ISOLATION\_AWARE\_ENABLED uses is per-DLL, it is safe to use in multiple DLLs, each with their own manifest calling out dependencies.</span></span>

<span data-ttu-id="a3677-111">Wenn die Kompilierung mit aktivierter Isolations Funktion nicht möglich ist \_ \_ , verwenden Sie eine Lösung wie die unter [Verwenden von Rückrufen von gehosteten Komponenten](using-callbacks-from-hosted-components.md).</span><span class="sxs-lookup"><span data-stu-id="a3677-111">If it is not possible to compile with ISOLATION\_AWARE\_ENABLED, then use a solution like the one presented in [Using Callbacks From Hosted Components](using-callbacks-from-hosted-components.md).</span></span>

<span data-ttu-id="a3677-112">Sie sollten ihren eigenen Aktivierungs Kontext in allen Einstiegspunkten aktivieren, die von der Hostinganwendung aufgerufen werden können, um sicherzustellen, dass die gehostete Komponente vollständig mit dem richtigen Aktivierungs Kontext ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3677-112">You should activate your own activation context in all the entry points that the hosting application can call to ensure that your hosted component runs entirely with the correct activation context.</span></span> <span data-ttu-id="a3677-113">Sie können ein C++ Helper-Objekt verwenden, um das Ändern aller entrypunkte zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="a3677-113">You can use a C++ helper object to facilitate changing all the entrypoints.</span></span> <span data-ttu-id="a3677-114">Beispielsweise können Sie eine C++-Klasse wie die folgende verwenden:</span><span class="sxs-lookup"><span data-stu-id="a3677-114">For example, you could use a C++ class such as the following:</span></span>


```C++
#include <windows.h>

class CActivationContext 
{
    HANDLE m_hActivationContext;

public:
    CActivationContext() : m_hActivationContext(INVALID_HANDLE_VALUE) 
    {
    }

    VOID Set(HANDLE hActCtx) 
    {
        if (hActCtx != INVALID_HANDLE_VALUE)
            AddRefActCtx(hActCtx);

        if (m_hActivationContext != INVALID_HANDLE_VALUE)
            ReleaseActCtx(m_hActivationContext);
        m_hActivationContext = hActCtx;
    }

    ~CActivationContext() 
    {
        if (m_hActivationContext != INVALID_HANDLE_VALUE)
            ReleaseActCtx(m_hActivationContext);
    }

    BOOL Activate(ULONG_PTR &ulpCookie) 
    {
        return ActivateActCtx(m_hActivationContext, &ulpCookie);
    }

    BOOL Deactivate(ULONG_PTR ulpCookie) 
    {
        return DeactivateActCtx(0, ulpCookie);
    }
};

class CActCtxActivator 
{
    CActivationContext &m_ActCtx;
    ULONG_PTR m_Cookie;
    bool m_fActivated;

public:
    CActCtxActivator(CActivationContext& src, bool fActivate = true) 
        : m_ActCtx(src), m_Cookie(0), m_fActivated(false) 
    {
        if (fActivate) {
            if (src.Activate(m_Cookie))
                m_fActivated = true;
        }
    }

    ~CActCtxActivator() 
    {
        if (m_fActivated) {
            m_ActCtx.Deactivate(m_Cookie);
            m_fActivated = false;
        }
    }
};

```



<span data-ttu-id="a3677-115">Dies kann dann in der Komponente verwendet werden, wobei eine globale Variable zum Speichern des Aktivierungs Kontexts verwendet wird, der für jeden Einstiegspunkt aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a3677-115">This can then be used in your component, using a global variable to store the activation context that should be activated on each entry point.</span></span> <span data-ttu-id="a3677-116">Auf diese Weise können Sie die Komponente von ihrer Hostinganwendung isolieren.</span><span class="sxs-lookup"><span data-stu-id="a3677-116">In this way, you can isolate your component from your hosting application.</span></span>


```C++
CActivationContext s_GlobalContext;

void MyExportedEntrypoint(void) 
{
    CActCtxActivator ScopedContext(s_GlobalContext);
    // Do whatever work here
    // Destructor automatically deactivates the context
}

void MyInitializerFunction() 
{
    HANDLE hActCtx;
    ACTCTX actctx = {sizeof(actctx)};
    hActCtx = CreateActCtx(&actctx);
    s_GlobalContext.Set(hActCtx);
    ReleaseActCtx(hActCtx);
    // The static destructor for s_GlobalContext destroys the
    // activation context on component unload.
}
```



 

 



