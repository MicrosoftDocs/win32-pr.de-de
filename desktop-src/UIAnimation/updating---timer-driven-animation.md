---
title: Erstellen eines Storyboards und Hinzufügen von Übergängen
description: Um eine Animation zu erstellen, muss eine Anwendung ein Storyboard erstellen.
ms.assetid: e2641c93-e520-4749-a98e-5a58c175fdb9
keywords:
- Storyboards Windows Animation , erstellen
- Storyboards Windows Animation, Hinzufügen von Übergängen
- überlädt Windows Animation , erstellt
- überlädt Windows Animation und fügt dem Storyboard hinzu.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f992ae7720fea692d5e0b813e6cb9c35fab61d4bf2c781c928d9c8fcd08adb33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999640"
---
# <a name="create-a-storyboard-and-add-transitions"></a>Erstellen eines Storyboards und Hinzufügen von Übergängen

Um eine Animation zu erstellen, muss eine Anwendung ein Storyboard erstellen.

## <a name="overview"></a>Übersicht

Die allgemeinen Schritte zum Erstellen eines Storyboards sind wie folgt:

1.  Erstellen eines Storyboards
2.  Erstellen eines oder mehrerer Übergänge
3.  Fügen Sie die Übergänge zum Storyboard hinzu, und geben Sie an, welche Variablen sie animieren.

Ein leeres Storyboard kann mit dem Animations-Manager erstellt werden. Die Anwendung muss jedes Storyboard mit Übergängen auffüllen. Jeder Übergang gibt an, wie sich eine einzelne Animationsvariable in einem bestimmten Zeitintervall ändert. Übergänge können mithilfe der Übergangsbibliothekskomponente erstellt werden, die in Windows Animation enthalten ist. Alternativ kann eine Anwendung eigene benutzerdefinierte Übergänge erstellen oder eine Übergangsbibliothek von einem Drittanbieter verwenden. Wenn die Anwendung einem Storyboard einen Übergang hinzufügt, gibt sie an, welche Animationsvariable der Übergang animiert.

Ein Storyboard kann Übergänge für eine oder mehrere Animationsvariablen enthalten. Komplexere Storyboards können Keyframes verwenden, um die Start- oder Enden von Übergängen zu synchronisieren oder Teile des Storyboards anzugeben, die wiederholt werden sollen (eine feste Anzahl von Malen oder unbegrenzt).

## <a name="example-code"></a>Beispielcode

Der folgende Beispielcode stammt aus MainWindow.cpp in der [timergesteuerten Animation](timer-driven-animation-sample.md)Windows Animation. siehe die CMainWindow::ChangeColor-Methode. In diesem Beispiel wird das Storyboard (Schritt 1) mithilfe der [**IUIAnimationManager::CreateStoryboard-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) erstellt, die Übergänge (Schritt 2) mithilfe der [**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) erstellt und die Übergänge mithilfe der [**IUIAnimationStoryboard::AddTransition-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) zum Storyboard (Schritt 3) hinzugefügt.


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



## <a name="previous-step"></a>Vorheriger Schritt

Bevor Sie mit diesem Schritt beginnen, sollten Sie diesen Schritt abgeschlossen haben: [Lesen der Werte der Animationsvariablen](updating---application-driven-animation.md).

## <a name="next-step"></a>Nächster Schritt

Nach Abschluss dieses Schritts lautet der nächste Schritt: [Planen eines Storyboards.](scheduling-a-storyboard.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IUIAnimationManager::CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard)
</dt> <dt>

[**IUIAnimationStoryboard::AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition)
</dt> <dt>

[**IUIAnimationTransitionLibrary::CreateAccelerateDecelerateTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition)
</dt> <dt>

[Übersicht über Storyboards](storyboard-construction.md)
</dt> </dl>

 

 




