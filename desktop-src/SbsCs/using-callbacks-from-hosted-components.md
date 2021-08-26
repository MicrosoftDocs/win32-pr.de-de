---
description: Rückrufe von gehosteten Komponenten ermöglichen das Hosting. Es ist jedoch möglich, dass die Komponente, die Sie hosten, einen anderen Aktivierungskontext aktiviert hat, den sie für den Zugriff auf Plug-Ins oder eigene Komponenten verwendet.
ms.assetid: 794a2e2f-ba1f-48ad-a435-244fc7936097
title: Verwenden von Rückrufen von gehosteten Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb13e61b83ba52f0f8dd5265b11585e8366c0e8558d45c5738f179d43df2eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884600"
---
# <a name="using-callbacks-from-hosted-components"></a>Verwenden von Rückrufen von gehosteten Komponenten

Rückrufe von gehosteten Komponenten ermöglichen das Hosting. Es ist jedoch möglich, dass die Komponente, die Sie hosten, einen anderen Aktivierungskontext aktiviert hat, den sie für den Zugriff auf Plug-Ins oder eigene Komponenten verwendet. Wenn die gehostete Komponente in diesem Fall einen Aktivierungskontext im Stapel verlässt, der auf ihr eigenes COM-Objekt verweist, kann die Hostanwendung [**Möglicherweise CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufrufen, um ein Objekt zu erhalten, von dem erwartet wird, dass es sich um eine eigene Implementierung handelt, und stattdessen das -Objekt der gehosteten Komponente empfangen. Um diese Vererbung von Aktivierungskontexten zu verhindern, sollten gute Hostinganwendungen zuerst während eines Rückrufs ihren eigenen bekannten Aktivierungskontext aktivieren.

Betrachten Sie das folgende Beispiel, das den Code der Hostanwendung schützt:

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

Dadurch wird sichergestellt, dass ein ordnungsgemäßer Aktivierungskontext festgelegt wird, bevor die Anforderung an eine innere Implementierung von **Funct übergeben wird.** Ihre eigene Implementierung kann die tatsächliche Implementierung inline haben, aber die vorherige Methode stellt eine einfachere Interoperabilität sicher, indem nur delegierte Wrapper erstellt werden. Es wird empfohlen, eine ähnliche Methode zu verwenden, wenn normale Rückrufe (nicht COM) verfügbar sind.

 

 
