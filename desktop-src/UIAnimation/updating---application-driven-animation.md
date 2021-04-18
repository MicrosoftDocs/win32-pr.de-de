---
title: Lesen der Animations Variablen Werte
description: Jedes Mal, wenn die Anwendung zeichnet, sollte Sie die aktuellen Werte der Animations Variablen lesen, die die zu animierenden visuellen Merkmale darstellen.
ms.assetid: 7abf084a-31f5-4e32-bfd1-e88fbc2bf63d
keywords:
- Animations Variablen Windows-Animation, lesen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16187547bb3efd99a2f45a8fcc0668a6b6603efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337854"
---
# <a name="read-the-animation-variable-values"></a><span data-ttu-id="ff72f-104">Lesen der Animations Variablen Werte</span><span class="sxs-lookup"><span data-stu-id="ff72f-104">Read the Animation Variable Values</span></span>

<span data-ttu-id="ff72f-105">Jedes Mal, wenn die Anwendung zeichnet, sollte Sie die aktuellen Werte der Animations Variablen lesen, die die zu animierenden visuellen Merkmale darstellen.</span><span class="sxs-lookup"><span data-stu-id="ff72f-105">Each time your application paints, it should read the current values of the animation variables that represent the visual characteristics to be animated.</span></span>

## <a name="overview"></a><span data-ttu-id="ff72f-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="ff72f-106">Overview</span></span>

<span data-ttu-id="ff72f-107">Beim Zeichnen eines Frames kann eine Anwendung die [**iuianimationvariable:: GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) -Methode oder die [**iuianimationvariable:: getIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) -Methode verwenden, um die Werte aller Animations Variablen anzufordern, die sich auf visuelle Elemente innerhalb des Frames auswirken.</span><span class="sxs-lookup"><span data-stu-id="ff72f-107">When drawing a frame, an application can use the [**IUIAnimationVariable::GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) or [**IUIAnimationVariable::GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) method to request the values of any animation variables that will affect visuals within the frame.</span></span> <span data-ttu-id="ff72f-108">Es ist möglich, eine Animations Variable auf einen Wertebereich ([**setlowerbound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) und [**setupperbound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)) zu setzen und ihren Wert mit einem angegebenen Rundungs Schema ([**setroundingmode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)) auf eine ganze Zahl zu setzen.</span><span class="sxs-lookup"><span data-stu-id="ff72f-108">It is possible to clip an animation variable to a range of values ([**SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) and [**SetUpperBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)), and to request its value be rounded to an integer using a specified rounding scheme ([**SetRoundingMode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)).</span></span>

<span data-ttu-id="ff72f-109">Anstatt die Werte aller Variablen für jeden Frame zu lesen, kann eine Anwendung den [**iuianimationvariable:: setvariablechangehandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) oder [**iuianimationvariable:: setvariableintegerchangehandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) -Methode zum Registrieren mindestens eines Variablen Änderungs Handler für den Empfang von Benachrichtigungen, wenn eine Änderung am Wert der Variablen ([**iuianimationvariablechangehandler:: OnValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)) oder auf einem gerundeten Wert ([**iuianimationvariableintegerchangehandler:: onintegervaluechanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)) vorliegt.</span><span class="sxs-lookup"><span data-stu-id="ff72f-109">Instead of reading the values of all variables for every frame, an application can use the [**IUIAnimationVariable::SetVariableChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) or [**IUIAnimationVariable::SetVariableIntegerChangeHandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) method to register one or more variable change handlers to receive notifications only when there is a change to the variables' value ([**IUIAnimationVariableChangeHandler::OnValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)) or rounded value ([**IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)).</span></span> <span data-ttu-id="ff72f-110">Um die an Variablen Änderungs Handler übergebenen Variablen zu identifizieren, kann eine Anwendung mithilfe der [**iuianimationvariable:: settag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) -Methode Tags auf Variablen anwenden.</span><span class="sxs-lookup"><span data-stu-id="ff72f-110">To identify the variables passed to variable change handlers, an application can apply tags to variables using the [**IUIAnimationVariable::SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) method.</span></span> <span data-ttu-id="ff72f-111">Dabei handelt es sich um Objekt (IUnknown \* ), ganzzahlige Paare, die von der Anwendung interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="ff72f-111">These are object (IUnknown\*), integer pairs that are interpreted by the application.</span></span>

## <a name="example-code"></a><span data-ttu-id="ff72f-112">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="ff72f-112">Example Code</span></span>

