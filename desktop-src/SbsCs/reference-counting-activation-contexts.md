---
description: Aktivierungskontexte sind Objekte mit Verweiszählung. Ihre Anwendung muss über einen Verweis auf einen Aktivierungskontext verfügen, um sie verwenden zu können.
ms.assetid: 2dc8ffc5-0a65-4227-b93a-30c3cf0d3c2d
title: Aktivierungskontexte zur Verweiszählung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62f7806a452dc8b98f824069be0cd584c39f45ad9807a97a11f6f3d7c4929f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141933"
---
# <a name="reference-counting-activation-contexts"></a>Aktivierungskontexte zur Verweiszählung

Aktivierungskontexte sind Objekte mit Verweiszählung. Ihre Anwendung muss über einen Verweis auf einen Aktivierungskontext verfügen, um sie verwenden zu können. Die Funktionen der Aktivierungskontext-API, die einen Aktivierungskontext verwenden, können ihre eigene Verweiszählung durchführen. Beispielsweise erhöht [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) und [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) die Verweisanzahl. Wenn Ihre Anwendung jedoch einen Aktivierungskontext übergibt, ohne diese Funktionen zu verwenden, sollte die Anwendung eine eigene Methode zur Verweiszählung bereitstellen.

Wenn eine Anwendung [**CreateActCtx aufruft,**](/windows/desktop/api/Winbase/nf-winbase-createactctxa)hat das zurückgegebene Handle den Verweiszähler 1. Nachdem die Anwendung mit dem Aktivierungskontext abgeschlossen wurde, sollte das Handle freigegeben und die Verweisanzahl verringert werden, indem [**ReleaseActCtx aufruft.**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx) Versuchen Sie nicht, [**LocalFree,**](/windows/desktop/api/winbase/nf-winbase-localfree) [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree)oder andere Speicherverwaltungsfunktionen für das Aktivierungskontexthand handle zu verwenden.

Das folgende Beispiel zeigt eine Methode zum Behandeln der Verweiszählung über die Lebensdauer eines Aktivierungskontexts. Die Funktion Funct erstellt einen Aktivierungskontext, der dann an das Objekt Target übergeben wird, wodurch die Verweisanzahl auf 2 erhöht wird. Funct gibt dann seinen Verweis auf den Aktivierungskontext frei und verringert die Verweisanzahl wieder auf 1. Das Ziel besitzt dann die Freigabe seines eigenen Verweises, wenn SetActCtx erneut aufgerufen wird oder wenn das Objekt zerstört wird.


```C++
#include <windows.h>

class CMyObject 
{
private:
    HANDLE m_hActCtx;
public:
    CMyObject() : m_hActCtx(INVALID_HANDLE_VALUE) { }
    ~CMyObject() 
    { 
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            ReleaseActCtx(m_hActCtx);
            m_hActCtx = INVALID_HANDLE_VALUE;
        }
    }
    void SetActCtx(HANDLE hActCtx) 
    {
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            ReleaseActCtx(m_hActCtx);
        }
        m_hActCtx = hActCtx;
        if (m_hActCtx != INVALID_HANDLE_VALUE) 
        {
            AddRefActCtx(m_hActCtx);
        }
    }
    void DoWorkWithActCtx();
};

void Funct(CMyObject &Target) 
{
    HANDLE hActCtx;
    ACTCTX actctx = { sizeof(ACTCTX) };
    hActCtx = CreateActCtx(&actctx);  //create activation context  
    Target.SetActCtx(hActCtx);    //pass activation context to Target; 
    // actctx now has 1 more reference
    ReleaseActCtx(hActCtx);
}
```



 

 
