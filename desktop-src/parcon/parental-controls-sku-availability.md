---
description: Verfügbarkeit der SKU "Jugendschutz"
ms.assetid: 5fbf6c4a-3897-4a12-bef6-19478fdb48aa
title: Verfügbarkeit der SKU "Jugendschutz"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21184a383a28e3ae06198f203475c1c03334e5d678278bbb3b4988b52971e79e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461200"
---
# <a name="parental-controls-sku-availability"></a>Verfügbarkeit der SKU "Jugendschutz"

Die in diesem Abschnitt beschriebenen Benutzeroberflächen, Features und APIs für Die Jugendschutzfunktionen sind derzeit nur für kundenorientierte SKUs verfügbar, z. B.:

-   Windows Vista Starter
-   Windows Vista Home Basic
-   Windows Vista Home Premium
-   Windows Vista Ultimate

Die Jugendschutzelemente werden nur auf diesen SKUs installiert. Lösungen, für die eine Bereitstellung in Geschäfts-SKUs erforderlich ist, müssen eine der beiden voraussetzungen:

-   Erkennen sie die Funktionen für die Jugendschutzfunktionen für Geschäfts-SKUs, und stellen Sie sie nicht bereit.
-   Erkennen und Bereitstellen einer alternativen Möglichkeit für Konfiguration, Protokollierung und Einschränkungen.

Es wird empfohlen, dass Lösungen die Verfügbarkeit der Infrastruktur für die Jugendschutzfunktionen erkennen, indem sie überprüfen, ob COM CoCreateInstance in der Konformitäts-API erfolgreich ist.

Anwendungen mit Jugendschutz, die von der Windows Vista-Infrastruktur abhängig sind, möchten möglicherweise auch eine eigene Benutzeroberfläche unterdrücken, die Einstellungen oder andere Funktionen verfügbar macht, wenn die Benutzeroberfläche der Jugendschutzfunktionen in einer unterstützten SKU unterdrückt wird. Eine Funktion wird für die Sichtbarkeitsermittlung bereitgestellt, die Fälle wie die Unterdrückung in eine Domäne abdeckt.

 

 



