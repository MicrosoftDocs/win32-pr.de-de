---
title: Erstellen eines Storyboards und Hinzufügen von Übergängen
description: Zum Erstellen einer Animation muss eine Anwendung ein Storyboard erstellen.
ms.assetid: e2641c93-e520-4749-a98e-5a58c175fdb9
keywords:
- Storyboards Windows-Animation, erstellen
- Storyboards Windows-Animation, Hinzufügen von Übergängen
- Übergänge Windows-Animation, erstellen
- Übergänge Windows-Animation, hinzufügen zu Storyboard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee85aac4db11371c9a1e4a2aa254421d217cfd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310864"
---
# <a name="create-a-storyboard-and-add-transitions"></a><span data-ttu-id="bc642-107">Erstellen eines Storyboards und Hinzufügen von Übergängen</span><span class="sxs-lookup"><span data-stu-id="bc642-107">Create a Storyboard and Add Transitions</span></span>

<span data-ttu-id="bc642-108">Zum Erstellen einer Animation muss eine Anwendung ein Storyboard erstellen.</span><span class="sxs-lookup"><span data-stu-id="bc642-108">To create an animation, an application must construct a storyboard.</span></span>

## <a name="overview"></a><span data-ttu-id="bc642-109">Übersicht</span><span class="sxs-lookup"><span data-stu-id="bc642-109">Overview</span></span>

<span data-ttu-id="bc642-110">Die allgemeinen Schritte zum Erstellen eines Storyboards lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="bc642-110">The general steps for constructing a storyboard are as follows:</span></span>

1.  <span data-ttu-id="bc642-111">Storyboard erstellen</span><span class="sxs-lookup"><span data-stu-id="bc642-111">Create a storyboard</span></span>
2.  <span data-ttu-id="bc642-112">Erstellen eines oder mehrerer Übergänge</span><span class="sxs-lookup"><span data-stu-id="bc642-112">Create one or more transitions</span></span>
3.  <span data-ttu-id="bc642-113">Fügen Sie die Übergänge zum Storyboard hinzu, und geben Sie an, welche Variablen animiert werden.</span><span class="sxs-lookup"><span data-stu-id="bc642-113">Add the transitions to the storyboard, specifying which variables they animate</span></span>

<span data-ttu-id="bc642-114">Ein leeres Storyboard kann mit dem Animations-Manager erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="bc642-114">An empty storyboard can be created using the animation manager.</span></span> <span data-ttu-id="bc642-115">Die Anwendung muss jedes Storyboard mit Übergängen auffüllen.</span><span class="sxs-lookup"><span data-stu-id="bc642-115">The application must populate each storyboard with transitions.</span></span> <span data-ttu-id="bc642-116">Jeder Übergang gibt an, wie sich eine einzelne Animations Variable für ein bestimmtes Zeitintervall ändert.</span><span class="sxs-lookup"><span data-stu-id="bc642-116">Each transition specifies how a single animation variable changes over a given time interval.</span></span> <span data-ttu-id="bc642-117">Übergänge können mithilfe der Übergangs Bibliotheks Komponente erstellt werden, die in der Windows-Animation enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="bc642-117">Transitions can be created using the transition library component included in Windows Animation.</span></span> <span data-ttu-id="bc642-118">Alternativ kann eine Anwendung eigene benutzerdefinierte Übergänge erstellen oder eine Übergangs Bibliothek von Drittanbietern verwenden.</span><span class="sxs-lookup"><span data-stu-id="bc642-118">Alternately, an application can create its own custom transitions or use a transition library from a third party.</span></span> <span data-ttu-id="bc642-119">Wenn die Anwendung einen Übergang zu einem Storyboard hinzufügt, gibt Sie an, welche Animations Variable der Übergang animieren soll.</span><span class="sxs-lookup"><span data-stu-id="bc642-119">When the application adds a transition to a storyboard, it specifies which animation variable the transition will animate.</span></span>

<span data-ttu-id="bc642-120">Ein Storyboard kann Übergänge für eine oder mehrere Animations Variablen enthalten.</span><span class="sxs-lookup"><span data-stu-id="bc642-120">A storyboard may include transitions on one or more animation variables.</span></span> <span data-ttu-id="bc642-121">Komplexere Storyboards können Keyframes verwenden, um die Starts oder enden von Übergängen zu synchronisieren oder um Teile des Storyboards anzugeben, die wiederholt werden sollen (eine festgelegte Anzahl von Zeiten oder unbegrenzt).</span><span class="sxs-lookup"><span data-stu-id="bc642-121">More complex storyboards can use keyframes to synchronize the starts or ends of transitions, or to specify portions of the storyboard that should repeat (a fixed number of times or indefinitely).</span></span>

## <a name="example-code"></a><span data-ttu-id="bc642-122">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="bc642-122">Example Code</span></span>

