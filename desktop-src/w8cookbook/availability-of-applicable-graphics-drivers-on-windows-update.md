---
title: Verfügbarkeit der anwendbaren Grafiktreiber auf Windows Update
description: Die Verfügbarkeit dieser Treiber auf Windows Update (Wu) bestimmt, ob einem Benutzer automatisch ein Upgrade von Windows 7, Windows 8 oder Windows 8.1 auf Windows 10 angeboten wird.
ms.assetid: 166C0FE3-CB9D-4895-91AC-6E57EC1D8B21
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 208e984199c8de63dfa49133a255865035c84bdd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341442"
---
# <a name="availability-of-applicable-graphics-drivers-on-windows-update"></a>Verfügbarkeit der anwendbaren Grafiktreiber auf Windows Update

Die Verfügbarkeit dieser Treiber auf Windows Update (Wu) bestimmt, ob einem Benutzer automatisch ein Upgrade von Windows 7, Windows 8 oder Windows 8.1 auf Windows 10 angeboten wird. Wenn in den Hardware Scans festgestellt wurde, dass auf Windows Update für den Grafikadapter des PCs kein Grafiktreiber verfügbar war, wurde den Benutzern das aktualisierte Windows 10-Betriebssystem nicht angeboten. Allerdings können Benutzer Windows 10 weiterhin durch andere Quellen abrufen und das Upgrade manuell durchführen.

Einige Benutzer waren nicht sicher, warum Ihnen das Upgrade nicht angeboten wurde, als andere Benutzer waren, obwohl der Upgrade Advisor erläuterte, dass kein Grafiktreiber für die Hardware verfügbar war.

Außerdem haben einige Benutzer ein Upgrade erzwungen und dann festgestellt, dass Ihre Grafik Funktionalität und Leistung aufgrund des Mangels an Hardware Treibern aufgetreten ist.

## <a name="mitigations"></a>Gegenmaßnahmen

Um dies zu vermeiden, können Benutzer einen älteren Treiber manuell installieren, d. h. von Windows 7, Windows 8 oder Windows 8.1, indem Sie die IHV-oder OEM-Website aufrufen und einen Treiber explizit herunterladen. Dies muss nach dem Upgrade erfolgen, und es ist nicht garantiert, dass es funktioniert. Es gibt keine unterstützte Lösung, wenn in Wu kein geeigneter Grafiktreiber verfügbar ist. Der Benutzer muss entscheiden, ob Folgendes erforderlich ist:

-   Auf dem vorherigen Betriebssystem verbleiben;
-   Akzeptieren Sie die Einschränkungen des Software Treibers, Microsoft Basic Display Adapter (msbda); noch
-   Erwerben Sie eine neue Grafikkarte, die über einen unterstützten Windows 10-Treiber verfügt.

## <a name="solutions"></a>Lösungen

Es ist wichtig, dass IHVs und OEMs Ihre Windows 10-Grafiktreiber für alle Hardware, die Sie unterstützen möchten, in Wu hochladen.

Beachten Sie, dass die Hardware, die das Ende der Live-(EOL) erreicht hat, möglicherweise keine Treiber auf Wu hat. In diesem Fall ist keine Lösung vorhanden – der Benutzer muss eine der Optionen unter entschärfungen oben auswählen.

 

 




