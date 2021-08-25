---
description: Gut verfasste Komponenten machen weder die Umgebung der Hostinganwendung aus noch geben sie Aktivierungskontexte frei.
ms.assetid: cc3e21fd-5fd3-40b6-9218-cb5f47be3567
title: Isolieren von Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411d5e90114b7509dff2e5e48a4770841774df52fce804895155d2bd4d43e514
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885190"
---
# <a name="isolating-components"></a>Isolieren von Komponenten

Gut verfasste Komponenten machen weder die Umgebung der Hostinganwendung aus noch geben sie Aktivierungskontexte frei. Gut verfasste Komponenten führen ihre eigene Kontextverwaltung durch, anstatt sich auf die Umgebung der Hostinganwendung zu verlassen.

Der Autor der gehosteten Komponente ist am besten in der Lage, genau zu wissen, welche anderen Assemblys die Komponente benötigt. Die Verwendung der Hostanwendung zur Bereitstellung der richtigen Umgebung für Ihre gehostete Komponente ist eine wahrscheinliche Fehlerquelle. Erstellen Sie stattdessen ein Manifest für Ihre gehostete Komponente, das alle Abhängigkeiten angibt, und kompilieren Sie dann mit ISOLATION \_ AWARE \_ ENABLED. Dadurch wird sichergestellt, dass externe Aufrufe Ihrer Komponente isoliert sind und die richtigen Versionen verwenden. Da der Aktivierungskontext, den ISOLATION AWARE ENABLED verwendet, pro DLL ist, ist es sicher, in mehreren DLLs zu verwenden, die jeweils über ein eigenes Manifest verfügen, das \_ \_ Abhängigkeiten aufruft.

Wenn es nicht möglich ist, mit ISOLATION AWARE ENABLED zu kompilieren, verwenden Sie eine Lösung wie die unter Using Callbacks From Hosted Components (Verwenden von Rückrufen \_ \_ aus [gehosteten Komponenten).](using-callbacks-from-hosted-components.md)

Sie sollten ihren eigenen Aktivierungskontext in allen Einstiegspunkten aktivieren, die die Hostanwendung aufrufen kann, um sicherzustellen, dass Ihre gehostete Komponente vollständig mit dem richtigen Aktivierungskontext ausgeführt wird. Sie können ein C++-Hilfsobjekt verwenden, um das Ändern aller Einstiegpunkte zu vereinfachen. Beispielsweise können Sie eine C++-Klasse wie die folgende verwenden:


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



Dies kann dann in Ihrer Komponente verwendet werden, indem eine globale Variable verwendet wird, um den Aktivierungskontext zu speichern, der an jedem Einstiegspunkt aktiviert werden soll. Auf diese Weise können Sie Ihre Komponente von Ihrer Hostinganwendung isolieren.


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



 

 