<span data-ttu-id="bc642-123">Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" im Windows Animation Sample [Timer-gesteuerte Animation](timer-driven-animation-sample.md). Weitere Informationen finden Sie unter der CMainWindow:: ChangeColor-Methode.</span><span class="sxs-lookup"><span data-stu-id="bc642-123">The following example code is taken from MainWindow.cpp in the Windows Animation sample [Timer-Driven Animation](timer-driven-animation-sample.md); see the CMainWindow::ChangeColor method.</span></span> <span data-ttu-id="bc642-124">In diesem Beispiel wird das Storyboard (Schritt 1) mithilfe von [**iuianimationmanager erstellt: die Methode "kreatestoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) " erstellt die Übergänge (Schritt 2) mithilfe der [**iuianimationtransitionlibrary::**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) -Methode der Methode "-Methode" und fügt die Übergänge dem Storyboard hinzu (Schritt 3), indem die [**iuianimationstoryboard:: addtransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) -Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bc642-124">This example creates the storyboard (step 1) using the [**IUIAnimationManager::CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) method, creates the transitions (step 2) using the [**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) method, and adds the transitions to the storyboard (step 3) using the [**IUIAnimationStoryboard::AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) method.</span></span>


```C++
const UI_ANIMATION_SECONDS DURATION = 0.5;
const DOUBLE ACCELERATION_RATIO = 0.5;
const DOUBLE DECELERATION_RATIO = 0.5;

// Create a storyboard

IUIAnimationStoryboard *pStoryboard = NULL;
HRESULT hr = m_pAnimationManager->CreateStoryboard(
    &pStoryboard
    );
if (SUCCEEDED(hr))
{
    // Create transitions for the RGB animation variables

    IUIAnimationTransition *pTransitionRed;
    hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
        DURATION,
        red,
        ACCELERATION_RATIO,
        DECELERATION_RATIO,
        &pTransitionRed
        );
    if (SUCCEEDED(hr))
    {
        IUIAnimationTransition *pTransitionGreen;
        hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
            DURATION,
            green,
            ACCELERATION_RATIO,
            DECELERATION_RATIO,
            &pTransitionGreen
            );
        if (SUCCEEDED(hr))
        {
            IUIAnimationTransition *pTransitionBlue;
            hr = m_pTransitionLibrary->CreateAccelerateDecelerateTransition(
                DURATION,
                blue,
                ACCELERATION_RATIO,
                DECELERATION_RATIO,
                &pTransitionBlue
                );
            if (SUCCEEDED(hr))
            {
                // Add transitions to the storyboard

                hr = pStoryboard->AddTransition(
                    m_pAnimationVariableRed,
                    pTransitionRed
                    );
                if (SUCCEEDED(hr))
                {
                    hr = pStoryboard->AddTransition(
                        m_pAnimationVariableGreen,
                        pTransitionGreen
                        );
                    if (SUCCEEDED(hr))
                    {
                        hr = pStoryboard->AddTransition(
                            m_pAnimationVariableBlue,
                            pTransitionBlue
                            );
                        if (SUCCEEDED(hr))
                        {
                            // Get the current time and schedule the storyboard for play

                            ...

}
```



## <a name="previous-step"></a><span data-ttu-id="bc642-125">Vorheriger Schritt</span><span class="sxs-lookup"><span data-stu-id="bc642-125">Previous Step</span></span>

<span data-ttu-id="bc642-126">Bevor Sie mit diesem Schritt beginnen, sollten Sie diesen Schritt abgeschlossen haben: [Lesen der Animations Variablen Werte](updating---application-driven-animation.md).</span><span class="sxs-lookup"><span data-stu-id="bc642-126">Before starting this step, you should have completed this step: [Read the Animation Variable Values](updating---application-driven-animation.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="bc642-127">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="bc642-127">Next Step</span></span>

<span data-ttu-id="bc642-128">Nachdem Sie diesen Schritt abgeschlossen haben, ist der nächste Schritt: [Planen eines Storyboards](scheduling-a-storyboard.md).</span><span class="sxs-lookup"><span data-stu-id="bc642-128">After completing this step, the next step is: [Schedule a Storyboard](scheduling-a-storyboard.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc642-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bc642-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc642-130">**Iuianimationmanager:: foratestoryboard**</span><span class="sxs-lookup"><span data-stu-id="bc642-130">**IUIAnimationManager::CreateStoryboard**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard)
</dt> <dt>

[<span data-ttu-id="bc642-131">**Iuianimationstoryboard:: addtransition**</span><span class="sxs-lookup"><span data-stu-id="bc642-131">**IUIAnimationStoryboard::AddTransition**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition)
</dt> <dt>

[<span data-ttu-id="bc642-132">**Iuianimationtransitionlibrary:: feateaccelerateverlangsamatetransition**</span><span class="sxs-lookup"><span data-stu-id="bc642-132">**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition)
</dt> <dt>

[<span data-ttu-id="bc642-133">Übersicht über Storyboards</span><span class="sxs-lookup"><span data-stu-id="bc642-133">Storyboard Overview</span></span>](storyboard-construction.md)
</dt> </dl>

 

 




