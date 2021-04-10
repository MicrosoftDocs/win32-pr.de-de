---
description: Die untc-Schnittstelle stellt die Methoden bereit, mit denen die NPP mit dem Netzwerk verbunden, Netzwerk Datenverkehr erfasst, Statistiken abgerufen und die Netzwerkverbindung vom Netzwerk getrennt wird.
ms.assetid: 9252a9ba-2c3e-40b9-b8de-84ef5d4831a7
title: Untc-Schnittstelle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: c937d7d9233b1df063a7cf4a12e57e909145b8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959384"
---
# <a name="irtc-interface"></a>Untc-Schnittstelle

Die **untc** -Schnittstelle stellt die Methoden bereit, mit denen die NPP mit dem Netzwerk verbunden, Netzwerk Datenverkehr erfasst, Statistiken abgerufen und die Netzwerkverbindung vom Netzwerk getrennt wird. Bei " **untc** " wird eine Schnittstelle zu lokalen Einstiegspunkten abgerufen, die zum Einbinden der echt Zeiterfassung notwendig sind. Diese Schnittstelle enthält eine Methode, die einen Rückruf an den NPP übergibt.

## <a name="members"></a>Member

Die Schnittstelle " **iritc** " erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Außerdem gibt** es die folgenden Arten von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die Schnittstelle " **iritc** " verfügt über diese Methoden.



| Methode                                                              | BESCHREIBUNG                                                                                                                                             |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Konfigurieren**](irtc-configure.md)                                 | Legt den-, Muster Übereinstimmungs-und Puffergröße der Erfassung fest.<br/>                                                                             |
| [**Verbinden**](irtc-connect.md)                                     | Verbindet den NPP mit dem Netzwerk.<br/>                                                                                                             |
| [**Trennen**](irtc-disconnect.md)                               | Trennt die NPP vom Netzwerk.<br/>                                                                                                        |
| [**Getcontrolstate**](irtc-getcontrolstate.md)                     | Ruft den Zustand der [*Erfassung*](c.md)ab, der angibt, ob die Erfassung ausgeführt wird oder angehalten wurde.<br/>                      |
| [**Getconversation ationstatistics**](irtc-getconversationstatistics.md) | Ruft [*Sitzungs*](s.md) -und [*Stations Informationen*](s.md) für die aktuelle Erfassung ab.<br/> |
| [**Gettotalstatistics**](irtc-gettotalstatistics.md)               | Extrahiert Zeit, Puffer, Treiber und andere Netzwerk Statistiken aus der aktuell laufenden Erfassung.<br/>                                              |
| [**Anhalten**](irtc-pause.md)                                         | Beendet vorübergehend die aktuelle Erfassung.<br/>                                                                                                       |
| [**Querystations**](irtc-querystations.md)                         | Ruft eine Liste aller Computer in einem Subnetz ab, die Netzwerkmonitor zum Erfassen von Netzwerkdaten verwenden.<br/>                                        |
| [**QueryStatus**](irtc-querystatus.md)                             | Ruft den Status des NPP ab.<br/>                                                                                                             |
| [**Fortsetzen**](irtc-resume.md)                                       | Startet eine angehaltene Erfassung neu.<br/>                                                                                                                   |
| [**Start**](irtc-start.md)                                         | Startet eine Aufzeichnung.<br/>                                                                                                                            |
| [**Stop**](irtc-stop.md)                                           | Hält die aktuelle Erfassung an.<br/>                                                                                                                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

