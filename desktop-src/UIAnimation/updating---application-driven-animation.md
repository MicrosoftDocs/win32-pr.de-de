---
title: Lesen der Werte der Animationsvariablen
description: Jedes Mal, wenn Ihre Anwendung zeichnet, sollte sie die aktuellen Werte der Animationsvariablen lesen, die die visuellen Merkmale darstellen, die animiert werden sollen.
ms.assetid: 7abf084a-31f5-4e32-bfd1-e88fbc2bf63d
keywords:
- Animationsvariablen Windows Animation , Lesen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2cc164091be9ecca292e26ab1247ba18c61d89f11dad8fc2530a3e45ca7629
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058167"
---
# <a name="read-the-animation-variable-values"></a>Lesen der Werte der Animationsvariablen

Jedes Mal, wenn Ihre Anwendung zeichnet, sollte sie die aktuellen Werte der Animationsvariablen lesen, die die visuellen Merkmale darstellen, die animiert werden sollen.

## <a name="overview"></a>Übersicht

Beim Zeichnen eines Frames kann eine Anwendung die [**IUIAnimationVariable::GetValue-**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) oder [**IUIAnimationVariable::GetIntegerValue-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) verwenden, um die Werte aller Animationsvariablen an fordern, die sich auf visuelle Elemente innerhalb des Frames auswirken. Es ist möglich, eine Animationsvariable in einen Wertebereich [**(SetLowerBound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) und [**SetUpperBound)**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)zu beschneiden und den Wert mithilfe eines angegebenen Rundungsschemas [**(SetRoundingMode)**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)auf eine ganze Zahl zu runden.

Anstatt die Werte aller Variablen für jeden Frame zu lesen, Eine Anwendung kann die [**IUIAnimationVariable::SetVariableChangeHandler-**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) oder [**IUIAnimationVariable::SetVariableIntegerChangeHandler-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) verwenden, um einen oder mehrere Variablenänderungshandler zum Empfangen von Benachrichtigungen nur dann zu registrieren, wenn sich der Wert der Variablen ([**IUIAnimationVariableChangeHandler::OnValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)) oder ein gerundeter Wert ([**IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)) ändert. Um die Variablen zu identifizieren, die an Variablenänderungshandler übergeben werden, kann eine Anwendung Tags mithilfe der [**IUIAnimationVariable::SetTag-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) auf Variablen anwenden. Dies sind Objektpaare (IUnknown), ganzzahlige \* Paare, die von der Anwendung interpretiert werden.

## <a name="example-code"></a>Beispielcode

Der folgende Beispielcode ist aus Thumbnail.cpp im Beispiel Windows Animation [Grid Layout entnommen.](/windows/desktop/UIAnimation/grid-layout-sample) siehe CMainWindow::Render-Methode. Sie verwendet die [**GetValue-Methode,**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) um die Werte als Gleitkommawerte zu lesen.


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



Der folgende Beispielcode wird aus MainWindow.cpp im Beispiel Windows [Animation Timer-Driven Animation ( Timergesteuerte Animation) entnommen.](timer-driven-animation-sample.md) siehe CMainWindow::D rawBackground-Methode. Sie verwendet die [**GetIntegerValue-Methode,**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) um die Werte als ganzzahlige Werte zu lesen.


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



## <a name="previous-step"></a>Vorheriger Schritt

Bevor Sie mit diesem Schritt beginnen, sollten Sie diesen Schritt abgeschlossen haben: Aktualisieren des [Animations-Managers und Zeichnen von Frames](introducing-windows-animation-manager.md).

## <a name="next-step"></a>Nächster Schritt

Nach Abschluss dieses Schritts ist der nächste Schritt: Erstellen eines [Storyboards und Hinzufügen von Übergängen](updating---timer-driven-animation.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IUIAnimationVariable::GetIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue)
</dt> <dt>

[**IUIAnimationVariable::GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue)
</dt> <dt>

[Windows Übersicht über Animationen](scenic-animation-api-overview.md)
</dt> </dl>

 

 