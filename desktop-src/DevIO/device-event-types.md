---
description: Über \_ prüfen Sie den wParam-Parameter, um den Geräte Ereignistyp bei der Verarbeitung einer WM-devicechange-Nachricht zu ermitteln.
ms.assetid: 17078548-879d-4a11-a268-27d1f30180ab
title: Geräte Ereignis Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35ece6b810ba4d1310638bbfbdcdcaa7f67f79d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041429"
---
# <a name="device-event-types"></a>Geräte Ereignis Typen

Überprüfen Sie den *wParam* -Parameter, um den Geräte Ereignistyp bei der Verarbeitung einer [**WM- \_ devicechange**](wm-devicechange.md) -Nachricht zu ermitteln. Der Wert von *wParam* bestimmt die Bedeutung der ereignisspezifischen Daten im *LPARAM* -Parameter. Im Allgemeinen wird das Gerät von den ereignisspezifischen Daten identifiziert, und es werden weitere Details zum Ereignis bereitstellt. Das Format dieser Daten hängt vom Gerätetyp ab, aber die ersten Bytes haben immer das gleiche Format wie die HDR-Struktur von [**dev \_ Broadcast \_**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) . Um das Format der Daten zu bestimmen, überprüfen Sie das **dbch \_ den DeviceType "** -Element.

Das System überträgt ein Geräte Ereignis vom Typ [DBT \_ devicearrival (d](dbt-devicearrival.md) . h. eine [**WM- \_ devicechange**](wm-devicechange.md) -Nachricht, bei der *wParam* auf DBT \_ devicearrival festgelegt ist), wenn ein Gerät eingefügt und zur Verwendung verfügbar ist. Anwendungen überprüfen in der Regel den Gerätetyp und beginnen sofort mit der Verwendung des Geräts.

Das System überträgt ein [DBT \_ DeviceQueryRemove](dbt-devicequeryremove.md) -Geräte Ereignis, um die Berechtigung zum Entfernen eines Geräts anzufordern. Um zu ermitteln, ob das Gerät benötigt wird, kann eine Anwendung ein Dialogfeld anzeigen, um den Benutzer zur Eingabe von Anweisungen aufzufordern. Wenn eine Anwendung ermittelt, dass Sie das Gerät benötigt, kann Sie diese Anforderung verweigern und das Entfernen abbrechen, indem Broadcast Query Deny zurückgegeben wird \_ \_ . Wenn die Anwendung das Gerät nicht benötigt, muss Sie " **true**" zurückgeben. Das System sendet sofort eine [DBT \_ devicequeryremovefailed](dbt-devicequeryremovefailed.md) -Nachricht, wenn eine Anwendung oder ein Treiber eine vorherige Anforderung zum Entfernen eines Geräts abgebrochen hat.

Das System überträgt ein [DBT \_ deviceremovepend](dbt-deviceremovepending.md) -Geräte Ereignis als letzte Warnung, bevor ein Gerät entfernt wird. An diesem Punkt kann die Anwendung die Entfernung nicht abbrechen, d. h., wenn Sie das Gerät verwendet, muss Sie die Entfernung vorbereiten, um Datenverluste zu verhindern. Dies ist besonders wichtig, wenn eine Netzwerkverbindung entfernt wird. Die Anwendung muss bestimmen, ob eine Ihrer geöffneten Dateien oder Pipes über diese Verbindung verfügt. Hierzu kann der Netzwerkressourcen Bezeichner in den ereignisspezifischen Daten der Nachricht mit den Ressourcen Bezeichnern verglichen werden, die zuvor für die Dateien und Pipes abgerufen wurden. Das System überträgt ein [DBT \_ deviceremovecomplete](dbt-deviceremovecomplete.md) -Geräte Ereignis, wenn ein Gerät entfernt wurde und nicht mehr verfügbar ist.

Das System überträgt ein [DBT \_ querychangeconfig](dbt-querychangeconfig.md) -Geräte Ereignis, um die Berechtigung zum Ändern der aktuellen Konfiguration (Andocken oder Abdocken) anzufordern. Jede Anwendung kann die Übertragungs \_ Abfrage \_ ablehnen zurückgeben, um die Anforderung zu verweigern und die Änderung abzubrechen. Wenn eine Anwendung die Anforderung ablehnt, sendet das System eine [DBT \_ configchangeabgeb Rochen](dbt-configchangecanceled.md) -Nachricht. Wenn sich die aktuelle Konfiguration aufgrund eines Andocken oder abdostems geändert hat, sendet das System eine [DBT \_ ConfigChanged](dbt-configchanged.md) -Nachricht.

Das System überträgt immer dann ein [DBT \_ -](dbt-devicetypespecific.md) Geräte Ereignis, wenn ein Geräte spezifisches Ereignis auftritt.

Treiber können eigene benutzerdefinierte Ereignis Typen erstellen. Benutzerdefinierte Ereignisse werden nur an eine Anwendung gesendet, die auf einem bestimmten Gerät für die Benachrichtigung über Geräte Ereignisse registriert ist, und können nur von Kernelmodustreibern initiiert werden. Weitere Informationen finden Sie unter [DBT \_ CustomEvent](dbt-customevent.md).

 

 



