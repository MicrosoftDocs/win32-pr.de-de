---
title: Funktionen (Touch-Treffertests)
description: Die Themen in diesem Abschnitt enthalten die Referenzspezifikationen für Touch-Treffertestfunktionen.
ms.assetid: C7275A12-4F76-485D-896F-3CCB8CE92F8E
keywords:
- Benutzereingriff
- input
- Zeiger
- Toucheingabe
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 83ab93fbff031423b6478926e499077ac78b1aec686d596ca069fda6d1b2298b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118248357"
---
# <a name="touch-hit-testing-functions"></a>Touch-Treffertestfunktionen

Die Themen in diesem Abschnitt enthalten die Referenzspezifikationen für [Touch-Treffertestfunktionen.](functions.md)

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
| --- | --- |
| [**EvaluateProximityToPolygon**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytopolygon)<br/> | Gibt die Bewertung eines Polygons als wahrscheinliches Berührungsziel (im Vergleich zu allen anderen Polygonen, die den Berührungskontaktbereich überschneiden) und einen angepassten Berührungspunkt innerhalb des Polygons zurück. <br/> |
| [**EvaluateProximityToRect**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytorect)<br/> | Gibt die Bewertung eines Rechtecks als wahrscheinliches Berührungsziel im Vergleich zu allen anderen Rechtecke, die den Berührungskontaktbereich überschneiden, und einen angepassten Berührungspunkt innerhalb des Rechtecks zurück. <br/> |
| [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)<br/> | Gibt die Näherungsauswertungsbewertung und die angepassten Touchpunktkoordinaten als gepackten Wert für den [WM_TOUCHHITTESTING Nachrichtenrückruf](../inputmsg/wm-touchhittesting.md) zurück. <br/> |
| [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)<br/> | Registriert ein Fenster zum Verarbeiten der [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) Benachrichtigung.<br/> |

## <a name="related-topics"></a>Zugehörige Themen

[Referenz zu Touchtreffertests](touchhittest-reference.md)
