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
# <a name="read-the-animation-variable-values"></a>Lesen der Animations Variablen Werte

Jedes Mal, wenn die Anwendung zeichnet, sollte Sie die aktuellen Werte der Animations Variablen lesen, die die zu animierenden visuellen Merkmale darstellen.

## <a name="overview"></a>Übersicht

Beim Zeichnen eines Frames kann eine Anwendung die [**iuianimationvariable:: GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) -Methode oder die [**iuianimationvariable:: getIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) -Methode verwenden, um die Werte aller Animations Variablen anzufordern, die sich auf visuelle Elemente innerhalb des Frames auswirken. Es ist möglich, eine Animations Variable auf einen Wertebereich ([**setlowerbound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setlowerbound) und [**setupperbound**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setupperbound)) zu setzen und ihren Wert mit einem angegebenen Rundungs Schema ([**setroundingmode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setroundingmode)) auf eine ganze Zahl zu setzen.

Anstatt die Werte aller Variablen für jeden Frame zu lesen, kann eine Anwendung den [**iuianimationvariable:: setvariablechangehandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariablechangehandler) oder [**iuianimationvariable:: setvariableintegerchangehandler**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler) -Methode zum Registrieren mindestens eines Variablen Änderungs Handler für den Empfang von Benachrichtigungen, wenn eine Änderung am Wert der Variablen ([**iuianimationvariablechangehandler:: OnValueChanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged)) oder auf einem gerundeten Wert ([**iuianimationvariableintegerchangehandler:: onintegervaluechanged**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged)) vorliegt. Um die an Variablen Änderungs Handler übergebenen Variablen zu identifizieren, kann eine Anwendung mithilfe der [**iuianimationvariable:: settag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-settag) -Methode Tags auf Variablen anwenden. Dabei handelt es sich um Objekt (IUnknown \* ), ganzzahlige Paare, die von der Anwendung interpretiert werden.

## <a name="example-code"></a>Beispielcode

Der folgende Beispielcode stammt aus "Miniaturansicht. cpp" im Beispiel [Raster Layout](/windows/desktop/UIAnimation/grid-layout-sample)der Windows-Animation. Weitere Informationen finden Sie unter der CMainWindow:: Rendering-Methode. Er verwendet die [**GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue) -Methode, um die Werte als Gleit Komma Werte zu lesen.


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



Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" im Windows Animation Sample [Timer-gesteuerte Animation](timer-driven-animation-sample.md). Weitere Informationen finden Sie unter CMainWindow::D rawbackground-Methode. Er verwendet die [**getIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue) -Methode, um die Werte als ganzzahlige Werte zu lesen.


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

Bevor Sie mit diesem Schritt beginnen, sollten Sie diesen Schritt abgeschlossen haben: [Aktualisieren Sie den Animations-Manager, und zeichnen Sie Frames](introducing-windows-animation-manager.md).

## <a name="next-step"></a>Nächster Schritt

Nachdem Sie diesen Schritt abgeschlossen haben, ist der nächste Schritt: [Erstellen eines Storyboards und hinzufügen](updating---timer-driven-animation.md)von Übergängen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iuianimationvariable:: getIntegerValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getintegervalue)
</dt> <dt>

[**Iuianimationvariable:: GetValue**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationvariable-getvalue)
</dt> <dt>

[Übersicht über Windows-Animationen](scenic-animation-api-overview.md)
</dt> </dl>

 

 