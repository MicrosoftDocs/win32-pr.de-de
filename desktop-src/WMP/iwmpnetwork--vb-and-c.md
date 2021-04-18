---
title: Iwmpnetwork (VB und C)-Schnittstelle (WMP. h)
description: Stellt Eigenschaften und Methoden für den Zugriff auf Statistiken in Bezug auf die Qualität einer Netzwerkverbindung sowie zum angeben und Abrufen der Netzwerk Proxy Einstellungen bereit. Die iwmpnetwork-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: d385510f-11cf-4a2a-96be-b416cddc3d80
keywords:
- Iwmpnetwork (VB und C) Interface Windows Media Player
- Iwmpnetwork (VB und C) Interface Windows Media Player, beschrieben
topic_type:
- apiref
api_name:
- IWMPNetwork (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 301fe5c89d2eb5df3dd4c22927e75a5607e7abd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364700"
---
# <a name="iwmpnetwork-vb-and-c-interface"></a>Iwmpnetwork (VB und c#)-Schnittstelle

Stellt Eigenschaften und Methoden für den Zugriff auf Statistiken in Bezug auf die Qualität einer Netzwerkverbindung sowie zum angeben und Abrufen der Netzwerk Proxy Einstellungen bereit.

Die **iwmpnetwork** -Schnittstelle macht die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die **iwmpnetwork (VB und c#)** -Schnittstelle verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **iwmpnetwork (VB und c#)** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                           | BESCHREIBUNG                                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**getproxybypassforlocal**](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)                   | Gibt einen Wert zurück, der angibt, ob der Proxy Server umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.<br/> |
| [**getproxyexceptionlist**](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)   | Gibt die Liste der Proxy Ausnahmen zurück.<br/>                                                                           |
| [**getproxyname**](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)                     | Gibt den Namen des verwendeten Proxy Servers zurück.<br/>                                                            |
| [**getproxyport**](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)                     | Gibt den verwendeten ProxyPort zurück.<br/>                                                                          |
| [**getproxysettings**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)             | Gibt Informationen zu den Proxy Einstellungen für ein Protokoll zurück.<br/>                                                |
| [**setproxybypassforlocal**](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md) | Gibt an, ob der Proxy Server umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.<br/>                  |
| [**setproxyexceptionlist**](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)   | Gibt die Proxy Ausnahmeliste an.<br/>                                                                         |
| [**setproxyname**](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)                     | Gibt den Namen des zu verwendenden Proxy Servers an.<br/>                                                              |
| [**setproxyport**](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)                     | Gibt den zu verwendenden ProxyPort an.<br/>                                                                            |
| [**setProxySettings**](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)             | Gibt die Proxy Einstellungen für ein Protokoll an.<br/>                                                                |



 

### <a name="properties"></a>Eigenschaften

Die **iwmpnetwork (VB und c#)** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                          | Zugriffstyp           | BESCHREIBUNG                                                                                  |
|:--------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------|
| [**Bandbreite**](wmplibiwmpnetwork-iwmpnetwork-bandwidth--vb-and-c.md)<br/>                 | Schreibgeschützt<br/>  | Ruft die aktuelle Bandbreite des Medien Elements ab.<br/>                                     |
| [**Bitrate**](wmplibiwmpnetwork-iwmpnetwork-bitrate--vb-and-c.md)<br/>                     | Schreibgeschützt<br/>  | Ruft die aktuelle Bitrate ab, die empfangen wird.<br/>                                         |
| [**bufferingcount**](wmplibiwmpnetwork-iwmpnetwork-bufferingcount--vb-and-c.md)<br/>       | Schreibgeschützt<br/>  | Ruft ab, wie oft die Pufferung während der Wiedergabe aufgetreten ist.<br/>                      |
| [**Pufferungs**](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)<br/> | Schreibgeschützt<br/>  | Ruft den Prozentsatz der abgeschlossenen Pufferung ab.<br/>                                       |
| [**BufferingTime**](wmplibiwmpnetwork-iwmpnetwork-bufferingtime--vb-and-c.md)<br/>         | Lesen/Schreiben<br/> | Ruft die Zeitspanne in Millisekunden ab, bevor die Wiedergabe beginnt, oder legt Sie fest.<br/> |
| [**Download Fortschritt**](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)<br/>   | Schreibgeschützt<br/>  | Ruft den Prozentsatz des abgeschlossenen Downloads ab.<br/>                                     |
| [**encodframerate**](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)<br/>   | Schreibgeschützt<br/>  | Ruft die vom Inhalts Autor angegebene Video Frame Rate ab.<br/>                        |
| [**Framerate**](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)<br/>                 | Schreibgeschützt<br/>  | Ruft die aktuelle Video Frame Rate ab.<br/>                                                |
| [**framesskipped**](wmplibiwmpnetwork-iwmpnetwork-framesskipped--vb-and-c.md)<br/>         | Schreibgeschützt<br/>  | Ruft die Gesamtanzahl der während der Wiedergabe übersprungenen Frames ab.<br/>                          |
| [**lostpakete**](wmplibiwmpnetwork-iwmpnetwork-lostpackets--vb-and-c.md)<br/>             | Schreibgeschützt<br/>  | Ruft die Anzahl der verlorenen Pakete ab.<br/>                                                  |
| [**maxBandwidth**](wmplibiwmpnetwork-iwmpnetwork-maxbandwidth--vb-and-c.md)<br/>           | Lesen/Schreiben<br/> | Ruft die maximal zulässige Bandbreite ab oder legt Sie fest.<br/>                                       |
| [**maxbitrate**](wmplibiwmpnetwork-iwmpnetwork-maxbitrate--vb-and-c.md)<br/>               | Schreibgeschützt<br/>  | Ruft die maximal mögliche Video Bitrate ab.<br/>                                         |
| [**receivedpakete**](wmplibiwmpnetwork-iwmpnetwork-receivedpackets--vb-and-c.md)<br/>     | Schreibgeschützt<br/>  | Ruft die Anzahl der empfangenen Pakete ab.<br/>                                              |
| [**"receptionquality"**](wmplibiwmpnetwork-iwmpnetwork-receptionquality--vb-and-c.md)<br/>   | Schreibgeschützt<br/>  | Ruft den Prozentsatz der in den letzten 30 Sekunden nicht verlorenen Pakete ab.<br/>                   |
| [**wiederherstellbare Pakete**](wmplibiwmpnetwork-iwmpnetwork-recoveredpackets--vb-and-c.md)<br/>   | Schreibgeschützt<br/>  | Ruft die Anzahl der wiederhergestellten Pakete ab.<br/>                                             |
| [**sourceprotocol**](wmplibiwmpnetwork-iwmpnetwork-sourceprotocol--vb-and-c.md)<br/>       | Schreibgeschützt<br/>  | Ruft das Quell Protokoll ab, das zum Empfangen von Daten verwendet wird.<br/>                                    |



 

Verwenden Sie die folgende Eigenschaft, um eine **iwmpnetwork** -Schnittstelle zu erhalten.



| Object                                                                   | Eigenschaft                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------|
| [AxWindowsMediaPlayer-Objekt](axwindowsmediaplayer-object--vb-and-c.md) | [**Netzwerk**](axwmplib-axwindowsmediaplayer-network--vb-and-c.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Visual Basic .net und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





