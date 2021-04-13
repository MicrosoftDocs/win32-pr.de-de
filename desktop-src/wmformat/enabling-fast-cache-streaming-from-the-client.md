---
title: Aktivieren von schnellem Cache Streaming vom Client
description: Aktivieren von schnellem Cache Streaming vom Client
ms.assetid: 2a850d6f-8e1d-4aeb-9791-c51c3debf118
keywords:
- Windows Media-Format-SDK, Aktivieren von schnellem Cache Streaming
- Windows Media-Format-SDK, schnelles Cache Streaming
- Advanced Systems Format (ASF), Aktivieren von schnellem Cache Streaming
- ASF (Advanced Systems Format), Aktivieren von schnellem Cache Streaming
- Advanced Systems Format (ASF), schnelles Cache Streaming
- ASF (Advanced Systems Format), schnelles Cache Streaming
- Streams, Aktivieren von schnellem Cache Streaming
- Schnelles Cache Streaming, aktivieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3f8423a6f71b86ea91a05ed74b931eaa28a64be
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389865"
---
# <a name="enabling-fast-cache-streaming-from-the-client"></a>Aktivieren von schnellem Cache Streaming vom Client

Fast Cache ist eine Streamingtechnologie, bei der der-Server Inhalte in einer höheren Bitrate als die für die Wiedergabe benötigte Datenströme zustreamt.

Wenn die verfügbare Bandbreite höher ist als die Bitrate des Inhalts, werden schnelle Cache Datenströme mit höherer Geschwindigkeit gespeichert, und der Inhalt wird gepuffert. Dies trägt dazu bei, dass Unterbrechungen später reduziert werden, wenn das Netzwerk überlastet wird. Wenn die Netzwerkbandbreite niedriger ist als die Bitrate des Inhalts, puffert der schnelle Cache einen Teil der Daten, bevor die Wiedergabe gestartet wird. Der schnelle Cache wird für unzuverlässige Netzwerke (z. b. drahtlose Netzwerke) oder Netzwerke empfohlen, die große Schwankungen des Netzwerkverkehrs, z. b. Kabelmodems, aufweisen. Es wird auch für den Inhalt der Variable Bitrate (VBR) empfohlen. Die Bandbreitenanforderungen für VBR-Inhalte sind nicht konstant, und der Reader ermöglicht den Reader, den Datenstrom während der unteren Bitrate zu puffern.

Schnelles Cache Streaming wird nur für Bedarfs gesteuerte Inhalte unterstützt. Außerdem muss der Server so konfiguriert werden, dass er schnelles Cache Streaming verwendet.

Um den schnellen Cache im Reader-Objekt zu aktivieren, müssen Sie die Methoden [**IWMReaderNetworkConfig2:: setenablecontentcaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching) und [**IWMReaderNetworkConfig2:: setenablefastcache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache) mit dem Wert **true** aufrufen. Die erste Methode ermöglicht dem Reader das Zwischenspeichern von Streaming-Inhalten. Die zweite Option ermöglicht insbesondere die Verwendung von schnellem Cache.

Mit diesen Einstellungen aktiviert der Reader standardmäßig den schnellen Cache, wenn die Netzwerkbandbreite deutlich höher oder niedriger als die Bitrate des Inhalts ist und der Server diese unterstützt. Der Benutzer kann auch steuern, ob das Reader-Objekt einen schnellen Cache verwendet, indem er einen oder mehrere der folgenden modifiziererer zur URL hinzufügt.



| Modifizierer         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                      |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMCache          | Wenn dieser Modifizierer vorhanden ist, deaktiviert der Wert ' 0 ' explizit den schnellen Cache, während der Wert ' 1 ' dies explizit ermöglicht.                                                                                                                                                                                                                            |
| WMBitrate        | Dieser Modifizierer gibt die maximale Bitrate vom Server an. Dieser Modifizierer kann verwendet werden, um den schnellen Cache auf eine bestimmte Bandbreitenbeschränkung zu beschränken. Dieser Modifizierer wird ignoriert, wenn eine explizite Verbindungs Bandbreite bereits mit einem [**callmreadernetworkconfig:: setconnectionbandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth)-Befehl festgelegt wurde. |
| WMContentBitrate | Dieser Modifizierer gibt die Bitrate für den Inhalt an. Der Reader verwendet diesen Modifizierer, falls vorhanden, wenn er Datenströme aus einer MBR-Datei (Multiple Bitrate) auswählt. Dies kann dazu führen, dass der Leser mit hoher Bitrate Inhalte über eine langsame Verbindung empfängt, was zu sehr langen Pufferzeiten und Verzögerungen führt.                                          |



 

Der Modifizierer WMCache = 1 erzwingt, dass der Reader schnelles Cache Streaming verwendet, unabhängig von der Netzwerkbandbreite oder der Bitrate des Inhalts und unabhängig von vorherigen Aufrufen von " **abtenablefastcache**". Allerdings wird die Einstellung **setenablecontentcaching** für den Reader nicht überschrieben. Außerdem wird die Serverkonfiguration nicht überschrieben.

URL-Modifizierer haben folgende Form:

*URL*? *Modifizierer* = *Wert*

Beispiel:

MMS://MyServer/MyVideo.WMV? WMCache = 1

Es können mehrere Modifizierer angegeben werden. Verwenden Sie ein kaufmännisches und-(&), um Sie zu trennen:

MMS://MyServer/MyVideo.WMV? WMCache = 1&WMContentBitrate = (56.000

 

 




