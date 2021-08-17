---
title: Informationen zu Geräten
description: Informationen zu Geräten
ms.assetid: 9e68c5eb-5fcb-4d7d-8dbb-7e951f253df8
keywords:
- Windows Media Player,Synchronisieren von Geräten
- Windows Media Player Objektmodell, Synchronisieren von Geräten
- Objektmodell, Synchronisieren von Geräten
- Windows Media Player ActiveX,Synchronisieren von Geräten
- ActiveX,Synchronisieren von Geräten
- Windows Media Player Mobile ActiveX,Synchronisieren von Geräten
- Windows Media Player Mobil,Synchronisieren von Geräten
- Synchronisieren von Geräten, Informationen
- Gerätesynchronisierung, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66383082bae772b48f913f6bd4615724de8f7b7735e387ba93407a9848f17074
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956920"
---
# <a name="about-devices"></a>Informationen zu Geräten

Portable Geräte sind Hardwaregeräte, die Benutzer verwenden, um digitale Medieninhalte zu nutzen, wenn sie sich nicht am Computer befinden. In der Regel werden tragbare Geräte im Akkubetrieb betrieben. Einige Geräte können nur Musik wieder geben. Andere Geräte können Videos und Musik wiederrufen.

Einige Geräte unterstützen die automatische Synchronisierung digitaler Medieninhalte mit Windows Media Player. Andere Geräte unterstützen nur die manuelle Übertragung. Sie können ermitteln, ob ein bestimmtes Gerät die automatische Synchronisierung unterstützt, indem Sie [IWMPSyncDevice::get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) aufrufen und dann den abgerufenen [WMPDeviceStatus-Wert](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) überprüfen. Wenn der abgerufene Wert **wmpdsManualDevice ist,** unterstützt das Gerät keine automatische Synchronisierung.

Sie können die Geräte aufzählen, die mit dem Computer des Benutzers verbunden sind. Verwenden Sie hierzu zunächst [IWMPSyncServices::get \_ deviceCount,](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) um die Anzahl der Geräte abzurufen. Rufen Sie dann in einer Schleife [IWMPSyncServices::getDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice)auf, und übergeben Sie jedes Mal den entsprechenden Indexwert. Sie können [IWMPSyncDevice::get \_ connected](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) verwenden, um zu bewerten, ob ein bestimmtes Gerät derzeit verbunden ist.

Um zu erfahren, wann Geräte eine Verbindung herstellen oder trennen, können Sie die **Ereignisse DeviceConnect** und **DeviceDisconnect** empfangen. Diese Ereignisse werden über die **IWMPEvents2-Schnittstelle** empfangen.

Die **IWMPSyncDevice-Schnittstelle stellt** zusätzliche Methoden bereit, mit denen Sie Informationen zu einem Gerät erhalten oder festlegen können. Beispiel:

-   Mit **den Methoden get \_ FriendlyName** und **put \_ FriendlyName** können Sie den benutzerdefinierten Gerätenamen abrufen und angeben.
-   Mit **der \_ get deviceName-Methode** können Sie den Gerätenamen abrufen, der Benutzern in der xp Windows angezeigt wird.
-   Mit **der getItemInfo-Methode** können Sie Metadaten von Geräten abrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zur Gerätesynchronisierung**](about-device-synchronization.md)
</dt> <dt>

[**IWMPEvents2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**IWMPSyncDevice-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**Arbeiten mit portablen Geräten**](working-with-portable-devices.md)
</dt> </dl>

 

 




