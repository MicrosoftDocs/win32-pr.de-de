---
description: Die idelta Interface-Schnittstelle stellt die Methoden bereit, die zum Herstellen einer Verbindung mit dem Netzwerk, zum Erfassen von Netzwerk Datenverkehr für eine Aufzeichnungsdatei, zum Abrufen von Statistiken und zum Trennen der Verbindung mit dem Netzwerk
ms.assetid: ab275653-2377-4af6-a810-48515962c88c
title: Idelta aydc-Schnittstelle (Netmon. h)
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
ms.openlocfilehash: cb87bc9f821e758b83a1bc3dee5d81a4b1b771d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372895"
---
# <a name="idelaydc-interface"></a>Idelta aydc-Schnittstelle

Die **idelta** Interface-Schnittstelle stellt die Methoden bereit, die zum Herstellen einer Verbindung mit dem Netzwerk, zum Erfassen von Netzwerk Datenverkehr für eine Aufzeichnungsdatei, zum Abrufen von Statistiken und zum Trennen der Verbindung mit dem Netzwerk

Diese Schnittstelle erfasst Frames aus dem Netzwerkdaten Strom und kopiert dann die Frames in eine Erfassungs Datei. Diese Schnittstelle wird von Netzwerkmonitor-und NPP-Anwendungen verwendet. Zum Empfangen der Netzwerkdaten muss die Ziel-NIC den gemischten-Modus unterstützen.

## <a name="members"></a>Member

Die **idelta-DC** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Idelta aydc** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **idelta-DC** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                                                                             |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Konfigurieren**](idelaydc-configure.md)                                 | Übermittelt Konfigurationsinformationen, die für eine Erfassung verwendet werden.<br/>                                                                                        |
| [**Verbinden**](idelaydc-connect.md)                                     | Verbindet den NPP mit dem Netzwerk.<br/>                                                                                                             |
| [**Trennen**](idelaydc-disconnect.md)                               | Trennt die NPP vom Netzwerk.<br/>                                                                                                        |
| [**Getcontrolstate**](idelaydc-getcontrolstate.md)                     | Ruft den Zustand der [*Erfassung*](c.md)ab, der angibt, ob die Erfassung ausgeführt wird oder angehalten wurde.<br/>                      |
| [**Getconversation ationstatistics**](idelaydc-getconversationstatistics.md) | Ruft [*Sitzungs*](s.md) -und [*Stations Informationen*](s.md) für die aktuelle Erfassung ab.<br/> |
| [**Gettotalstatistics**](idelaydc-gettotalstatistics.md)               | Extrahiert Zeit, Puffer, Treiber und andere Netzwerk Statistiken aus der aktuell laufenden Erfassung.<br/>                                              |
| [**Anhalten**](idelaydc-pause.md)                                         | Beendet vorübergehend die aktuelle Erfassung.<br/>                                                                                                       |
| [**Querystations**](idelaydc-querystations.md)                         | Ruft eine Liste aller Computer ab, von denen Netzwerkmonitor zum Erfassen von Daten in einem Subnetz verwendet wird.<br/>                                                      |
| [**QueryStatus**](idelaydc-querystatus.md)                             | Ruft den Status des NPP ab.<br/>                                                                                                             |
| [**Fortsetzen**](idelaydc-resume.md)                                       | Setzt eine angehaltene Erfassung fort.<br/>                                                                                                                    |
| [**Start**](idelaydc-start.md)                                         | Startet eine Erfassung und erstellt die [*Erfassungs Datei*](c.md).<br/>                                                           |
| [**Stop**](idelaydc-stop.md)                                           | Beendet die aktuelle Erfassung und schließt die [*Erfassungs Datei*](c.md).<br/>                                                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

