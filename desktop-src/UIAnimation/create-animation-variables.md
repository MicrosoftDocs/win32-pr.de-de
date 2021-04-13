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
# <a name="create-animation-variables"></a>Erstellen von Animations Variablen

Eine Anwendung muss eine Animations Variable für jedes visuelle Merkmal erstellen, das mithilfe der Windows-Animation animiert werden soll.

## <a name="overview"></a>Übersicht

Animations Variablen werden mit dem Animations-Manager erstellt, und die Anwendung sollte einen Verweis auf jede für die Dauer beibehalten, sofern Sie benötigt wird. Die Anwendung erstellt in der Regel jede Animations Variable zur gleichen Zeit wie das visuelle Objekt, das Sie animiert.

Wenn eine Animations Variable erstellt wird, muss der Anfangswert angegeben werden. Danach kann der Wert nur geändert werden, indem Storyboards geplant werden, die ihn animieren.

Animations Variablen werden bei der Erstellung von Storyboards als Parameter weitergegeben, sodass die Anwendung Sie nicht freigeben sollte, bis die visuellen Merkmale, die Sie darstellen, nicht mehr animiert werden müssen. Dies ist in der Regel der Fall, wenn die zugehörigen visuellen Objekte zerstört werden.

## <a name="example-code"></a>Beispielcode

-   [Animieren von Farben](#animating-colors)
-   [Animieren von x-und y-Koordinaten](#animating-x-and-y-coordinates)

### <a name="animating-colors"></a>Animieren von Farben

Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" in den Windows-Animations Beispielen [Anwendungs gesteuerte Animation](application-driven-animation-sample.md) und [Timer-gesteuerte Animation](timer-driven-animation-sample.md). Im Beispiel werden drei Animations Variablen mithilfe von "" [**erstellt, um**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) Hintergrundfarben darzustellen. Der Code verwendet auch die [**setlowerbound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) -Methode und die [**setupperbound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound) -Methode, um den Wert der Animations Variablen zu steuern.


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



Beachten Sie die folgenden Definitionen von "MainWindow. h".


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



### <a name="animating-x-and-y-coordinates"></a>Animieren von x-und y-Koordinaten

Der folgende Beispielcode stammt aus "Miniaturansicht. cpp" im Windows-Animations [Raster-Layoutbeispiel](/windows/desktop/UIAnimation/grid-layout-sample). Weitere Informationen finden Sie unter der CMainWindow:: erkreateanimationvariables-Methode. Es werden zwei Animations Variablen erstellt, die die X-und Y-Koordinaten der einzelnen-Objekte darstellen.


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



Beachten Sie die folgenden Definitionen aus "Miniaturansicht. h".


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



Animations Variablen sind Gleit Komma Zahlen, aber ihre Werte können auch als ganze Zahlen abgerufen werden. Standardmäßig wird jeder Wert auf die nächste ganze Zahl gerundet, aber es ist möglich, den für eine Variable verwendeten Rundungs Modus zu überschreiben. Der folgende Beispielcode verwendet die [**setroundingmode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode) -Methode, um anzugeben, dass die Werte immer gerundet werden sollen.


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



## <a name="previous-step"></a>Vorheriger Schritt

Bevor Sie mit diesem Schritt beginnen, sollten Sie diesen Schritt abgeschlossen haben: [Erstellen der Haupt Animations Objekte](adding-animation-to-an-application.md).

## <a name="next-step"></a>Nächster Schritt

Nachdem Sie diesen Schritt abgeschlossen haben, ist der nächste Schritt: [Aktualisieren des Animations-Managers und Zeichnen von Frames](introducing-windows-animation-manager.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iuianimationmanager:: kreateanimationvariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable)
</dt> <dt>

[**Iuianimationvariable:: setlowerbound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound)
</dt> <dt>

[**Iuianimationvariable:: setroundingmode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)
</dt> <dt>

[**Iuianimationvariable:: setupperbound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)
</dt> <dt>

[Übersicht über Windows-Animationen](scenic-animation-api-overview.md)
</dt> </dl>

 

 