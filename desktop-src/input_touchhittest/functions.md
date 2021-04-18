---
title: Funktionen (Berührungs Treffer Tests)
description: Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für Berührungs Treffer-Testfunktionen.
ms.assetid: C7275A12-4F76-485D-896F-3CCB8CE92F8E
keywords:
- Benutzereingriff
- input
- Zeiger
- Toucheingabe
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 03fcb4fb3fbe4f56e288703316f4b6e3ff02bba4
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "106365443"
---
# <a name="touch-hit-testing-functions"></a>Funktionen für Berührungs Treffer Tests

Die Themen in diesem Abschnitt enthalten die Referenz Spezifikationen für [Berührungs Treffer-Testfunktionen](functions.md).

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
| --- | --- |
| [**Evaluateproximitytopolygon**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytopolygon)<br/> | Gibt das Ergebnis eines Polygone als wahrscheinliches Berührungs Ziel (im Vergleich zu allen anderen Polygonen, die den Berührungs Kontaktbereich überschneiden) und einen angepassten Berührungspunkt innerhalb des Polygone zurück. <br/> |
| [**Evaluateproximitytor**](/windows/win32/api/winuser/nf-winuser-evaluateproximitytorect)<br/> | Gibt das Ergebnis eines Rechtecks als wahrscheinliches Berührungs Ziel zurück, verglichen mit allen anderen Rechtecke, die den Berührungs Kontaktbereich überschneiden, und einem angepassten Berührungspunkt innerhalb des Rechtecks. <br/> |
| [**Packtouchhittestingproximityevaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)<br/> | Gibt das Näherungs Bewertungsergebnis und die angepassten Berührungspunkt Koordinaten als einen gepackten Wert für den [WM_TOUCHHITTESTING Nachrichten](../inputmsg/wm-touchhittesting.md) Rückruf zurück. <br/> |
| [**Registertouchhittestingwindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow)<br/> | Registriert ein Fenster zur Verarbeitung der [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) Benachrichtigung.<br/> |

## <a name="related-topics"></a>Zugehörige Themen

[Referenz zu Berührungs Treffer Tests](touchhittest-reference.md)
