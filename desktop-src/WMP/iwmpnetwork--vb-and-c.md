---
title: IWMPNetwork-Schnittstelle (VB und C ) (Wmp.h)
description: Stellt Eigenschaften und Methoden für den Zugriff auf Statistiken im Zusammenhang mit der Qualität einer Netzwerkverbindung sowie zum Angeben und Abrufen der Netzwerkproxyeinstellungen zur Auswahl. Die IWMPNetwork-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: d385510f-11cf-4a2a-96be-b416cddc3d80
keywords:
- IWMPNetwork-Schnittstelle (VB und C) Windows Media Player
- IWMPNetwork -Schnittstelle (VB und C) Windows Media Player , beschrieben
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
ms.openlocfilehash: 93110b25bd7d194c4f1d7c213228512fd8bc6000df15b726e3f32a6e6e79a62a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572450"
---
# <a name="iwmpnetwork-vb-and-c-interface"></a>IWMPNetwork-Schnittstelle (VB und C#)

Stellt Eigenschaften und Methoden für den Zugriff auf Statistiken im Zusammenhang mit der Qualität einer Netzwerkverbindung sowie zum Angeben und Abrufen der Netzwerkproxyeinstellungen zur Auswahl.

Die **IWMPNetwork-Schnittstelle** macht die folgenden Eigenschaften verfügbar.

## <a name="members"></a>Member

Die **IWMPNetwork-Schnittstelle (VB und C#)** verfügt über diese Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IWMPNetwork-Schnittstelle (VB und C#)** verfügt über diese Methoden.



| Methode                                                                                           | Beschreibung                                                                                                            |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**getProxyBypassForLocal**](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)                   | Gibt einen Wert zurück, der angibt, ob der Proxyserver umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.<br/> |
| [**getProxyExceptionList**](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)   | Gibt die Proxyausnahmeliste zurück.<br/>                                                                           |
| [**getProxyName**](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)                     | Gibt den Namen des verwendeten Proxyservers zurück.<br/>                                                            |
| [**getProxyPort**](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)                     | Gibt den verwendeten Proxyport zurück.<br/>                                                                          |
| [**getProxySettings**](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)             | Gibt Informationen zu den Proxyeinstellungen für ein Protokoll zurück.<br/>                                                |
| [**setProxyBypassForLocal**](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md) | Gibt an, ob der Proxyserver umgangen wird, wenn sich der Ursprungsserver in einem lokalen Netzwerk befindet.<br/>                  |
| [**setProxyExceptionList**](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)   | Gibt die Proxyausnahmeliste an.<br/>                                                                         |
| [**setProxyName**](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)                     | Gibt den Namen des zu verwendenden Proxyservers an.<br/>                                                              |
| [**setProxyPort**](wmplibiwmpnetwork-iwmpnetwork-setproxyport--vb-and-c.md)                     | Gibt den zu verwendenden Proxyport an.<br/>                                                                            |
| [**setProxySettings**](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)             | Gibt die Proxyeinstellungen für ein Protokoll an.<br/>                                                                |



 

### <a name="properties"></a>Eigenschaften

Die **IWMPNetwork-Schnittstelle (VB und C#)** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                          | Zugriffstyp           | Beschreibung                                                                                  |
|:--------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------|
| [**Bandbreite**](wmplibiwmpnetwork-iwmpnetwork-bandwidth--vb-and-c.md)<br/>                 | Schreibgeschützt<br/>  | Ruft die aktuelle Bandbreite des Medienelements ab.<br/>                                     |
| [**Bitrate**](wmplibiwmpnetwork-iwmpnetwork-bitrate--vb-and-c.md)<br/>                     | Schreibgeschützt<br/>  | Ruft die aktuelle Bitrate ab, die empfangen wird.<br/>                                         |
| [**bufferingCount**](wmplibiwmpnetwork-iwmpnetwork-bufferingcount--vb-and-c.md)<br/>       | Schreibgeschützt<br/>  | Ruft ab, wie oft die Pufferung während der Wiedergabe aufgetreten ist.<br/>                      |
| [**bufferingProgress**](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)<br/> | Schreibgeschützt<br/>  | Ruft den Prozentsatz der abgeschlossenen Pufferung ab.<br/>                                       |
| [**bufferingTime**](wmplibiwmpnetwork-iwmpnetwork-bufferingtime--vb-and-c.md)<br/>         | Lesen/Schreiben<br/> | Ruft die Pufferzeit in Millisekunden ab, bevor die Wiedergabe beginnt, oder legt diese fest.<br/> |
| [**downloadProgress**](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)<br/>   | Schreibgeschützt<br/>  | Ruft den Prozentsatz des abgeschlossenen Downloads ab.<br/>                                     |
| [**encodedFrameRate**](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)<br/>   | Schreibgeschützt<br/>  | Ruft die vom Inhaltsautor angegebene Videobildrate ab.<br/>                        |
| [**frameRate**](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)<br/>                 | Schreibgeschützt<br/>  | Ruft die aktuelle Videobildrate ab.<br/>                                                |
| [**framesSkipped**](wmplibiwmpnetwork-iwmpnetwork-framesskipped--vb-and-c.md)<br/>         | Schreibgeschützt<br/>  | Ruft die Gesamtanzahl der Frames ab, die während der Wiedergabe übersprungen wurden.<br/>                          |
| [**lostPackets**](wmplibiwmpnetwork-iwmpnetwork-lostpackets--vb-and-c.md)<br/>             | Schreibgeschützt<br/>  | Ruft die Anzahl der verloren gegangenen Pakete ab.<br/>                                                  |
| [**Maxbandwidth**](wmplibiwmpnetwork-iwmpnetwork-maxbandwidth--vb-and-c.md)<br/>           | Lesen/Schreiben<br/> | Ruft die maximal zulässige Bandbreite ab oder legt sie fest.<br/>                                       |
| [**maxBitRate**](wmplibiwmpnetwork-iwmpnetwork-maxbitrate--vb-and-c.md)<br/>               | Schreibgeschützt<br/>  | Ruft die maximal mögliche Videobitrate ab.<br/>                                         |
| [**receivedPackets**](wmplibiwmpnetwork-iwmpnetwork-receivedpackets--vb-and-c.md)<br/>     | Schreibgeschützt<br/>  | Ruft die Anzahl der empfangenen Pakete ab.<br/>                                              |
| [**receptionQuality**](wmplibiwmpnetwork-iwmpnetwork-receptionquality--vb-and-c.md)<br/>   | Schreibgeschützt<br/>  | Ruft den Prozentsatz der Pakete ab, die in den letzten 30 Sekunden nicht verloren gegangen sind.<br/>                   |
| [**recoveredPackets**](wmplibiwmpnetwork-iwmpnetwork-recoveredpackets--vb-and-c.md)<br/>   | Schreibgeschützt<br/>  | Ruft die Anzahl der wiederhergestellten Pakete ab.<br/>                                             |
| [**sourceProtocol**](wmplibiwmpnetwork-iwmpnetwork-sourceprotocol--vb-and-c.md)<br/>       | Schreibgeschützt<br/>  | Ruft das Quellprotokoll ab, das zum Empfangen von Daten verwendet wird.<br/>                                    |



 

Verwenden Sie die folgende Eigenschaft, um eine **IWMPNetwork-Schnittstelle** zu erhalten.



| Object                                                                   | Eigenschaft                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------|
| [AxWindowsMediaPlayer-Objekt](axwindowsmediaplayer-object--vb-and-c.md) | [**Netzwerk**](axwmplib-axwindowsmediaplayer-network--vb-and-c.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen für Visual Basic .NET und C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





