---
title: Erstellen von Animations Variablen
description: Eine Anwendung muss eine Animations Variable für jedes visuelle Merkmal erstellen, das mithilfe der Windows-Animation animiert werden soll.
ms.assetid: 360aa157-cb50-400a-b373-45885410469d
keywords:
- Animations Variablen Windows-Animation, erstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c059a924e22700bb4abd794435ad708a2775a9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390828"
---
# <a name="create-animation-variables"></a><span data-ttu-id="97ff4-104">Erstellen von Animations Variablen</span><span class="sxs-lookup"><span data-stu-id="97ff4-104">Create Animation Variables</span></span>

<span data-ttu-id="97ff4-105">Eine Anwendung muss eine Animations Variable für jedes visuelle Merkmal erstellen, das mithilfe der Windows-Animation animiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="97ff4-105">An application must create an animation variable for each visual characteristic that is to be animated using Windows Animation.</span></span>

## <a name="overview"></a><span data-ttu-id="97ff4-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="97ff4-106">Overview</span></span>

<span data-ttu-id="97ff4-107">Animations Variablen werden mit dem Animations-Manager erstellt, und die Anwendung sollte einen Verweis auf jede für die Dauer beibehalten, sofern Sie benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="97ff4-107">Animation variables are created using the animation manager, and the application should retain a reference to each for as long as it is needed.</span></span> <span data-ttu-id="97ff4-108">Die Anwendung erstellt in der Regel jede Animations Variable zur gleichen Zeit wie das visuelle Objekt, das Sie animiert.</span><span class="sxs-lookup"><span data-stu-id="97ff4-108">Your application will generally create each animation variable at the same time as the visual object it animates.</span></span>

<span data-ttu-id="97ff4-109">Wenn eine Animations Variable erstellt wird, muss der Anfangswert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="97ff4-109">When an animation variable is created, its initial value must be specified.</span></span> <span data-ttu-id="97ff4-110">Danach kann der Wert nur geändert werden, indem Storyboards geplant werden, die ihn animieren.</span><span class="sxs-lookup"><span data-stu-id="97ff4-110">Thereafter, its value can only be altered by scheduling storyboards that animate it.</span></span>

<span data-ttu-id="97ff4-111">Animations Variablen werden bei der Erstellung von Storyboards als Parameter weitergegeben, sodass die Anwendung Sie nicht freigeben sollte, bis die visuellen Merkmale, die Sie darstellen, nicht mehr animiert werden müssen. Dies ist in der Regel der Fall, wenn die zugehörigen visuellen Objekte zerstört werden.</span><span class="sxs-lookup"><span data-stu-id="97ff4-111">Animation variables are passed as parameters when storyboards are constructed, so the application should not release them until the visual characteristics they represent no longer need to be animated, typically when the associated visual objects are about to be destroyed.</span></span>

## <a name="example-code"></a><span data-ttu-id="97ff4-112">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="97ff4-112">Example Code</span></span>

