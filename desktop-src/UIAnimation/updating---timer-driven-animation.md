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
# <a name="create-a-storyboard-and-add-transitions"></a>Erstellen eines Storyboards und Hinzufügen von Übergängen

Zum Erstellen einer Animation muss eine Anwendung ein Storyboard erstellen.

## <a name="overview"></a>Übersicht

Die allgemeinen Schritte zum Erstellen eines Storyboards lauten wie folgt:

1.  Storyboard erstellen
2.  Erstellen eines oder mehrerer Übergänge
3.  Fügen Sie die Übergänge zum Storyboard hinzu, und geben Sie an, welche Variablen animiert werden.

Ein leeres Storyboard kann mit dem Animations-Manager erstellt werden. Die Anwendung muss jedes Storyboard mit Übergängen auffüllen. Jeder Übergang gibt an, wie sich eine einzelne Animations Variable für ein bestimmtes Zeitintervall ändert. Übergänge können mithilfe der Übergangs Bibliotheks Komponente erstellt werden, die in der Windows-Animation enthalten ist. Alternativ kann eine Anwendung eigene benutzerdefinierte Übergänge erstellen oder eine Übergangs Bibliothek von Drittanbietern verwenden. Wenn die Anwendung einen Übergang zu einem Storyboard hinzufügt, gibt Sie an, welche Animations Variable der Übergang animieren soll.

Ein Storyboard kann Übergänge für eine oder mehrere Animations Variablen enthalten. Komplexere Storyboards können Keyframes verwenden, um die Starts oder enden von Übergängen zu synchronisieren oder um Teile des Storyboards anzugeben, die wiederholt werden sollen (eine festgelegte Anzahl von Zeiten oder unbegrenzt).

## <a name="example-code"></a>Beispielcode

Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" im Windows Animation Sample [Timer-gesteuerte Animation](timer-driven-animation-sample.md). Weitere Informationen finden Sie unter der CMainWindow:: ChangeColor-Methode. In diesem Beispiel wird das Storyboard (Schritt 1) mithilfe von [**iuianimationmanager erstellt: die Methode "kreatestoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) " erstellt die Übergänge (Schritt 2) mithilfe der [**iuianimationtransitionlibrary::**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition) -Methode der Methode "-Methode" und fügt die Übergänge dem Storyboard hinzu (Schritt 3), indem die [**iuianimationstoryboard:: addtransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) -Methode verwendet wird.


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

Bevor Sie mit diesem Schritt beginnen, sollten Sie diesen Schritt abgeschlossen haben: [Lesen der Animations Variablen Werte](updating---application-driven-animation.md).

## <a name="next-step"></a>Nächster Schritt

Nachdem Sie diesen Schritt abgeschlossen haben, ist der nächste Schritt: [Planen eines Storyboards](scheduling-a-storyboard.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iuianimationmanager:: foratestoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard)
</dt> <dt>

[**Iuianimationstoryboard:: addtransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition)
</dt> <dt>

[**Iuianimationtransitionlibrary:: feateaccelerateverlangsamatetransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createacceleratedeceleratetransition)
</dt> <dt>

[Übersicht über Storyboards](storyboard-construction.md)
</dt> </dl>

 

 




