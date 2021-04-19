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
# <a name="calling-outside-an-assembly"></a>Aufrufen außerhalb einer Assembly

Gehostete Komponenten sollten sicherstellen, dass der richtige Aktivierungs Kontext aktiv ist, wenn der Aufruf außerhalb der Komponente erfolgt. Aufrufe von externen Code, der durch Aufrufen von [**createactctx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa) und [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)gefunden wurde, sollten mit demselben Kontext aufgerufen werden, der zum Suchen verwendet wurde. Aufrufe von Code, der außerhalb von Aktivierungs Kontexten gefunden wurde, oder Rückrufe in der Host Anwendung sollten mit dem Standard Aktivierungs Kontext der Anwendung aufgerufen werden.

Die Kompilierung mit aktivierter Isolations Funktion ist \_ \_ möglicherweise nützlich, wenn außerhalb von gehosteten Komponenten aufgerufen wird. Dies bedeutet jedoch, dass nur Aufrufe von Windows-APIs in den Aktivierungs Kontext der Komponente isoliert sind. Dies ist in den meisten Fällen ausreichend, da Aufrufe von Funktionen von Drittanbietern keinen Kontext aktiviert haben, bevor Sie aufgerufen werden. Die Kompilierung mit aktivierter Isolations Funktion \_ \_ ist nicht hilfreich, wenn die Komponente mehrere Aktivierungs Kontexte mit verschiedenen Plattform-APIs verwendet.

Um dies zu implementieren, verwenden Sie einen Aktivierungs Kontext Aktivator, wie in dem Beispiel unter [Isolieren von Komponenten](isolating-components.md)dargestellt. Hier ist "Externals. Manifest" der Satz von Abhängigkeiten außerhalb derjenigen, mit denen die Komponente erstellt wurde. Sie enthält möglicherweise eine erweiterbare Liste von Komponenten, die während der Laufzeit geladen und verwendet werden sollen. Internalcontext. Manifest enthält den Satz von Abhängigkeiten, die von der Komponente während ihrer Lebensdauer sicher verwendet werden, und der in allen entryPoints von außen festgelegt werden sollte. Beachten Sie, dass dieser interne Kontext in allen Einstiegspunkten aktiviert ist, während der Kontext Aktivator mit der C++-Bereichs Definition verwendet wird, sodass der richtige Kontext festgelegt wird, wenn der von dieser Komponente verwendete externe Code aufgerufen wird.

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

 

 
