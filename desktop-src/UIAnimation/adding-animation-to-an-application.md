---
title: Erstellen der Haupt Animations Objekte
description: Um die Windows-Animation in Ihrer Anwendung zu verwenden, besteht der erste Schritt darin, eine kleine Gruppe von Haupt Animations Objekten zu erstellen.
ms.assetid: 4005819e-482c-4052-89f8-b8e457c0c3dc
keywords:
- Animation-Manager-Objekte Windows-Animation, erstellen
- Animation Zeit Geber Objekte Windows-Animation, erstellen
- Übergangs Bibliotheksobjekte Windows-Animation, erstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ccd1cab32e72bf1382469ada52abeecee47b6a1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390787"
---
# <a name="create-the-main-animation-objects"></a><span data-ttu-id="870d0-106">Erstellen der Haupt Animations Objekte</span><span class="sxs-lookup"><span data-stu-id="870d0-106">Create the Main Animation Objects</span></span>

<span data-ttu-id="870d0-107">Um die Windows-Animation in Ihrer Anwendung zu verwenden, besteht der erste Schritt darin, eine kleine Gruppe von Haupt Animations Objekten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="870d0-107">To use Windows Animation in your application, the first step is to create a small set of main animation objects.</span></span>

## <a name="overview"></a><span data-ttu-id="870d0-108">Übersicht</span><span class="sxs-lookup"><span data-stu-id="870d0-108">Overview</span></span>

<span data-ttu-id="870d0-109">Verwenden Sie die [**cokreatanstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion, um den Animations-Manager, den Animations Timer und die Übergangs Bibliotheksobjekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="870d0-109">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create the animation manager, animation timer, and transition library objects.</span></span>

<span data-ttu-id="870d0-110">Diese Objekte werden zum Erstellen und Anzeigen von Animationen benötigt, sodass Sie normalerweise erst freigegeben werden, wenn die Anwendung heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="870d0-110">These objects will be needed to create and display animations, so they usually should not be released until the application is shutting down.</span></span> <span data-ttu-id="870d0-111">Wenn keine Möglichkeit besteht, dass registrierte Rückrufe einen Verweis Durchlauf erstellt haben, reicht das Freigeben der Objekte für eine ordnungsgemäße Bereinigung aus.</span><span class="sxs-lookup"><span data-stu-id="870d0-111">If there is no chance that any registered callbacks could have created a reference cycle, releasing the objects is sufficient for a proper cleanup.</span></span> <span data-ttu-id="870d0-112">Andernfalls kann die Anwendung bereinigt werden, indem die Rückrufe (an der Stelle von **null** ) oder durch Aufrufen der [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) -Methode des Animations-Managers gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="870d0-112">Otherwise, the application can clean up by clearing the callbacks (passing **NULL** in the place of each) or by calling the animation manager's [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) method.</span></span>

## <a name="example-code"></a><span data-ttu-id="870d0-113">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="870d0-113">Example Code</span></span>

<span data-ttu-id="870d0-114">Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" in den Windows-Animations Beispielen. Weitere Informationen finden Sie unter der CMainWindow:: initializeanimation-Methode.</span><span class="sxs-lookup"><span data-stu-id="870d0-114">The following example code is taken from MainWindow.cpp in the Windows Animation samples; see the CMainWindow::InitializeAnimation method.</span></span>


```C++
// Create the animation manager object

HRESULT hr = CoCreateInstance(
    CLSID_UIAnimationManager,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&m_pAnimationManager)
    );

if (SUCCEEDED(hr))
{
    // Create the animation timer object

    hr = CoCreateInstance(
        CLSID_UIAnimationTimer,
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_pAnimationTimer)
        );

    if (SUCCEEDED(hr))
    {
        // Create the transition library object

        hr = CoCreateInstance(
            CLSID_UIAnimationTransitionLibrary,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_PPV_ARGS(&m_pTransitionLibrary)
            );

        ...

    }

    ...

}
```



<span data-ttu-id="870d0-115">Beachten Sie die folgenden Definitionen von "MainWindow. h".</span><span class="sxs-lookup"><span data-stu-id="870d0-115">Note the following definitions from MainWindow.h.</span></span>


```
class CMainWindow
{

    ...

private:

    // Animation components

    IUIAnimationManager *m_pAnimationManager;
    IUIAnimationTimer *m_pAnimationTimer;
    IUIAnimationTransitionLibrary *m_pTransitionLibrary;

    ...

};
```



## <a name="next-step"></a><span data-ttu-id="870d0-116">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="870d0-116">Next Step</span></span>

<span data-ttu-id="870d0-117">Nachdem Sie diesen Schritt abgeschlossen haben, ist der nächste Schritt: [Erstellen von Animations Variablen](create-animation-variables.md).</span><span class="sxs-lookup"><span data-stu-id="870d0-117">After completing this step, the next step is: [Create Animation Variables](create-animation-variables.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="870d0-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="870d0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="870d0-119">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="870d0-119">**CoCreateInstance**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="870d0-120">**Iuianimationmanager**</span><span class="sxs-lookup"><span data-stu-id="870d0-120">**IUIAnimationManager**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[<span data-ttu-id="870d0-121">**Iuianimationtimer**</span><span class="sxs-lookup"><span data-stu-id="870d0-121">**IUIAnimationTimer**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtimer)
</dt> <dt>

[<span data-ttu-id="870d0-122">**Iuianimationtransitionlibrary**</span><span class="sxs-lookup"><span data-stu-id="870d0-122">**IUIAnimationTransitionLibrary**</span></span>](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> <dt>

[<span data-ttu-id="870d0-123">Übersicht über Windows-Animationen</span><span class="sxs-lookup"><span data-stu-id="870d0-123">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 