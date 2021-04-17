---
description: Ein interessantes neues Feature von Tablet PC ist das Stift Eingabe System.
ms.assetid: 8432617a-5ae7-44cb-a5f7-f3b2d8885846
title: Stift Eingabe, frei Hand Eingabe und-Erkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a46d865e40d1779edaa2607b1754c45659609b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558705"
---
# <a name="pen-input-ink-and-recognition"></a>Stift Eingabe, frei Hand Eingabe und-Erkennung

Ein interessantes neues Feature von Tablet PC ist das Stift Eingabe System. Alle Tablet PC-Computer verfügen unter dem Bildschirm über einen Digitalisierer, der Stift Eingaben akzeptiert. Dieser neue Eingabe Mechanismus erfordert, dass Sie sich Gedanken über das Erstellen von Anwendungen speziell für Tablet PC machen müssen. Die Tablet PC Platform-API (Application Programming Interface) hilft Ihnen dabei, dies zu tun.

## <a name="collection-data-management-and-recognition"></a>Erfassung, Datenverwaltung und Erkennung

Die Tablet PC-Plattform kann in drei verschiedene Bereiche unterteilt werden:

-   Ink-Auflistung (Objekte, die verwendet werden, um frei Hand Eingaben vom Digitalisierer zu erfassen).
-   Frei Hand Datenverwaltung (Objekte, die zum Verwalten der gesammelten frei Hand Eingaben verwendet werden).
-   Frei Handerkennung (-Objekte, die zum Konvertieren der gesammelten frei Hand Eingaben in andere Datentypen verwendet werden, z. b. Text).

Die folgende Abbildung zeigt, wie die frei Hand Sammlungs-API (Pen API), die frei Hand Datenverwaltung-API (Ink-API) und die frei Hand Erkennungs-API (Erkennungs-API) auf der Tablet PC-Plattform zusammenarbeiten.

![illustraton zeigt, wie die Stift-API, die frei Hand-API und die Erkennungs-API zusammenarbeiten](images/aabc298b-fd64-435b-87bc-eb7cd11524e8.jpg)

Die Tablet PC Platform-API ist sowohl in verwalteten APIs als auch in einer COM-Bibliothek verfügbar. In den folgenden Themen werden die Objekte in der API beschrieben und veranschaulicht, wie Anwendungen diese Objekte verwenden:

-   [Ink-Auflistung](ink-collection.md)
-   [Frei Hand Daten](ink-data.md)
-   [Frei Handerkennung](ink-recognition.md)
-   [Ink-Analyse](ink-analysis.md)
-   [Handschrifterkennung in Windows Server 2008 R2](handwriting-recognition-in-windows-server-2008-r2.md)

 

 



