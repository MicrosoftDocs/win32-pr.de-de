---
title: Verfügbarkeit anwendbarer Grafiktreiber bei Windows Update
description: Die Verfügbarkeit dieser Treiber auf Windows Update (WU) bestimmt, ob einem Benutzer automatisch ein Upgrade von Windows 7, Windows 8 oder Windows 8.1 auf Windows 10 angeboten wird.
ms.assetid: 166C0FE3-CB9D-4895-91AC-6E57EC1D8B21
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 906894f317a86d851501e913e3c9491dc1f83336f7f80eefa660ee43d3510b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935430"
---
# <a name="availability-of-applicable-graphics-drivers-on-windows-update"></a>Verfügbarkeit anwendbarer Grafiktreiber bei Windows Update

Die Verfügbarkeit dieser Treiber auf Windows Update (WU) bestimmt, ob einem Benutzer automatisch ein Upgrade von Windows 7, Windows 8 oder Windows 8.1 auf Windows 10 angeboten wird. Wenn hardwarescans zeigten, dass auf Windows Update für den Grafikadapter auf dem PC kein Grafiktreiber verfügbar war, wurde benutzern das aktualisierte Windows 10 Betriebssystem nicht angeboten. Benutzer können jedoch weiterhin Windows 10 über andere Quellen abrufen und das Upgrade manuell ausführen.

Einige Benutzer waren sich nicht sicher, warum ihnen das Upgrade nicht angeboten wurde, als es andere Personen waren, obwohl die Aktualisierungsratgeber erklärt haben, dass kein Grafiktreiber für ihre Hardware verfügbar war.

Darüber hinaus haben einige Benutzer ein Upgrade erzwungen und dann festgestellt, dass ihre Grafikfunktionalität und -leistung aufgrund eines fehlenden Hardwaretreibers nicht funktionierten.

## <a name="mitigations"></a>Gegenmaßnahmen

Um dies zu vermeiden, können Benutzer manuell einen älteren Treiber installieren, d. h. von Windows 7, Windows 8 oder Windows 8.1, indem sie zur IHV- oder OEM-Website gehen und einen Treiber explizit herunterladen. Dies muss nach dem Upgrade erfolgen und funktioniert nicht garantiert. Es gibt keine unterstützte Lösung, wenn auf WU kein geeigneter Grafiktreiber verfügbar ist. Der Benutzer muss entscheiden, ob Folgendes zu beachten ist:

-   Verbleiben Sie auf dem vorherigen Betriebssystem.
-   Akzeptieren Sie die Einschränkungen des Softwaretreibers Microsoft Basic Display Adapter (MSBDA). Oder
-   Erwerben Sie eine neue Grafikkarte, die über einen unterstützten Windows 10-Treiber verfügt.

## <a name="solutions"></a>Lösungen

Es ist wichtig, dass IHVs und OEMs ihre Windows 10 Grafiktreiber für jede Hardware, die sie unterstützen möchten, auf WU hochladen.

Beachten Sie, dass Hardware, die das Ende des Live-Geräts (End-Of-Live, EOL) erreicht hat, möglicherweise keine Treiber auf WU hat. In diesem Fall gibt es keine Lösung: Der Benutzer muss eine der Optionen unter Entschärfungen oben auswählen.

 

 




