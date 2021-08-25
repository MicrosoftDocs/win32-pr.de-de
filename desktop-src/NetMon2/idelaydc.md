---
description: Die IDelaydC-Schnittstelle stellt die Methoden bereit, die zum Herstellen einer Verbindung mit dem Netzwerk, zum Erfassen des Netzwerkdatenverkehrs zu einer Erfassungsdatei, zum Abrufen von Statistiken und zum Trennen der Verbindung mit dem Netzwerk verwendet werden.
ms.assetid: ab275653-2377-4af6-a810-48515962c88c
title: IDelaydC-Schnittstelle (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1b6b965990435dd7b9a1758cc9bf8ac8001c747ae800225a90123da862032ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890560"
---
# <a name="idelaydc-interface"></a>IDelaydC-Schnittstelle

Die **IDelaydC-Schnittstelle** stellt die Methoden bereit, die zum Herstellen einer Verbindung mit dem Netzwerk, zum Erfassen des Netzwerkdatenverkehrs zu einer Erfassungsdatei, zum Abrufen von Statistiken und zum Trennen der Verbindung mit dem Netzwerk verwendet werden.

Diese Schnittstelle erfasst Frames aus dem Netzwerkdatenstrom und kopiert die Frames dann in eine Aufzeichnungsdatei. Diese Schnittstelle wird von Netzwerkmonitor- und NPP-Anwendungen verwendet. Um die Netzwerkdaten zu empfangen, muss die Ziel-NIC den promiscuous-Modus unterstützen.

## <a name="members"></a>Member

Die **IDelaydC-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDelaydC** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDelaydC-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                                                                             |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Konfigurieren**](idelaydc-configure.md)                                 | Übermittelt Konfigurationsinformationen, die für eine Erfassung verwendet werden.<br/>                                                                                        |
| [**Verbinden**](idelaydc-connect.md)                                     | Verbindet das NPP mit dem Netzwerk.<br/>                                                                                                             |
| [**Trennen**](idelaydc-disconnect.md)                               | Trennt die NPP vom Netzwerk.<br/>                                                                                                        |
| [**GetControlState**](idelaydc-getcontrolstate.md)                     | Ruft den Zustand der [*Erfassung*](c.md)ab, der angibt, ob die Erfassung ausgeführt oder angehalten wird.<br/>                      |
| [**GetConversationStatistics**](idelaydc-getconversationstatistics.md) | Ruft [*Sitzungs-*](s.md) und [*Stationsinformationen*](s.md) für die aktuelle Erfassung ab.<br/> |
| [**GetTotalStatistics**](idelaydc-gettotalstatistics.md)               | Extrahiert Zeit-, Puffer-, Treiber- und andere Netzwerkstatistiken aus der aktuell ausgeführten Erfassung.<br/>                                              |
| [**Anhalten**](idelaydc-pause.md)                                         | Beendet vorübergehend die aktuelle Erfassung.<br/>                                                                                                       |
| [**QueryStations**](idelaydc-querystations.md)                         | Ruft eine Liste aller Computer ab, die Netzwerkmonitor verwenden, um Daten in einem Subnetz zu erfassen.<br/>                                                      |
| [**QueryStatus**](idelaydc-querystatus.md)                             | Ruft den Status des NPP ab.<br/>                                                                                                             |
| [**Fortsetzen**](idelaydc-resume.md)                                       | Setzt eine angehaltene Erfassung fort.<br/>                                                                                                                    |
| [**Starten**](idelaydc-start.md)                                         | Startet eine Erfassung und erstellt die [*Erfassungsdatei*](c.md).<br/>                                                           |
| [**Beenden**](idelaydc-stop.md)                                           | Beendet die aktuelle Erfassung und schließt die [*Erfassungsdatei*](c.md).<br/>                                                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

