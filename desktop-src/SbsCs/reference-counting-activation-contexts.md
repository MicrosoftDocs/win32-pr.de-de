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
# <a name="reference-counting-activation-contexts"></a><span data-ttu-id="31cfd-104">Aktivierungs Kontexte der Verweis Zählung</span><span class="sxs-lookup"><span data-stu-id="31cfd-104">Reference Counting Activation Contexts</span></span>

<span data-ttu-id="31cfd-105">Aktivierungs Kontexte sind Objekte mit Verweis Zählung.</span><span class="sxs-lookup"><span data-stu-id="31cfd-105">Activation contexts are reference-counted objects.</span></span> <span data-ttu-id="31cfd-106">Die Anwendung muss über einen Verweis auf einen Aktivierungs Kontext verfügen, damit Sie verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="31cfd-106">Your application must have a reference on an activation context in order to use it.</span></span> <span data-ttu-id="31cfd-107">Die Funktionen der Aktivierungs Kontext-API, die einen Aktivierungs Kontext annehmen, können eine eigene Verweis Zählung ausführen.</span><span class="sxs-lookup"><span data-stu-id="31cfd-107">The functions of the Activation Context API that take an activation context can perform their own reference counting.</span></span> <span data-ttu-id="31cfd-108">Beispielsweise wird [**activateactctx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) vergrößert, und [**deactivateactctx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) verringert den Verweis Zähler.</span><span class="sxs-lookup"><span data-stu-id="31cfd-108">For example, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) increases and [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx) decreases the reference count.</span></span> <span data-ttu-id="31cfd-109">Wenn Ihre Anwendung jedoch einen Aktivierungs Kontext übergibt, ohne diese Funktionen zu verwenden, sollte die Anwendung eine eigene Methode zum zählen von verweisen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="31cfd-109">If however your application passes an activation context without using these functions, the application should provide its own method of reference counting.</span></span>

<span data-ttu-id="31cfd-110">Wenn eine Anwendung " [**kreateactctx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa)" aufruft, hat das zurückgegebene Handle einen Verweis Zähler von 1.</span><span class="sxs-lookup"><span data-stu-id="31cfd-110">When an application calls [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa), the handle returned will have a reference count of one.</span></span> <span data-ttu-id="31cfd-111">Nachdem die Anwendung mit dem Aktivierungs Kontext abgeschlossen wurde, sollte das Handle freigegeben und der Verweis Zähler durch Aufrufen von [**releaseactctx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx)gesenkt werden.</span><span class="sxs-lookup"><span data-stu-id="31cfd-111">After the application finishes with the activation context, the handle should be released and the reference count decreased by calling [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx).</span></span> <span data-ttu-id="31cfd-112">Versuchen Sie nicht, [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree)oder andere Speicherverwaltungsfunktionen auf dem Aktivierungs Kontext Handle zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="31cfd-112">Do not attempt to use [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree), [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree), or any other memory-management functions on the activation context handle.</span></span>

<span data-ttu-id="31cfd-113">Das folgende Beispiel zeigt eine Methode zum Behandeln der Verweis Zählung über die Lebensdauer eines Aktivierungs Kontexts.</span><span class="sxs-lookup"><span data-stu-id="31cfd-113">The following example shows a method for handling reference counting over the lifetime of an activation context.</span></span> <span data-ttu-id="31cfd-114">Die Funktion Funct erstellt einen Aktivierungs Kontext, der an das Objekt Ziel weitergeleitet wird, das den Verweis Zähler auf 2 erhöht.</span><span class="sxs-lookup"><span data-stu-id="31cfd-114">The function Funct creates an activation context, which it then passes to the object Target, which increments the reference count to 2.</span></span> <span data-ttu-id="31cfd-115">"Funct" gibt dann seinen Verweis auf den Aktivierungs kontextfrei und verringert den Verweis Zähler auf 1.</span><span class="sxs-lookup"><span data-stu-id="31cfd-115">Funct then releases its reference on the activation context and decreases the reference count back to 1.</span></span> <span data-ttu-id="31cfd-116">Das Ziel ist dann in der Besitz Freigabe seines eigenen Verweises, wenn setactctx erneut aufgerufen wird oder wenn das Objekt zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="31cfd-116">Target then owns releasing its own reference when SetActCtx is called again or when the object is destroyed.</span></span>


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



 

 
