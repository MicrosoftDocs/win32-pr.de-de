---
title: Direct2D-Debugebene
description: Eine Laufzeiterweiterung für Direct2D, die beschreibende Fehlermeldungen, Objektverlusterkennung, Leistungshinweise und andere Hinweise zum Erstellen von Direct2D-Apps bietet.
ms.assetid: 23b522d4-0733-4892-b93d-28f899fa0f17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29cb01c2f8f4f4b14694da94262847ae0def0817a13ffffc48f5c414a8eacda7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044360"
---
# <a name="direct2d-debug-layer"></a>Direct2D-Debugebene

## <a name="purpose"></a>Zweck

Die Direct2D-Debugebene, die separat von Direct2D in einer eigenen DLL mit dem Namen d2d1debug.dll implementiert wird, stellt Debugmeldungen zur Entwurfszeit bereit, mit deren Hilfe Sie Laufzeitanwendungsfehler minimieren können. Die Debugmeldungen resultieren häufig aus Verstößen gegen API-Verträge, z. B. ungültige Parameter (kann direct3D-bezogen sein), ungültige Ressourcen, Threadingverletzungen und andere Leistungsprobleme wie die Verwendung einer Ebene, wenn ein Clip ausreichen würde.

Damit Sie entscheiden können, wie viele Informationen von der Debugschicht nachverfolgt werden, bietet die Debugebene drei Debugebenen: Informationen, Warnungen und Fehler. Diese drei Ebenen werden wie folgt interpretiert:

-   **Fehler:** Direct2D sendet schwerwiegende Fehlermeldungen an die Debugebene. Wenn Sie z. B. eine Threadingeinschränkung aufbrechen, wird ein schwerwiegender Fehler generiert.

    Darüber hinaus löst eine Meldung vom Levelfehler den Haltepunkt aus, um Sie beim Debuggen zu unterstützen.

-   **Warnung:** Direct2D sendet Fehlermeldungen und Warnungen an die Debugebene, damit Sie diese Meldungen beheben können.

-   **Informationen:** Direct2D sendet Fehlermeldungen, Warnungen und zusätzliche Diagnoseinformationen an die Debugebene. Beispielsweise werden Meldungen zur Leistungsverbesserung auf dieser Debugebene gesendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                     | BESCHREIBUNG                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Installieren der Direct2D-Debugebene](installing-the-direct2d-debug-layer.md)<br/> | Beschreibt, wie die Direct2D-Debugebene installiert wird.<br/>      |
| [Übersicht über Direct2D-Debugebenen](direct2ddebuglayer-overview.md)<br/>               |                                                                    |
| [Debugmeldungen](direct2ddebuglayer-debugmessages.md)<br/>                         | Listet die Debugmeldungen von der Direct2D-Debugebene auf.<br/> |



 

 

 





