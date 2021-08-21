---
description: Die IStats-Schnittstelle stellt die Methoden bereit, die Sie verwenden, um eine NPP mit dem Netzwerk zu verbinden, Netzwerkdatenverkehr zu erfassen, Statistiken abzurufen und die NPP vom Netzwerk zu trennen. Diese Schnittstelle generiert Statistiken ohne Frames.
ms.assetid: 57cfcdd6-f16c-4a1c-b2ba-ce98f0576862
title: IStats-Schnittstelle (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 27a43f8ea2902af7e2847e032da18543ffdbb228c2aa3e49fde63ce7cd727512
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495010"
---
# <a name="istats-interface"></a>IStats-Schnittstelle

Die **IStats-Schnittstelle** stellt die Methoden bereit, die Sie verwenden, um eine NPP mit dem Netzwerk zu verbinden, Netzwerkdatenverkehr zu erfassen, Statistiken abzurufen und die NPP vom Netzwerk zu trennen. Diese Schnittstelle generiert Statistiken ohne Frames.

## <a name="members"></a>Member

Die **IStats-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IStats verfügt** auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IStats-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                | Beschreibung                                                                                                                                               |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Konfigurieren**](istats-configure.md)                                 | Konfiguriert den Trigger, die Musterüber übereinstimmung und die Puffergröße der Erfassungsdatei.<br/>                                                                    |
| [**Verbinden**](istats-connect.md)                                     | Verbindet das NPP mit dem Netzwerk.<br/>                                                                                                               |
| [**Trennen**](istats-disconnect.md)                               | Trennt die Verbindung zwischen dem NPP und dem Netzwerk.<br/>                                                                                                          |
| [**GetControlState**](istats-getcontrolstate.md)                     | Ruft den Zustand der Erfassung [*ab,*](c.md)der angibt, ob die Erfassung ausgeführt wird oder angehalten wurde.<br/>                        |
| [**GetConversationStatistics**](istats-getconversationstatistics.md) | Ruft [*Sitzungs-*](s.md) und [*Stationsinformationen zur*](s.md) aktuellen Erfassung ab.<br/> |
| [**GetTotalStatistics**](istats-gettotalstatistics.md)               | Extrahiert Zeit-, Puffer-, Treiber- und andere Netzwerkstatistiken aus der aktuell ausgeführten Erfassung.<br/>                                                |
| [**Anhalten**](istats-pause.md)                                         | Beendet vorübergehend die aktuelle Erfassung.<br/>                                                                                                         |
| [**QueryStations**](istats-querystations.md)                         | Ruft eine Liste aller Computer ab, die Netzwerkmonitor zum Erfassen von Daten in einem Subnetz verwenden.<br/>                                                  |
| [**QueryStatus**](istats-querystatus.md)                             | Ruft den Status des NPP ab.<br/>                                                                                                               |
| [**Fortsetzen**](istats-resume.md)                                       | Startet eine angehaltene Erfassung neu.<br/>                                                                                                                     |
| [**Starten**](istats-start.md)                                         | Startet die Erfassung.<br/>                                                                                                                            |
| [**Stoppen**](istats-stop.md)                                           | Beendet die aktuelle Erfassung.<br/>                                                                                                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

