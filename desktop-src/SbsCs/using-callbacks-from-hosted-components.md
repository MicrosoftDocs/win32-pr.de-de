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
# <a name="using-callbacks-from-hosted-components"></a>Verwenden von Rückrufen von gehosteten Komponenten

Durch Rückrufe von gehosteten Komponenten wird das Hosting ermöglicht. Es ist jedoch möglich, dass die von Ihnen gehosteten Komponente einen anderen Aktivierungs Kontext aktiviert hat, den Sie für den Zugriff auf Plug-ins oder eigen Komponenten verwendet. Wenn in diesem Fall die gehostete Komponente einen Aktivierungs Kontext auf dem Stapel verlässt, der auf ein eigenes com-Objekt verweist, kann die hostende Anwendung [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufrufen, um ein Objekt abzurufen, das als eigene Implementierung erwartet wird, und stattdessen das Objekt der gehosteten Komponente empfängt. Um die Vererbung von Aktivierungs Kontexten zu verhindern, sollten gute Hostinganwendungen den eigenen bekannten Aktivierungs Kontext während eines Rückrufs aktivieren.

Sehen Sie sich das folgende Beispiel an, das den Code der Hostinganwendung schützt:

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

Dadurch wird sichergestellt, dass ein richtiger Aktivierungs Kontext festgelegt wird, bevor die Anforderung an eine interne Implementierung von **Funct** übergeben wird. Ihre eigene Implementierung kann die tatsächliche Implementierung Inline aufweisen, aber die vorhergehende Methode sorgt für eine einfachere Interoperabilität, indem nur Delegierte Wrapper erstellt werden. Es wird empfohlen, eine ähnliche Methode zu verwenden, wenn Sie normale (nicht-com-Rückrufe) verfügbar machen.

 

 
