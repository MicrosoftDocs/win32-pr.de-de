---
description: Aktivierungs Kontexte sind Objekte mit Verweis Zählung. Die Anwendung muss über einen Verweis auf einen Aktivierungs Kontext verfügen, damit Sie verwendet werden kann.
ms.assetid: 2dc8ffc5-0a65-4227-b93a-30c3cf0d3c2d
title: Aktivierungs Kontexte der Verweis Zählung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff00afa0dd3a347e14ff9723c06d54af4520ce4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350072"
---
# <a name="reference-counting-activation-contexts"></a>Aktivierungs Kontexte der Verweis Zählung

Aktivierungs Kontexte sind Objekte mit Verweis Zählung. Die Anwendung muss über einen Verweis auf einen Aktivierungs Kontext verfügen, damit Sie verwendet werden kann. Die Funktionen der Aktivierungs Kontext-API, die einen Aktivierungs Kontext annehmen, können eine eigene Verweis Zählung ausführen. Beispielsweise wird [**activateactctx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) vergrößert, und [**deactivateactctx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) verringert den Verweis Zähler. Wenn Ihre Anwendung jedoch einen Aktivierungs Kontext übergibt, ohne diese Funktionen zu verwenden, sollte die Anwendung eine eigene Methode zum zählen von verweisen bereitstellen.

Wenn eine Anwendung " [**kreateactctx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa)" aufruft, hat das zurückgegebene Handle einen Verweis Zähler von 1. Nachdem die Anwendung mit dem Aktivierungs Kontext abgeschlossen wurde, sollte das Handle freigegeben und der Verweis Zähler durch Aufrufen von [**releaseactctx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx)gesenkt werden. Versuchen Sie nicht, [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree)oder andere Speicherverwaltungsfunktionen auf dem Aktivierungs Kontext Handle zu verwenden.

Das folgende Beispiel zeigt eine Methode zum Behandeln der Verweis Zählung über die Lebensdauer eines Aktivierungs Kontexts. Die Funktion Funct erstellt einen Aktivierungs Kontext, der an das Objekt Ziel weitergeleitet wird, das den Verweis Zähler auf 2 erhöht. "Funct" gibt dann seinen Verweis auf den Aktivierungs kontextfrei und verringert den Verweis Zähler auf 1. Das Ziel ist dann in der Besitz Freigabe seines eigenen Verweises, wenn setactctx erneut aufgerufen wird oder wenn das Objekt zerstört wird.


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



 

 
