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
# <a name="isolating-components"></a>Isolieren von Komponenten

Ordnungsgemäß erstellte Komponenten machen weder die Umgebung der Host Anwendung noch auch Aktivierungs Kontexte aus. Gut erstellte Komponenten führen eine eigene Kontext Verwaltung aus, anstatt sich auf die Umgebung der Host Anwendung zu verlassen.

Der Autor der gehosteten Komponente hat die beste Position, um genau zu wissen, welche anderen Assemblys für die Komponente erforderlich sind. Die Verwendung der Host Anwendung, um die richtige Umgebung für die gehostete Komponente bereitzustellen, ist eine wahrscheinliche Fehlerquelle. Erstellen Sie stattdessen ein Manifest für die gehostete Komponente, das alle Abhängigkeiten angibt, und kompilieren Sie dann mit aktivierter Isolations Unterstützung \_ \_ . Dadurch wird sichergestellt, dass externe Aufrufe von Ihrer Komponente isoliert sind und die richtigen Versionen verwenden. Da der Aktivierungs Kontext, den Isolations \_ \_ fähig ist, pro-dll verwendet, ist es sicher, in mehreren DLLs zu verwenden, die jeweils über ein eigenes Manifest verfügen, das Abhängigkeiten aufruft.

Wenn die Kompilierung mit aktivierter Isolations Funktion nicht möglich ist \_ \_ , verwenden Sie eine Lösung wie die unter [Verwenden von Rückrufen von gehosteten Komponenten](using-callbacks-from-hosted-components.md).

Sie sollten ihren eigenen Aktivierungs Kontext in allen Einstiegspunkten aktivieren, die von der Hostinganwendung aufgerufen werden können, um sicherzustellen, dass die gehostete Komponente vollständig mit dem richtigen Aktivierungs Kontext ausgeführt wird. Sie können ein C++ Helper-Objekt verwenden, um das Ändern aller entrypunkte zu vereinfachen. Beispielsweise können Sie eine C++-Klasse wie die folgende verwenden:


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



Dies kann dann in der Komponente verwendet werden, wobei eine globale Variable zum Speichern des Aktivierungs Kontexts verwendet wird, der für jeden Einstiegspunkt aktiviert werden soll. Auf diese Weise können Sie die Komponente von ihrer Hostinganwendung isolieren.


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



 

 



