---
title: Treffertest-Rückgabewerte
description: In diesem Abschnitt werden die Treffertestcodewerte aufgeführt, die im pwHitTestCode-Parameter der HitTestThemeBackground-Funktion zurückgegeben werden.
ms.assetid: 95b4fc1a-2f9b-4464-b672-552d36b60c42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020765e6f766efc2c79e869a1b06cfceac2c13a451cc381d88ae066cc1478c11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797600"
---
# <a name="hit-test-return-values"></a>Treffertest-Rückgabewerte

In diesem Abschnitt werden die Treffertestcodewerte aufgeführt, die im *pwHitTestCode-Parameter* der [**HitTestThemeBackground-Funktion zurückgegeben**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground) werden. Die zurückgegebenen Codewerte hängen von den Treffertestoptionen ab, die im *dwOptions-Parameter* der **HitTestThemeBackground-Funktion angegeben** sind. Eine Liste der Optionen finden Sie unter [Treffertestoptionen.](theme-hit-test-options.md)

## <a name="return-values"></a>Rückgabewerte

In der folgenden Tabelle sind die Treffertestoptionen und die entsprechenden Rückgabecodes aufgeführt.



| Option                       | Rückgabecodes  | Beschreibung                                                                                                        |
|------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------|
| HTTB \_ BACKGROUNDSEG          | HTBOTTOM      | Der Treffertest war im unteren Rahmensegment erfolgreich.                                                                   |
|                              | HTBOTTOMLEFT  | Der Treffertest war in der unteren und linken Rahmenüberschnittmenge erfolgreich.                                                     |
|                              | HTBOTTOMRIGHT | Der Treffertest war am unteren und rechten Rand erfolgreich.                                                    |
|                              | HTCLIENT      | Der Treffertest war im mittleren Hintergrundsegment erfolgreich.                                                               |
|                              | HTLEFT        | Der Treffertest war im linken Rahmensegment erfolgreich.                                                                     |
|                              | HTNOWHERE     | Der Treffertest war außerhalb des Steuerelements oder in einem transparenten Bereich erfolgreich.                                                   |
|                              | HTRIGHT       | Der Treffertest war im rechten Rahmensegment erfolgreich.                                                                    |
|                              | HTTOP         | Der Treffertest war im oberen Rahmensegment erfolgreich.                                                                      |
|                              | HTTOPLEFT     | Der Treffertest war in der Schnittmenge des oberen und linken Rahmens erfolgreich.                                                            |
|                              | HTTOPRIGHT    | Der Treffertest war am oberen und rechten Rand erfolgreich.                                                       |
| HTTB \_ CAPTION                | BESENAPTION     | Der Treffertest war in den Hintergrundsegmenten oben links oder oben rechts erfolgreich.                                         |
|                              | HTNOWHERE     | Der Treffertest war außerhalb des Steuerelements oder in einem transparenten Bereich erfolgreich.                                                   |
| HTTB \_ FIXEDBORDER            | HTBORDER      | Der Treffertest war in jedem Hintergrundsegment mit Ausnahme des mittleren Hintergrundsegments erfolgreich.                                 |
|                              | HTCLIENT      | Der Treffertest war im mittleren Hintergrundsegment erfolgreich.                                                               |
| HTTB \_ RESIZINGBORDER         | HTBORDER      | Fehler beim Treffertest im mittleren Hintergrundsegment und beim Ändern der Größe von Zonen, aber erfolgreich in einem Hintergrund-Rahmensegment. |
| HTTB \_ RESIZINGBORDER \_ BOTTOM | HTBOTTOM      | Der Treffertest war im unteren Rahmensegment erfolgreich.                                                                   |
| HTTB \_ RESIZINGBORDER \_ LEFT   | HTLEFT        | Der Treffertest war im linken Rahmensegment erfolgreich.                                                                     |
| HTTB \_ RESIZINGBORDER \_ RIGHT  | HTRIGHT       | Der Treffertest war im rechten Rahmensegment erfolgreich.                                                                    |
| HTTB \_ RESIZINGBORDER \_ TOP    | HTTOP         | Der Treffertest war im oberen Rahmensegment erfolgreich.                                                                      |



 

 

 




