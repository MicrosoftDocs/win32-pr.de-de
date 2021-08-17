---
description: Ein interessantes neues Feature von Tablet PC ist das Stifteingabesystem.
ms.assetid: 8432617a-5ae7-44cb-a5f7-f3b2d8885846
title: Stifteingabe, Ink und Erkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8645a1a68499975ad3ef5cdafb8c07685e9ed9e600cdc9ca2129babaa8b953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716263"
---
# <a name="pen-input-ink-and-recognition"></a>Stifteingabe, Ink und Erkennung

Ein interessantes neues Feature von Tablet PC ist das Stifteingabesystem. Alle Tablet PC-Computer verfügen über einen Digitizer unterhalb des Bildschirms, der Stifteingaben akzeptiert. Dieser neue Eingabemechanismus erfordert, dass Sie überlegen, wie Sie Anwendungen speziell für Tablet PC erstellen. Die Api (Application Programming Interface) der Tablet PC-Plattform unterstützt Sie dabei.

## <a name="collection-data-management-and-recognition"></a>Sammlung, Datenverwaltung und Erkennung

Die Tablet PC-Plattform kann in drei verschiedene Bereiche unterteilt werden:

-   Ink-Auflistung (Objekte, die zum Sammeln von Ink aus dem Digitizer verwendet werden).
-   Verwaltung von Ink-Daten (Objekte, die zum Verwalten der gesammelten Ink verwendet werden).
-   Ink-Erkennung (Objekte, die verwendet werden, um die gesammelte Ink-Datei in andere Datentypen wie Text zu konvertieren).

Die folgende Abbildung zeigt auf hoher Ebene, wie die Ink Collection-API (Stift-API), die Ink-Datenverwaltung-API (Ink-API) und die Ink-Erkennungs-API (Erkennungs-API) auf der Tablet PC-Plattform zusammenarbeiten.

![illustrationon showing how pen api, ink api, and recognition api work together (Veranschaulichung der Zusammenarbeit von Stift-API, Ink-API und Erkennungs-API)](images/aabc298b-fd64-435b-87bc-eb7cd11524e8.jpg)

Die Tablet PC-Plattform-API ist sowohl in verwalteten APIs als auch in einer COM-Bibliothek verfügbar. Die folgenden Themen beschreiben die Objekte in der API und veranschaulichen, wie Anwendungen diese Objekte verwenden:

-   [Ink-Sammlung](ink-collection.md)
-   [Ink-Daten](ink-data.md)
-   [Ink-Erkennung](ink-recognition.md)
-   [Ink-Analyse](ink-analysis.md)
-   [Handschrifterkennung in Windows Server 2008 R2](handwriting-recognition-in-windows-server-2008-r2.md)

 

 



