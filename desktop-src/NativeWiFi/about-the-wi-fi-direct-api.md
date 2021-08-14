---
description: Die Native Wifi-API enthält eine Reihe von Funktionen, die die Verwendung von Wi-Fi Direct für Desktop-Apps unterstützen.
ms.assetid: A649EBBA-1076-4426-9C4D-85AB8C415C66
title: Informationen zum Wi-Fi Direct-Feature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2816938b3e2d9156f2a97b67990386af2d5d780aa0226316cccc5edd0f2a4b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620208"
---
# <a name="about-the-wi-fi-direct-feature"></a>Informationen zum Wi-Fi Direct-Feature

Die Native Wifi-API enthält eine Reihe von Funktionen, die die Verwendung von Wi-Fi Direct für Desktop-Apps unterstützen. Ab Windows 8 und Windows Server 2012 wurden der Native Wifi-API Wi-Fi Direct-Funktionen hinzugefügt.

Das Wi-Fi Direct-Feature basiert auf der Entwicklung der Wi-Fi technischen Peer-to-Peer-Spezifikation v1.1 durch die Wi-Fi Alliance (siehe Veröffentlichte Spezifikationen der [Wi-Fi Alliance](https://www.wi-fi.org/)). Das Ziel der Wi-Fi Technischen Peer-zu-Peer-Spezifikation besteht darin, eine Lösung für Wi-Fi Gerät-zu-Gerät-Konnektivität bereitzustellen, ohne dass entweder ein Drahtloszugriffspunkt (Wireless Access Point, Drahtlos-AP) zum Einrichten der Verbindung oder die Verwendung des vorhandenen Wi-Fi Ad-hoc-Mechanismus (IBSS) erforderlich ist.

> [!Note]  
> Der Ad-hoc-Modus ist in zukünftigen Versionen von Windows möglicherweise nicht verfügbar. Verwenden Sie ab Windows 8.1 und Windows Server 2012 R2 stattdessen Wi-Fi Direct.

 

Für eine Desktop-App erfordert das Wi-Fi Direct-Feature, dass WLAN Direct-Geräte zuvor vom Benutzer mit der Benutzeroberfläche für Windows-Kopplung gekoppelt wurden. Sobald diese Kopplung abgeschlossen ist, wird ein Profil gespeichert, mit dem die Wi-Fi Direct-Funktionen zum Starten einer Wi-Fi Direct-Sitzung verwendet werden können, um eine Verbindung zwischen den Wi-Fi Direct-Geräten herzustellen.

Die folgenden Funktionen unterstützen das Wi-Fi Direct-Feature.

-   [**WFDCancelOpenSession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) Gibt an, dass die App eine ausstehende [**WFDStartOpenSession-Funktion**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) abbrechen möchte, die nicht abgeschlossen wurde.
-   [**WFDCloseHandle:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) Schließt ein Handle für den Wi-Fi Direct-Dienst.
-   [**WFDCloseSession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) Schließt eine Sitzung nach einem zuvor erfolgreichen Aufruf der [**WFDStartOpenSession-Funktion.**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [**WFDOpenHandle:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) Öffnet ein Handle für den Wi-Fi Direct-Dienst und handelt eine Version der zu verwendenden WLAN Direct-API aus.
-   [**WFDOpenLegacySession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) Ruft ein gespeichertes Profil für ein Wi-Fi Direct-Legacygerät ab und wendet es an.
-   [**WFDStartOpenSession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) Startet eine bedarfsorientierte Verbindung mit einem bestimmten Wi-Fi Direct-Gerät, das zuvor über die Windows-Kopplung gekoppelt wurde.
-   [**WFDUpdateDeviceVisibility:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) Aktualisiert die Gerätesichtbarkeit für die Wi-Fi Direct-Geräteadresse für einen bestimmten installierten Wi-Fi Direct-Geräteknoten.
-   [**WFD \_ OPEN \_ SESSION \_ COMPLETE \_ CALLBACK:**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) Definiert die Rückruffunktion, die von der [**WFDStartOpenSession-Funktion**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) aufgerufen wird, wenn der **WFDStartOpenSession-Vorgang** abgeschlossen ist.

Weitere Informationen zur Verwendung von Wi-Fi Direct in einer Desktop-App finden Sie unter [Verwenden der Wi-Fi Direct-Funktionen.](using-the-wi-fi-direct-api.md)

Weitere Informationen zu Wi-Fi Direct für die Verwendung in Windows Store-Apps finden Sie unter [**PeerClass**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) und verwandte Klassen im [**Windows. Networking.Proximity-Namespace.**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Weitere Ressourcen**
</dt> <dt>

[Informationen zu Native Wifi](about-native-wifi.md)
</dt> <dt>

[Informationen zur Native Wifi-API](about-the-native-wifi-api.md)
</dt> <dt>

[Informationen zur Drahtlosen Ad-hoc-API](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[Verwenden der Wi-Fi Direct-Funktionen](using-the-wi-fi-direct-api.md)
</dt> <dt>

**Referenz**
</dt> <dt>

[**Peer Auserwarte**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[**WFD \_ OPEN \_ SESSION \_ COMPLETE \_ CALLBACK**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 
