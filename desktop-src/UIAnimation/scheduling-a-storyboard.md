---
title: Planen eines Storyboards
description: Nachdem ein Storyboard erstellt wurde, wird es vom Animations-Manager geplant.
ms.assetid: f3c8fe34-8bca-4421-a390-9e0ba9af27b4
keywords:
- Storyboards Windows-Animation, Planung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3feae253804d20711c9bbd8ed50895f43272a3f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036403"
---
# <a name="schedule-a-storyboard"></a>Planen eines Storyboards

Nachdem ein Storyboard erstellt wurde, wird es vom Animations-Manager geplant.

## <a name="overview"></a>Übersicht

Standardmäßig wird jedes Storyboard sofort nach der Planung gestartet. Dies bedeutet, dass beim Starten einer oder mehrerer Variablen durch ein Storyboard möglicherweise alle anderen Storyboards, die dieselben Variablen animieren, unterbrochen werden. Allerdings kann eine Anwendung andere Verhalten angeben, indem die relative Priorität zwischen Storyboards festgelegt wird.

Nachdem ein Storyboard geplant wurde, kann es nicht mehr geändert werden. Nachdem ein Storyboard aus dem Zeitplan entfernt wurde, kann es jedoch wiedergegeben werden. Entwickler sollten bei der erneuten Verwendung von Storyboards Vorsicht walten lassen, da dies nur dann der Fall sein sollte, wenn es nicht möglich ist, dass das gleiche Storyboard aufgrund einer Benutzeraktion in die Warteschlange eingereiht werden muss, wenn Sie bereits im Zeitplan vorhanden ist oder in die Warteschlange eingereiht wurde.

## <a name="example-code"></a>Beispielcode

Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" in den Windows-Animations Beispielen [Anwendungs gesteuerte Animation](application-driven-animation-sample.md) und [Timer-gesteuerte Animation](timer-driven-animation-sample.md). Er verwendet die [**iuianimationstoryboard:: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) -Methode, um das Storyboard zu planen. Diese Methode erfordert die aktuelle Zeit als Parameter.


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

Bevor Sie mit diesem Schritt beginnen, sollten Sie diesen Schritt abgeschlossen haben: [Erstellen eines Storyboards und hinzufügen](updating---timer-driven-animation.md)von Übergängen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iuianimationstoryboard:: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule)
</dt> <dt>

[**Iuianimationtimer:: getTime**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[Übersicht über Storyboards](storyboard-construction.md)
</dt> </dl>

 

 




