---
title: Netzwerk Objekt
description: Das Netzwerk Objekt stellt Eigenschaften und Methoden bereit, die für den Zugriff auf Statistiken in Bezug auf die Qualität einer Netzwerkverbindung und zum angeben und Abrufen der Netzwerk Proxy Einstellungen verwendet werden.
ms.assetid: 5ae6137e-22f5-4a65-8793-b6f66adb4cba
keywords:
- Windows-Media Player für Netzwerk Objekte
topic_type:
- apiref
api_name:
- Network Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d439679636bce773c43f5610060c4744ef4d5d7c
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "104389372"
---
# <a name="network-object"></a>Netzwerk Objekt

Das **Netzwerk** Objekt stellt Eigenschaften und Methoden bereit, die für den Zugriff auf Statistiken in Bezug auf die Qualität einer Netzwerkverbindung und zum angeben und Abrufen der Netzwerk Proxy Einstellungen verwendet werden.

Das **Netzwerk** Objekt unterstützt die folgenden Eigenschaften.



| Eigenschaft                                           | BESCHREIBUNG                                                                                 |
|----------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Bandbreite](network-bandwidth.md)                 | Ruft die aktuelle Bandbreite des Medien Elements ab.                                          |
| [Bitrate](network-bitrate.md)                     | Ruft die aktuelle Bitrate ab, die empfangen wird.                                              |
| [bufferingcount](network-bufferingcount.md)       | Ruft ab, wie oft die Pufferung während der Wiedergabe aufgetreten ist.                           |
| [Pufferungs](network-bufferingprogress.md) | Ruft den Prozentsatz der abgeschlossenen Pufferung ab.                                            |
| [BufferingTime](network-bufferingtime.md)         | Gibt den Puffer Zeitraum in Millisekunden vor Beginn der Wiedergabe an oder ruft ihn ab. |
| [Download Fortschritt](network-downloadprogress.md)   | Ruft den Prozentsatz des abgeschlossenen Downloads ab.                                             |
| [encodframerate](network-encodedframerate.md)   | Ruft die vom Inhalts Autor angegebene Video Frame Rate ab.                             |
| [Framerate](network-framerate.md)                 | Ruft die aktuelle Video Frame Rate ab.                                                     |
| [framesskipped](network-framesskipped.md)         | Ruft die Gesamtanzahl der Frames ab, die während der Wiedergabe übersprungen wurden.                               |
| [lostpakete](network-lostpackets.md)             | Ruft die Anzahl der verlorenen Pakete ab.                                                       |
| [maxBandwidth](network-maxbandwidth.md)           | Gibt die maximal zulässige Bandbreite an oder ruft diese ab.                                       |
| [maxbitrate](network-maxbitrate.md)               | Ruft die maximal mögliche Video Bitrate ab.                                              |
| [receivedpakete](network-receivedpackets.md)     | Ruft die Anzahl der empfangenen Pakete ab.                                                   |
| ["receptionquality"](network-receptionquality.md)   | Ruft den Prozentsatz der in den letzten 30 Sekunden empfangenen Pakete ab.                        |
| [wiederherstellbare Pakete](network-recoveredpackets.md)   | Ruft die Anzahl der wiederhergestellten Pakete ab.                                                  |
| [sourceprotocol](network-sourceprotocol.md)       | Ruft das Quell Protokoll ab, das zum Empfangen von Daten verwendet wird.                                         |



 

Das- **Netzwerk** Objekt unterstützt die folgenden Methoden.



| Methode                                                       | BESCHREIBUNG                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [getproxybypassforlocal](network-getproxybypassforlocal.md) | Ruft einen Wert ab, der angibt, ob der Proxy Server umgangen werden soll, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet. |
| [getproxyexceptionlist](network-getproxyexceptionlist.md)   | Ruft die Proxy Ausnahmeliste ab.                                                                                  |
| [getproxyname](network-getproxyname.md)                     | Ruft den Namen des zu verwendenden Proxy Servers ab.                                                                         |
| [getproxyport](network-getproxyport.md)                     | Ruft den zu verwendenden ProxyPort ab.                                                                                     |
| [getproxysettings](network-getproxysettings.md)             | Ruft die Proxy Einstellung für ein bestimmtes Protokoll ab.                                                                    |
| [setproxybypassforlocal](network-setproxybypassforlocal.md) | Gibt einen Wert an, der angibt, ob der Proxy Server umgangen werden soll, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet. |
| [setproxyexceptionlist](network-setproxyexceptionlist.md)   | Gibt die Proxy Ausnahmeliste an.                                                                                  |
| [setproxyname](network-setproxyname.md)                     | Gibt den Namen des zu verwendenden Proxy Servers an.                                                                         |
| [setproxyport](network-setproxyport.md)                     | Gibt den zu verwendenden ProxyPort an.                                                                                     |
| [setProxySettings](network-setproxysettings.md)             | Gibt die Proxy Einstellung für ein bestimmtes Protokoll an.                                                                    |



 

Der Zugriff auf das **Netzwerk** Objekt erfolgt über die folgende Eigenschaft.



| Object                      | Eigenschaft                      |
|-----------------------------|-------------------------------|
| [Player](player-object.md) | [network](player-network.md) |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Objektmodell Referenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




