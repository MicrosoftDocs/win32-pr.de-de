---
description: Die iESP-Schnittstelle stellt die Methoden bereit, die die NPP mit dem Netzwerk verbinden, den Netzwerk Datenverkehr für eine Erfassungs Datei erfassen, Statistiken abrufen und die Verbindung mit dem NPP vom Netzwerk trennen.
ms.assetid: e483f501-4928-4bfd-b212-e100f2b8f64f
title: IESP-Schnittstelle (Netmon. h)
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
ms.openlocfilehash: 1a7400bb9a16e6ece5f5f26fe95a0398a7d45e19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128917"
---
# <a name="iesp-interface"></a>IESP-Schnittstelle

Die **iESP** -Schnittstelle stellt die Methoden bereit, die die NPP mit dem Netzwerk verbinden, den Netzwerk Datenverkehr für eine Erfassungs Datei erfassen, Statistiken abrufen und die Verbindung mit dem NPP vom Netzwerk trennen. Diese Schnittstelle wird hauptsächlich verwendet, wenn Sie [*netzwerkkonversationsstatistiken*](c.md) in einem proprietären ESP-Dateiformat erfassen müssen.

## <a name="members"></a>Member

Die **iESP** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **IESP** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iESP** -Schnittstelle verfügt über diese Methoden.



| Methode                                          | BESCHREIBUNG                                                                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**Konfigurieren**](iesp-configure.md)             | Übermittelt Konfigurationsinformationen für eine Erfassung<br/>                                                                         |
| [**Verbinden**](iesp-connect.md)                 | Verbindet den NPP mit dem Netzwerk.<br/>                                                                                        |
| [**Trennen**](iesp-disconnect.md)           | Trennt die NPP vom Netzwerk.<br/>                                                                                   |
| [**Getcontrolstate**](iesp-getcontrolstate.md) | Ruft den Zustand der [*Erfassung*](c.md)ab, der angibt, ob die Erfassung ausgeführt wird oder angehalten wurde.<br/> |
| [**Anhalten**](iesp-pause.md)                     | Beendet vorübergehend die aktuelle Erfassung.<br/>                                                                                  |
| [**Querystations**](iesp-querystations.md)     | Ruft eine Liste aller Computer ab, die Netzwerkmonitor zum Erfassen von Daten in einem Subnetz verwenden.<br/>                           |
| [**QueryStatus**](iesp-querystatus.md)         | Ruft den Status des NPP ab.<br/>                                                                                        |
| [**Fortsetzen**](iesp-resume.md)                   | Setzt eine angehaltene Erfassung fort.<br/>                                                                                               |
| [**Start**](iesp-start.md)                     | Startet die Erfassung und erstellt die Erfassungs Datei.<br/>                                                                        |
| [**Stop**](iesp-stop.md)                       | Hält die aktuelle Erfassung an.<br/>                                                                                              |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

