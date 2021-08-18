---
title: Netzwerkobjekt
description: Das Network-Objekt stellt Eigenschaften und Methoden für den Zugriff auf Statistiken im Zusammenhang mit der Qualität einer Netzwerkverbindung sowie zum Angeben und Abrufen der Netzwerkproxyeinstellungen zur Auswahl.
ms.assetid: 5ae6137e-22f5-4a65-8793-b6f66adb4cba
keywords:
- Netzwerkobjekt-Windows Media Player
topic_type:
- apiref
api_name:
- Network Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6bf91c23d6a5c581430b17a370e66027a5f9174d0511a2647fba33834ec6c4b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996110"
---
# <a name="network-object"></a>Netzwerkobjekt

Das **Network-Objekt** stellt Eigenschaften und Methoden für den Zugriff auf Statistiken im Zusammenhang mit der Qualität einer Netzwerkverbindung sowie zum Angeben und Abrufen der Netzwerkproxyeinstellungen zur Auswahl.

Das **Network-Objekt** unterstützt die folgenden Eigenschaften.



| Eigenschaft                                           | BESCHREIBUNG                                                                                 |
|----------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Bandbreite](network-bandwidth.md)                 | Ruft die aktuelle Bandbreite des Medienelements ab.                                          |
| [Bitrate](network-bitrate.md)                     | Ruft die aktuelle Bitrate ab, die empfangen wird.                                              |
| [bufferingCount](network-bufferingcount.md)       | Ruft ab, wie oft die Pufferung während der Wiedergabe aufgetreten ist.                           |
| [bufferingProgress](network-bufferingprogress.md) | Ruft den Prozentsatz der abgeschlossenen Pufferung ab.                                            |
| [bufferingTime](network-bufferingtime.md)         | Gibt die Pufferzeit in Millisekunden an oder ruft sie ab, bevor die Wiedergabe beginnt. |
| [downloadProgress](network-downloadprogress.md)   | Ruft den Prozentsatz des abgeschlossenen Downloads ab.                                             |
| [encodedFrameRate](network-encodedframerate.md)   | Ruft die vom Inhaltsautor angegebene Videobildrate ab.                             |
| [frameRate](network-framerate.md)                 | Ruft die aktuelle Videobildrate ab.                                                     |
| [framesSkipped](network-framesskipped.md)         | Ruft die Gesamtanzahl der Frames ab, die während der Wiedergabe übersprungen wurden.                               |
| [lostPackets](network-lostpackets.md)             | Ruft die Anzahl der verlorenen Pakete ab.                                                       |
| [Maxbandwidth](network-maxbandwidth.md)           | Gibt die maximal zulässige Bandbreite an oder ruft sie ab.                                       |
| [maxBitRate](network-maxbitrate.md)               | Ruft die maximal mögliche Videobitrate ab.                                              |
| [receivedPackets](network-receivedpackets.md)     | Ruft die Anzahl der empfangenen Pakete ab.                                                   |
| [receptionQuality](network-receptionquality.md)   | Ruft den Prozentsatz der Pakete ab, die in den letzten 30 Sekunden empfangen wurden.                        |
| [recoveredPackets](network-recoveredpackets.md)   | Ruft die Anzahl der wiederhergestellten Pakete ab.                                                  |
| [sourceProtocol](network-sourceprotocol.md)       | Ruft das Quellprotokoll ab, das zum Empfangen von Daten verwendet wird.                                         |



 

Das **Network-Objekt** unterstützt die folgenden Methoden.



| Methode                                                       | BESCHREIBUNG                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [getProxyBypassForLocal](network-getproxybypassforlocal.md) | Ruft einen Wert ab, der angibt, ob der Proxyserver umgangen werden soll, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet. |
| [getProxyExceptionList](network-getproxyexceptionlist.md)   | Ruft die Proxyausnahmeliste ab.                                                                                  |
| [getProxyName](network-getproxyname.md)                     | Ruft den Namen eines zu verwendenden Proxyservers ab.                                                                         |
| [getProxyPort](network-getproxyport.md)                     | Ruft den zu verwendenden Proxyport ab.                                                                                     |
| [getProxySettings](network-getproxysettings.md)             | Ruft die Proxyeinstellung für ein bestimmtes Protokoll ab.                                                                    |
| [setProxyBypassForLocal](network-setproxybypassforlocal.md) | Gibt einen Wert an, der angibt, ob der Proxyserver umgangen werden soll, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet. |
| [setProxyExceptionList](network-setproxyexceptionlist.md)   | Gibt die Proxyausnahmeliste an.                                                                                  |
| [setProxyName](network-setproxyname.md)                     | Gibt den Namen eines zu verwendenden Proxyservers an.                                                                         |
| [setProxyPort](network-setproxyport.md)                     | Gibt den zu verwendenden Proxyport an.                                                                                     |
| [setProxySettings](network-setproxysettings.md)             | Gibt die Proxyeinstellung für ein bestimmtes Protokoll an.                                                                    |



 

Auf **das Network-Objekt** wird über die folgende Eigenschaft zugegriffen.



| Object                      | Eigenschaft                      |
|-----------------------------|-------------------------------|
| [Player](player-object.md) | [network](player-network.md) |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Objektmodellreferenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




