---
title: Konstanten (Windows Animationsreferenz)
description: Referenzdokumentation für Konstanten und Enumerationen, die vom Animations-Manager Windows werden.
ms.assetid: c590cf68-28ce-4d7d-949d-2683ece3c12d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23964a2936b3879d551bcde9c2c25c2d63465e1cb4afb07cee25a3ce74a2a57f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419123"
---
# <a name="constants-windows-animation-reference"></a>Konstanten (Windows Animationsreferenz)

Referenzdokumentation für Konstanten und Enumerationen, die vom Animations-Manager Windows werden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                             | Beschreibung                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BENUTZEROBERFLÄCHENANIMATION \_ DIMENSION \_ UNKNOWN**](ui-animation-dimension-unknown.md)<br/>                                            | Gibt an, dass die angeforderte Dimension nicht abgerufen werden kann.<br/>                                                                                                                                                                                                     |
| [**KEINE ITERATION \_ DER \_ BENUTZEROBERFLÄCHENANIMATION \_**](-ui-animation-iteration-none.md)<br/>                                                 | Gibt an, dass dies der erste Eintrag in einer angegebenen Schleife ist.<br/>                                                                                                                                                                                                     |
| [**UI \_ ANIMATION \_ KEYFRAME \_ STORYBOARD \_ START**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85))<br/>                           | Stellt den impliziten Keyframe am Anfang jedes Storyboards dar.<br/>                                                                                                                                                                                              |
| [**\_ \_ BENUTZEROBERFLÄCHENANIMATION \_ WIRD UNBEGRENZT WIEDERHOLT**](ui-animation-repeat-indefinitely.md)<br/>                                        | Gibt an, dass das Intervall zwischen zwei Keyframes in einem Storyboard unbegrenzt wiederholt werden soll, bis die [**IUIAnimationStoryboard::Conclude-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) aufgerufen wird.<br/>                                                            |
| [**\_ \_ BENUTZEROBERFLÄCHENANIMATION \_ WIRD UNBEGRENZT AM ENDE \_ \_ \_ WIEDERHOLT**](ui-animation-repeat-indefinitely-conclude-at-end.md)<br/>     | Gibt an, dass das Intervall zwischen zwei Keyframes in einem Storyboard unbegrenzt wiederholt werden soll, bis die Keyframe-Schleife im endenden Keyframe beendet wird, wenn die [**IUIAnimationStoryboard::Conclude-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) aufgerufen wird.<br/>   |
| [**\_ \_ BENUTZEROBERFLÄCHENANIMATION \_ WIRD UNBEGRENZT BEIM START \_ \_ \_ WIEDERHOLT**](ui-animation-repeat-indefinitely-conclude-at-start.md)<br/> | Gibt an, dass das Intervall zwischen zwei Keyframes in einem Storyboard unbegrenzt wiederholt werden soll, bis die Keyframeschleife beim Aufrufen der [**IUIAnimationStoryboard::Conclude-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) auf dem Startschlüsselrahmen beendet wird.<br/> |
| [**\_ \_ BENUTZEROBERFLÄCHENANIMATION IN SEKUNDEN \_**](ui-animation-seconds-eventually.md)<br/>                                          | Gibt an, Windows Animation den geplanten Start eines Storyboards so lange wie nötig verzögern kann, um Planungskonflikte zu vermeiden.<br/>                                                                                                                     |
| [**\_BENUTZEROBERFLÄCHENANIMATION \_ SEKUNDEN \_ UNENDLICH**](ui-animation-seconds-infinite.md)<br/>                                              | Gibt an, dass keine geplanten Ereignisse sind.<br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Animationsreferenz](windows-animation-reference.md)
</dt> </dl>

 

