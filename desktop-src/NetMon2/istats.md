---
description: Die iStats-Schnittstelle stellt die Methoden bereit, die Sie verwenden, um eine NPP mit dem Netzwerk zu verbinden, den Netzwerk Datenverkehr zu erfassen, Statistiken abzurufen und die NPP vom Netzwerk zu trennen. Diese Schnittstelle generiert Statistiken ohne Frames.
ms.assetid: 57cfcdd6-f16c-4a1c-b2ba-ce98f0576862
title: IStats-Schnittstelle (Netmon. h)
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
ms.openlocfilehash: b64816589e3d4d0a2e3ace7be5c895e3d2cf22f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353130"
---
# <a name="istats-interface"></a>IStats-Schnittstelle

Die **iStats** -Schnittstelle stellt die Methoden bereit, die Sie verwenden, um eine NPP mit dem Netzwerk zu verbinden, den Netzwerk Datenverkehr zu erfassen, Statistiken abzurufen und die NPP vom Netzwerk zu trennen. Diese Schnittstelle generiert Statistiken ohne Frames.

## <a name="members"></a>Member

Die **iStats** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **IStats** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iStats** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                | BESCHREIBUNG                                                                                                                                               |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Konfigurieren**](istats-configure.md)                                 | Konfiguriert den-, Muster Übereinstimmungs-und Puffergröße der Erfassungs Datei.<br/>                                                                    |
| [**Verbinden**](istats-connect.md)                                     | Verbindet den NPP mit dem Netzwerk.<br/>                                                                                                               |
| [**Trennen**](istats-disconnect.md)                               | Trennt die NPP vom Netzwerk.<br/>                                                                                                          |
| [**Getcontrolstate**](istats-getcontrolstate.md)                     | Ruft den Zustand der [*Erfassung*](c.md)ab, der angibt, ob die Erfassung ausgeführt wird oder angehalten wurde.<br/>                        |
| [**Getconversation ationstatistics**](istats-getconversationstatistics.md) | Ruft [*Sitzungs*](s.md) -und [*Stations Informationen*](s.md) zur aktuellen Erfassung ab.<br/> |
| [**Gettotalstatistics**](istats-gettotalstatistics.md)               | Extrahiert Zeit, Puffer, Treiber und andere Netzwerk Statistiken aus der aktuell laufenden Erfassung.<br/>                                                |
| [**Anhalten**](istats-pause.md)                                         | Beendet vorübergehend die aktuelle Erfassung.<br/>                                                                                                         |
| [**Querystations**](istats-querystations.md)                         | Ruft eine Liste aller Computer ab, die Netzwerkmonitor zum Erfassen von Daten in einem Subnetz verwenden.<br/>                                                  |
| [**QueryStatus**](istats-querystatus.md)                             | Ruft den Status des NPP ab.<br/>                                                                                                               |
| [**Fortsetzen**](istats-resume.md)                                       | Startet eine angehaltene Erfassung neu.<br/>                                                                                                                     |
| [**Start**](istats-start.md)                                         | Startet die Erfassung.<br/>                                                                                                                            |
| [**Stop**](istats-stop.md)                                           | Hält die aktuelle Erfassung an.<br/>                                                                                                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