<span data-ttu-id="ff72f-113">Der folgende Beispielcode stammt aus "Miniaturansicht. cpp" im Beispiel [Raster Layout](/windows/desktop/UIAnimation/grid-layout-sample)der Windows-Animation. Weitere Informationen finden Sie unter der CMainWindow:: Rendering-Methode.</span><span class="sxs-lookup"><span data-stu-id="ff72f-113">The following example code is taken from Thumbnail.cpp in the Windows Animation sample [Grid Layout](/windows/desktop/UIAnimation/grid-layout-sample); see the CMainWindow::Render method.</span></span> <span data-ttu-id="ff72f-114">Er verwendet die [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) -Methode, um die Werte als Gleit Komma Werte zu lesen.</span><span class="sxs-lookup"><span data-stu-id="ff72f-114">It uses the [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) method to read the values as floating-point values.</span></span>


```C++
// Get the x-coordinate and y-coordinate animation variable values

DOUBLE x=0;
hr = m_pAnimationVariableX->GetValue(&x);
if (SUCCEEDED(hr))
{
    DOUBLE y=0;
    hr = m_pAnimationVariableY->GetValue(&y);
    if (SUCCEEDED(hr))
    {
        // Draw the object

        ...

    }
}
```



<span data-ttu-id="ff72f-115">Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" im Windows Animation Sample [Timer-gesteuerte Animation](timer-driven-animation-sample.md). Weitere Informationen finden Sie unter CMainWindow::D rawbackground-Methode.</span><span class="sxs-lookup"><span data-stu-id="ff72f-115">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::DrawBackground method.</span></span> <span data-ttu-id="ff72f-116">Er verwendet die [**getIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) -Methode, um die Werte als ganzzahlige Werte zu lesen.</span><span class="sxs-lookup"><span data-stu-id="ff72f-116">It uses the [**GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) method to read the values as integer values.</span></span>


```C++
// Get the RGB animation variable values

INT32 red;
HRESULT hr = m_pAnimationVariableRed->GetIntegerValue(
    &red
    );
if (SUCCEEDED(hr))
{
    INT32 green;
    hr = m_pAnimationVariableGreen->GetIntegerValue(
        &green
        );
    if (SUCCEEDED(hr))
    {
        INT32 blue;
        hr = m_pAnimationVariableBlue->GetIntegerValue(
            &blue
            );
        if (SUCCEEDED(hr))
        {
            // Set the RGB of the background brush to the new animated value

            ...
                
            // Paint the background

            ...

        }
    }

    ...

}
```



## <a name="previous-step"></a><span data-ttu-id="ff72f-117">Vorheriger Schritt</span><span class="sxs-lookup"><span data-stu-id="ff72f-117">Previous Step</span></span>

<span data-ttu-id="ff72f-118">Bevor Sie mit diesem Schritt beginnen, sollten Sie diesen Schritt abgeschlossen haben: [Aktualisieren Sie den Animations-Manager, und zeichnen Sie Frames](introducing-windows-animation-manager.md).</span><span class="sxs-lookup"><span data-stu-id="ff72f-118">Before starting this step, you should have completed this step: [Update the Animation Manager and Draw Frames](introducing-windows-animation-manager.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="ff72f-119">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="ff72f-119">Next Step</span></span>

<span data-ttu-id="ff72f-120">Nachdem Sie diesen Schritt abgeschlossen haben, ist der nächste Schritt: [Erstellen eines Storyboards und hinzufügen](updating---timer-driven-animation.md)von Übergängen.</span><span class="sxs-lookup"><span data-stu-id="ff72f-120">After completing this step, the next step is: [Create a Storyboard and Add Transitions](updating---timer-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff72f-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ff72f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff72f-122">**Iuianimationvariable:: getIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="ff72f-122">**IUIAnimationVariable::GetIntegerValue**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue)
</dt> <dt>

[<span data-ttu-id="ff72f-123">**Iuianimationvariable:: GetValue**</span><span class="sxs-lookup"><span data-stu-id="ff72f-123">**IUIAnimationVariable::GetValue**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue)
</dt> <dt>

[<span data-ttu-id="ff72f-124">Übersicht über Windows-Animationen</span><span class="sxs-lookup"><span data-stu-id="ff72f-124">Windows Animation Overview</span></span>](scenic-animation-api-overview.md)
</dt> </dl>

 

 