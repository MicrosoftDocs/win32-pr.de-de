---
description: Zeigt die Verwendung Wi-Fi Direct-Funktionen in Desktop-Apps.
ms.assetid: 50B95B7D-B860-44DF-8E78-1E7D2DC5A9B6
title: Verwenden der Wi-Fi Direct-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa9a00a5474632ed54a84a7dc8cc5c64774e7cfe7547e6994acee599df2461ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684730"
---
# <a name="using-the-wi-fi-direct-functions"></a>Verwenden der Wi-Fi Direct-Funktionen

In diesem Thema wird gezeigt, wie Sie Wi-Fi Direct-Funktionen in Desktop-Apps verwenden. Ab Windows 8 und Windows Server 2012 wurden der Native Wifi-API Wi-Fi Direct-Funktionen hinzugefügt.

Das Wi-Fi Direct-Feature basiert auf der Entwicklung der Wi-Fi Peer-to-Peer Technical Specification v1.1 durch die Wi-Fi Alliance (siehe Veröffentlichte Spezifikationen der [Wi-Fi Alliance](https://www.wi-fi.org/)). Das Ziel der Wi-Fi Technischen Peer-zu-Peer-Spezifikation besteht darin, eine Lösung für Wi-Fi Gerät-zu-Gerät-Konnektivität bereitzustellen, ohne dass entweder ein Drahtloszugriffspunkt (Wireless-AP) zum Einrichten der Verbindung oder die Verwendung des vorhandenen Wi-Fi Ad-hoc-Mechanismus (IBSS) erforderlich ist.

> [!Note]  
> Der Ad-hoc-Modus ist in zukünftigen Versionen von Windows möglicherweise nicht mehr verfügbar. Verwenden Sie ab Windows 8.1 und Windows Server 2012 R2 stattdessen Wi-Fi Direct.

 

Die folgenden Funktionen unterstützen das Wi-Fi Direct-Feature.

-   [**WFDCancelOpenSession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) Gibt an, dass die App eine ausstehende [**WFDStartOpenSession-Funktion**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) abbrechen möchte, die nicht abgeschlossen wurde.
-   [**WFDCloseHandle:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) Schließt ein Handle für den Wi-Fi Direct-Dienst.
-   [**WFDCloseSession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) Schließt eine Sitzung nach einem zuvor erfolgreichen Aufruf der [**WFDStartOpenSession-Funktion.**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [**WFDOpenHandle:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) Öffnet ein Handle für den Wi-Fi Direct-Dienst und handelt eine Version der zu verwendenden WLAN Direct-API aus.
-   [**WFDOpenLegacySession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) Ruft ein gespeichertes Profil für ein Wi-Fi Direct-Legacygerät ab und wendet es an.
-   [**WFDStartOpenSession:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) Startet eine bedarfsorientierte Verbindung mit einem bestimmten Wi-Fi Direct-Gerät, das zuvor über die Windows-Kopplung gekoppelt wurde.
-   [**WFDUpdateDeviceVisibility:**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) Aktualisiert die Gerätesichtbarkeit für die Wi-Fi Direct-Geräteadresse für einen bestimmten installierten Wi-Fi Direct-Geräteknoten.
-   [**WFD \_ OPEN \_ SESSION \_ COMPLETE \_ CALLBACK:**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) Definiert die Rückruffunktion, die von der [**WFDStartOpenSession-Funktion**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) aufgerufen wird, wenn der **WFDStartOpenSession-Vorgang** abgeschlossen ist.

Für eine Desktop-App erfordert das Wi-Fi Direct-Feature, dass WLAN Direct-Geräte zuvor vom Benutzer mit der Benutzeroberfläche für die Windows-Kopplung gekoppelt wurden. Sobald diese Kopplung abgeschlossen ist, wird ein Profil gespeichert, mit dem die Wi-Fi Direct-Funktionen zum Starten einer Wi-Fi Direct-Sitzung verwendet werden können, um eine Verbindung zwischen den Wi-Fi Direct-Geräten herzustellen.

Um Wi-Fi Direct verwenden zu können, muss eine App zunächst ein Handle für den Wi-Fi Direct-Dienst abrufen, indem sie die [**WFDOpenHandle-Funktion**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) aufruft. Das von der **WFDOpenHandle-Funktion** zurückgegebene Wi-Fi Direct-Handle (WFD) wird für nachfolgende Wi-Fi Direct-Funktionsaufrufe an den Wi-Fi Direct-Dienst verwendet.

Die [**WFDStartOpenSession-Funktion**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) startet einen asynchronen Vorgang, um eine bedarfsorientierte Verbindung mit einem bestimmten Wi-Fi Direct-Gerät zu starten. Das Ziel Wi-Fi Geräts muss zuvor über die Windows-Kopplung gekoppelt worden sein. Nach Abschluss des asynchronen Vorgangs wird die im *pfnCallback-Parameter* angegebene Rückruffunktion aufgerufen.

Sobald eine Anwendung mithilfe des Wi-Fi Direct-Diensts fertig ist, sollte die Anwendung die [**WFDCloseHandle-Funktion**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) aufrufen, um dem Wi-Fi Direct-Dienst zu signalisieren, dass die Anwendung mit dem Dienst ausgeführt wird. Dadurch kann der Wi-Fi Direct-Dienst von der Anwendung verwendete Ressourcen freigeben.

Weitere Informationen zu Wi-Fi Direct für die Verwendung in Windows Store-Apps finden Sie unter [**PeerClass**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) und verwandte Klassen im [**Windows. Networking.Proximity-Namespace.**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Weitere Ressourcen**
</dt> <dt>

[Informationen zu Native Wifi](about-native-wifi.md)
</dt> <dt>

[Informationen zur Native Wifi-API](about-the-native-wifi-api.md)
</dt> <dt>

[Informationen zum Wi-Fi Direct-Feature](about-the-wi-fi-direct-api.md)
</dt> <dt>

**Referenz**
</dt> <dt>

[**Peer Peer Auserz**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
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

 

 
