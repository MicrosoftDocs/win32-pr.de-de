---
description: Die IESP-Schnittstelle stellt die Methoden bereit, die das NPP mit dem Netzwerk verbinden, Netzwerkdatenverkehr zu einer Erfassungsdatei erfassen, Statistiken abrufen und den NPP vom Netzwerk trennen.
ms.assetid: e483f501-4928-4bfd-b212-e100f2b8f64f
title: IESP-Schnittstelle (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e7420e21a9f2c6ac92712326fa4a51159c6303d3972756e7a47c0797f22a1d83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037430"
---
# <a name="iesp-interface"></a>IESP-Schnittstelle

Die **IESP-Schnittstelle** stellt die Methoden bereit, die das NPP mit dem Netzwerk verbinden, Netzwerkdatenverkehr zu einer Erfassungsdatei erfassen, Statistiken abrufen und den NPP vom Netzwerk trennen. Diese Schnittstelle wird hauptsächlich verwendet, wenn Sie Netzwerk-Konversationsstatistiken [*in*](c.md) einem proprietären ESP-Dateiformat sammeln müssen.

## <a name="members"></a>Member

Die **IESP-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IESP** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IESP-Schnittstelle** verfügt über diese Methoden.



| Methode                                          | BESCHREIBUNG                                                                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**Konfigurieren**](iesp-configure.md)             | Übermittelt Konfigurationsinformationen für eine Erfassung<br/>                                                                         |
| [**Verbinden**](iesp-connect.md)                 | Verbindet das NPP mit dem Netzwerk.<br/>                                                                                        |
| [**Trennen**](iesp-disconnect.md)           | Trennt die Verbindung zwischen dem NPP und dem Netzwerk.<br/>                                                                                   |
| [**GetControlState**](iesp-getcontrolstate.md) | Ruft den Zustand der Erfassung [*ab,*](c.md)der angibt, ob die Erfassung ausgeführt wird oder angehalten wurde.<br/> |
| [**Anhalten**](iesp-pause.md)                     | Beendet vorübergehend die aktuelle Erfassung.<br/>                                                                                  |
| [**QueryStations**](iesp-querystations.md)     | Ruft eine Liste aller Computer ab, die Netzwerkmonitor zum Erfassen von Daten in einem Subnetz verwenden.<br/>                           |
| [**QueryStatus**](iesp-querystatus.md)         | Ruft den Status des NPP ab.<br/>                                                                                        |
| [**Fortsetzen**](iesp-resume.md)                   | Setzt eine angehaltene Erfassung wieder ein.<br/>                                                                                               |
| [**Starten**](iesp-start.md)                     | Startet die Erfassung und erstellt die Erfassungsdatei.<br/>                                                                        |
| [**Beenden**](iesp-stop.md)                       | Beendet die aktuelle Erfassung.<br/>                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

