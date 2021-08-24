---
description: Um den Geräteereignistyp bei der Verarbeitung einer WM DEVICECHANGE-Nachricht zu \_ bestimmen, überprüfen Sie den wParam-Parameter.
ms.assetid: 17078548-879d-4a11-a268-27d1f30180ab
title: Geräteereignistypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4d807cd7524d1906e86113c546306e08051ea80770900d42c1233364430e22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636640"
---
# <a name="device-event-types"></a>Geräteereignistypen

Um den Geräteereignistyp bei der Verarbeitung einer [**WM \_ DEVICECHANGE-Nachricht**](wm-devicechange.md) zu bestimmen, überprüfen Sie den *wParam-Parameter.* Der Wert von *wParam* bestimmt die Bedeutung der ereignisspezifischen Daten im *lParam-Parameter.* Im Allgemeinen identifizieren die ereignisspezifischen Daten das Gerät und bieten zusätzliche Details zum Ereignis. Das Format dieser Daten hängt vom Gerätetyp ab, aber die ersten Bytes haben immer das gleiche Format wie die [**\_ DEV \_ BROADCAST-HDR-Struktur.**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) Um das Format der Daten zu bestimmen, überprüfen Sie den **dbch \_ devicetype-Member.**

Das System überträgt ein Geräteereignis vom Typ [DBT \_ DEVICEARRARR (d.](dbt-devicearrival.md) h. eine [**WM \_ DEVICECHANGE-Nachricht,**](wm-devicechange.md) bei der *wParam* auf DBT DEVICEARRARR FESTGELEGT ist), wenn ein Gerät eingefügt wurde und zur Verwendung \_ verfügbar ist. Anwendungen überprüfen in der Regel den Gerätetyp und beginnen sofort, das Gerät zu verwenden, wenn es geeignet ist.

Das System sendet ein [DBT \_ DEVICEQUERYREMOVE-Geräteereignis,](dbt-devicequeryremove.md) um die Berechtigung zum Entfernen eines Geräts an fordern. Um zu bestimmen, ob das Gerät benötigt wird, kann eine Anwendung ein Dialogfeld anzeigen, in dem der Benutzer zur Eingabe von Anweisungen aufgefordert wird. Wenn eine Anwendung feststellt, dass sie das Gerät benötigt, kann sie diese Anforderung verweigern und die Entfernung abbrechen, indem sie BROADCAST \_ QUERY \_ DENY zurücksendet. Wenn die Anwendung das Gerät nicht benötigt, muss sie **TRUE zurückgeben.** Das System sendet sofort eine [DBT \_ DEVICEQUERYREMOVEFAILED-Nachricht,](dbt-devicequeryremovefailed.md) wenn eine Anwendung oder ein Treiber eine vorherige Anforderung zum Entfernen eines Geräts abgebrochen hat.

Das System sendet ein [DBT \_ DEVICEREMOVEPENDING-Geräteereignis](dbt-deviceremovepending.md) als letzte Warnung, bevor ein Gerät entfernt wird. An diesem Punkt kann die Anwendung die Entfernung nicht abbrechen. Wenn sie also das Gerät verwendet, muss sie sich auf die Entfernung vorbereiten, um Datenverluste zu verhindern. Dies ist besonders wichtig, wenn eine Netzwerkverbindung entfernt wird. Die Anwendung muss bestimmen, ob sich eine der geöffneten Dateien oder Pipes in dieser Verbindung befinden. Hierzu kann der Netzwerkressourcenbezeichner in den ereignisspezifischen Daten der Nachricht mit den Ressourcenbezeichnern verglichen werden, die zuvor für die Dateien und Pipes ermittelt wurden. Das System sendet ein [DBT \_ DEVICEREMOVECOMPLETE-Geräteereignis,](dbt-deviceremovecomplete.md) wenn ein Gerät entfernt wurde und nicht mehr verfügbar ist.

Das System überträgt ein [DBT \_ QUERYCHANGECONFIG-Geräteereignis,](dbt-querychangeconfig.md) um die Berechtigung zum Ändern der aktuellen Konfiguration (Dock oder Abdocken) an fordern. Jede Anwendung kann BROADCAST \_ QUERY \_ DENY zurückgeben, um die Anforderung zu verweigern und die Änderung abzubruchen. Wenn eine Anwendung die Anforderung verweigert, sendet das System eine [DBT \_ CONFIGCHANGECANCELED-Nachricht.](dbt-configchangecanceled.md) Wenn sich die aktuelle Konfiguration aufgrund eines Andocks oder Abdockens geändert hat, sendet das System eine [DBT \_ CONFIGCHANGED-Nachricht.](dbt-configchanged.md)

Das System sendet immer dann [ein DBT \_ DEVICETYPESPECIFIC-Geräteereignis,](dbt-devicetypespecific.md) wenn ein gerätespezifisches Ereignis auftritt.

Treiber können eigene benutzerdefinierte Ereignistypen erstellen. Benutzerdefinierte Ereignisse werden nur an Anwendungen gesendet, die für Geräteereignisbenachrichtigungen auf einem bestimmten Gerät registriert sind und nur von Kernelmodustreibern initiiert werden können. Weitere Informationen finden Sie unter [DBT \_ CUSTOMEVENT](dbt-customevent.md).

 

 



