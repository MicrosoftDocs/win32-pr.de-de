---
description: Die IRTC-Schnittstelle stellt die Methoden bereit, die verwendet werden, um die NPP mit dem Netzwerk zu verbinden, Netzwerkdatenverkehr zu erfassen, Statistiken abzurufen und das NPP aus dem Netzwerk zu trennen.
ms.assetid: 9252a9ba-2c3e-40b9-b8de-84ef5d4831a7
title: IRTC-Schnittstelle (Netmon.h)
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
ms.openlocfilehash: f330892da5844305d4d1f3ffa3aee0bf6e9ef50fb2a1cd951c332e2b17eb3b12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132929"
---
# <a name="irtc-interface"></a>IRTC-Schnittstelle

Die **IRTC-Schnittstelle** stellt die Methoden bereit, die verwendet werden, um die NPP mit dem Netzwerk zu verbinden, Netzwerkdatenverkehr zu erfassen, Statistiken abzurufen und das NPP aus dem Netzwerk zu trennen. **IRTC** ruft eine Schnittstelle zu rein lokalen Einstiegspunkten ab, die für die Echtzeiterfassung erforderlich sind. Diese Schnittstelle enthält eine Methode, die einen Rückruf an das NPP übergibt.

## <a name="members"></a>Member

Die **IRTC-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IRTC** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IRTC-Schnittstelle** verfügt über diese Methoden.



| Methode                                                              | Beschreibung                                                                                                                                             |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Konfigurieren**](irtc-configure.md)                                 | Legt den Trigger, die Musterübersprechung und die Puffergröße der Erfassung fest.<br/>                                                                             |
| [**Verbinden**](irtc-connect.md)                                     | Verbindet das NPP mit dem Netzwerk.<br/>                                                                                                             |
| [**Trennen**](irtc-disconnect.md)                               | Trennt die NPP vom Netzwerk.<br/>                                                                                                        |
| [**GetControlState**](irtc-getcontrolstate.md)                     | Ruft den Zustand der [*Erfassung*](c.md)ab, der angibt, ob die Erfassung ausgeführt oder angehalten wird.<br/>                      |
| [**GetConversationStatistics**](irtc-getconversationstatistics.md) | Ruft [*Sitzungs-*](s.md) und [*Stationsinformationen*](s.md) für die aktuelle Erfassung ab.<br/> |
| [**GetTotalStatistics**](irtc-gettotalstatistics.md)               | Extrahiert Zeit-, Puffer-, Treiber- und andere Netzwerkstatistiken aus der aktuell ausgeführten Erfassung.<br/>                                              |
| [**Anhalten**](irtc-pause.md)                                         | Beendet vorübergehend die aktuelle Erfassung.<br/>                                                                                                       |
| [**QueryStations**](irtc-querystations.md)                         | Ruft eine Liste aller Computer in einem Subnetz ab, die Netzwerkmonitor zum Erfassen von Netzwerkdaten verwenden.<br/>                                        |
| [**QueryStatus**](irtc-querystatus.md)                             | Ruft den Status des NPP ab.<br/>                                                                                                             |
| [**Fortsetzen**](irtc-resume.md)                                       | Startet eine angehaltene Erfassung neu.<br/>                                                                                                                   |
| [**Starten**](irtc-start.md)                                         | Startet eine Erfassung.<br/>                                                                                                                            |
| [**Stoppen**](irtc-stop.md)                                           | Beendet die aktuelle Erfassung.<br/>                                                                                                                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

