---
title: Planen eines Storyboards
description: Nachdem ein Storyboard erstellt wurde, wird es vom Animations-Manager geplant.
ms.assetid: f3c8fe34-8bca-4421-a390-9e0ba9af27b4
keywords:
- Storyboards Windows Animation , Planung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013adc114fd09f518c34bc15ca2e7799381b6cee3dfeeedaf3b26fcae6d506e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008170"
---
# <a name="schedule-a-storyboard"></a>Planen eines Storyboards

Nachdem ein Storyboard erstellt wurde, wird es vom Animations-Manager geplant.

## <a name="overview"></a>Übersicht

Standardmäßig wird jedes Storyboard sofort gestartet, wenn es geplant ist. Dies bedeutet, dass ein Storyboard, wenn es beginnt, eine oder mehrere Variablen zu animieren, alle anderen Storyboards unterbrechen kann, die dieselben Variablen animieren. Eine Anwendung kann jedoch andere Verhaltensweisen angeben, indem sie die relative Priorität zwischen Storyboards bestimmt.

Nachdem ein Storyboard geplant wurde, kann es nicht mehr geändert werden. Nachdem jedoch ein Storyboard aus dem Zeitplan entfernt wurde, kann es erneut für die Wiedergabe eingeplant werden. Entwickler sollten bei der erneuten Verwendung von Storyboards Vorsicht walten lassen, da dies nur erfolgen sollte, wenn es nicht möglich ist, dass dasselbe Storyboard aufgrund einer Benutzeraktion in die Warteschlange eingereiht werden muss, wenn es bereits im Zeitplan wiedergegeben oder in die Warteschlange eingereiht wird.

## <a name="example-code"></a>Beispielcode

Der folgende Beispielcode stammt aus MainWindow.cpp in den Beispielen Windows Animation [Application-Driven Animation](application-driven-animation-sample.md) und [Timer-Driven Animation](timer-driven-animation-sample.md). Sie verwendet die [**IUIAnimationStoryboard::Schedule-Methode,**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) um das Storyboard zu planen. Diese Methode erfordert die aktuelle Zeit als Parameter.


```
// Get the current time and schedule the storyboard for play

UI_ANIMATION_SECONDS secondsNow;
hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );
if (SUCCEEDED(hr))
{
    hr = pStoryboard->Schedule(
        secondsNow
    );
}
```



## <a name="previous-step"></a>Vorheriger Schritt

Bevor Sie mit diesem Schritt beginnen, sollten Sie diesen Schritt abgeschlossen haben: [Erstellen eines Storyboards und Hinzufügen von Übergängen.](updating---timer-driven-animation.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IUIAnimationStoryboard::Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule)
</dt> <dt>

[**IUIAnimationTimer::GetTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[Übersicht über Storyboards](storyboard-construction.md)
</dt> </dl>

 

 