-   [<span data-ttu-id="97ff4-113">Animieren von Farben</span><span class="sxs-lookup"><span data-stu-id="97ff4-113">Animating Colors</span></span>](#animating-colors)
-   [<span data-ttu-id="97ff4-114">Animieren von x-und y-Koordinaten</span><span class="sxs-lookup"><span data-stu-id="97ff4-114">Animating x and y Coordinates</span></span>](#animating-x-and-y-coordinates)

### <a name="animating-colors"></a><span data-ttu-id="97ff4-115">Animieren von Farben</span><span class="sxs-lookup"><span data-stu-id="97ff4-115">Animating Colors</span></span>

<span data-ttu-id="97ff4-116">Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" in den Windows-Animations Beispielen [Anwendungs gesteuerte Animation](application-driven-animation-sample.md) und [Timer-gesteuerte Animation](timer-driven-animation-sample.md).</span><span class="sxs-lookup"><span data-stu-id="97ff4-116">The following example code is taken from MainWindow.cpp in the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="97ff4-117">Im Beispiel werden drei Animations Variablen mithilfe von "" [**erstellt, um**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) Hintergrundfarben darzustellen.</span><span class="sxs-lookup"><span data-stu-id="97ff4-117">In the example, three animation variables are created using [**CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) to represent background colors.</span></span> <span data-ttu-id="97ff4-118">Der Code verwendet auch die [**setlowerbound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) -Methode und die [**setupperbound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) -Methode, um den Wert der Animations Variablen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="97ff4-118">The code also uses the [**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) and [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) methods to control the value of the animation variable.</span></span>


```
const DOUBLE INITIAL_RED = COLOR_MAX;
const DOUBLE INITIAL_GREEN = COLOR_MAX;
const DOUBLE INITIAL_BLUE = COLOR_MAX;

HRESULT hr = m_pAnimationManager->CreateAnimationVariable(
    INITIAL_RED,
    &m_pAnimationVariableRed
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationVariableRed->SetLowerBound(COLOR_MIN);
    if (SUCCEEDED(hr))
    {
        hr = m_pAnimationVariableRed->SetUpperBound(COLOR_MAX);
        if (SUCCEEDED(hr))
        {
            hr = m_pAnimationManager->CreateAnimationVariable(
                INITIAL_GREEN,
                &m_pAnimationVariableGreen
                );
            if (SUCCEEDED(hr))
            {
                hr = m_pAnimationVariableGreen->SetLowerBound(COLOR_MIN);
                if (SUCCEEDED(hr))
                {
                    hr = m_pAnimationVariableGreen->SetUpperBound(COLOR_MAX);
                    if (SUCCEEDED(hr))
                    {
                        hr = m_pAnimationManager->CreateAnimationVariable(
                            INITIAL_BLUE,
                            &m_pAnimationVariableBlue
                            );
                        if (SUCCEEDED(hr))
                        {
                            hr = m_pAnimationVariableBlue->SetLowerBound(COLOR_MIN);
                            if (SUCCEEDED(hr))
                            {
                                hr = m_pAnimationVariableBlue->SetUpperBound(COLOR_MAX);
                            }
                        }
                    }
                }
            }
        }
    }
}
```



<span data-ttu-id="97ff4-119">Beachten Sie die folgenden Definitionen von "MainWindow. h".</span><span class="sxs-lookup"><span data-stu-id="97ff4-119">Note the following definitions from MainWindow.h.</span></span>


```
class CMainWindow
{

    ...

private:

    // Animated Variables

    IUIAnimationVariable *m_pAnimationVariableRed;
    IUIAnimationVariable *m_pAnimationVariableGreen;
    IUIAnimationVariable *m_pAnimationVariableBlue;

    ...

};
```



### <a name="animating-x-and-y-coordinates"></a><span data-ttu-id="97ff4-120">Animieren von x-und y-Koordinaten</span><span class="sxs-lookup"><span data-stu-id="97ff4-120">Animating x and y Coordinates</span></span>

<span data-ttu-id="97ff4-121">Der folgende Beispielcode stammt aus "Miniaturansicht. cpp" im Windows-Animations [Raster-Layoutbeispiel](/windows/desktop/UIAnimation/grid-layout-sample). Weitere Informationen finden Sie unter der CMainWindow:: erkreateanimationvariables-Methode.</span><span class="sxs-lookup"><span data-stu-id="97ff4-121">The following example code is taken from Thumbnail.cpp in the Windows Animation [Grid Layout Sample](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::CreateAnimationVariables method.</span></span> <span data-ttu-id="97ff4-122">Es werden zwei Animations Variablen erstellt, die die X-und Y-Koordinaten der einzelnen-Objekte darstellen.</span><span class="sxs-lookup"><span data-stu-id="97ff4-122">Two animation variables are created to represent the X and Y coordinates of each object.</span></span>


```C++
// Create the animation variables for the x and y coordinates

hr = m_pAnimationManager->CreateAnimationVariable(
    xInitial,
    &m_pAnimationVariableX
    );

if (SUCCEEDED(hr))
{
    hr = m_pAnimationManager->CreateAnimationVariable(
        yInitial,
        &m_pAnimationVariableY
        );

    ...

}
```



<span data-ttu-id="97ff4-123">Beachten Sie die folgenden Definitionen aus "Miniaturansicht. h".</span><span class="sxs-lookup"><span data-stu-id="97ff4-123">Note the following definitions from Thumbnail.h.</span></span>


```
class CThumbnail
{
public:

    ...

    // X and Y Animation Variables

    IUIAnimationVariable *m_pAnimationVariableX;
    IUIAnimationVariable *m_pAnimationVariableY;

    ...

};
```



<span data-ttu-id="97ff4-124">Animations Variablen sind Gleit Komma Zahlen, aber ihre Werte können auch als ganze Zahlen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="97ff4-124">Animation variables are floating-point numbers, but their values can be fetched as integers, too.</span></span> <span data-ttu-id="97ff4-125">Standardmäßig wird jeder Wert auf die nächste ganze Zahl gerundet, aber es ist möglich, den für eine Variable verwendeten Rundungs Modus zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="97ff4-125">By default, each value will be rounded to the nearest integer, but it is possible to override the rounding mode used for a variable.</span></span> <span data-ttu-id="97ff4-126">Der folgende Beispielcode verwendet die [**setroundingmode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) -Methode, um anzugeben, dass die Werte immer gerundet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="97ff4-126">The following example code uses the [**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) method to specify that the values should always be rounded down.</span></span>


```C++
hr = m_pAnimationVariableX->SetRoundingMode(
    UI_ANIMATION_ROUNDING_MODE_FLOOR
    );
if (SUCCEEDED(hr))
{
    hr = m_pAnimationVariableY->SetRoundingMode(
        UI_ANIMATION_ROUNDING_MODE_FLOOR
        );

    ...

}
```



## <a name="previous-step"></a><span data-ttu-id="97ff4-127">Vorheriger Schritt</span><span class="sxs-lookup"><span data-stu-id="97ff4-127">Previous Step</span></span>

<span data-ttu-id="97ff4-128">Bevor Sie mit diesem Schritt beginnen, sollten Sie diesen Schritt abgeschlossen haben: [Erstellen der Haupt Animations Objekte](adding-animation-to-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="97ff4-128">Before starting this step, you should have completed this step: [Create the Main Animation Objects](adding-animation-to-an-application.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="97ff4-129">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="97ff4-129">Next Step</span></span>

<span data-ttu-id="97ff4-130">Nachdem Sie diesen Schritt abgeschlossen haben, ist der nächste Schritt: [Aktualisieren des Animations-Managers und Zeichnen von Frames](introducing-windows-animation-manager.md).</span><span class="sxs-lookup"><span data-stu-id="97ff4-130">After completing this step, the next step is: [Update the Animation Manager and Draw Frames](introducing-windows-animation-manager.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="97ff4-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="97ff4-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97ff4-132">**Iuianimationmanager:: kreateanimationvariable**</span><span class="sxs-lookup"><span data-stu-id="97ff4-132">**IUIAnimationManager::CreateAnimationVariable**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable)
</dt> <dt>

[<span data-ttu-id="97ff4-133">**Iuianimationvariable:: setlowerbound**</span><span class="sxs-lookup"><span data-stu-id="97ff4-133">**IUIAnimationVariable::SetLowerBound**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound)
</dt> <dt>

[<span data-ttu-id="97ff4-134">**Iuianimationvariable:: setroundingmode**</span><span class="sxs-lookup"><span data-stu-id="97ff4-134">**IUIAnimationVariable::SetRoundingMode**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)
</dt> <dt>

[<span data-ttu-id="97ff4-135">**Iuianimationvariable:: setupperbound**</span><span class="sxs-lookup"><span data-stu-id="97ff4-135">**IUIAnimationVariable::SetUpperBound**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)
</dt> <dt>

[<span data-ttu-id="97ff4-136">Übersicht über Windows-Animationen</span><span class="sxs-lookup"><span data-stu-id="97ff4-136">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 