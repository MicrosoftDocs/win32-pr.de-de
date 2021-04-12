---
title: Direct2D debugschicht
description: Eine Lauf Zeit Erweiterung für Direct2D, die beschreibende Fehlermeldungen, Erkennung von Objekt Lecks, Leistungs Hinweise und andere Hinweise bietet, die Sie beim Erstellen von Direct2D-apps unterstützen.
ms.assetid: 23b522d4-0733-4892-b93d-28f899fa0f17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f71b1364e645859059fb090634cbdae6f8c084e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388046"
---
# <a name="direct2d-debug-layer"></a>Direct2D debugschicht

## <a name="purpose"></a>Zweck

Die Direct2D-debugschicht, die separat von Direct2D in der eigenen dll mit dem Namen d2d1debug.dll implementiert wurde, stellt Entwurfszeit-Debugmeldungen bereit, um den Lauf Zeit Anwendungsfehler zu minimieren Die Debugmeldungen resultieren häufig aus Verstößen gegen API-Verträge, wie z. b. ungültige Parameter (Direct3D-bezogen), ungültigen Ressourcen, Threading Verstößen und anderen Leistungsproblemen, wie z. b. der Verwendung einer Ebene, wenn ein Clip ausreichen würde.

Um Ihnen bei der Entscheidung zu helfen, wie viele Informationen von der debugschicht verfolgt werden, bietet die debugschicht drei debugebenen: Information, Warnung und Fehler. Diese drei Ebenen werden wie folgt interpretiert:

-   **Fehler:** Direct2D sendet schwerwiegende Fehlermeldungen an die debugschicht. Beispielsweise wird durch das Unterbrechen einer Threading Einschränkung ein schwerwiegender Fehler generiert.

    Außerdem löst eine Meldung vom Typ Fehler den Haltepunkt aus, um Sie beim Debuggen zu unterstützen.

-   **Warnung:** Direct2D sendet Fehlermeldungen und Warnungen an die debugschicht, damit Sie diese Nachrichten adressieren können.

-   **Informationen:** Direct2D sendet Fehlermeldungen, Warnungen und zusätzliche Diagnoseinformationen an die debugschicht. Beispielsweise werden Meldungen zur Leistungsverbesserung auf dieser Debugebene gesendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                     | BESCHREIBUNG                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Installieren der Direct2D Debug-Ebene](installing-the-direct2d-debug-layer.md)<br/> | Beschreibt, wie die Direct2D-debugschicht installiert wird.<br/>      |
| [Direct2D Übersicht über die Debug-Ebene](direct2ddebuglayer-overview.md)<br/>               |                                                                    |
| [Debugmeldungen](direct2ddebuglayer-debugmessages.md)<br/>                         | Listet die Debugmeldungen von der Direct2D Debug-Ebene auf.<br/> |



 

 

 





