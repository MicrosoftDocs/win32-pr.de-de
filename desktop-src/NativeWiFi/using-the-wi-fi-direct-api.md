---
description: Zeigt, wie Wi-Fi Direct-Funktionen in Desktop-Apps verwendet werden.
ms.assetid: 50B95B7D-B860-44DF-8E78-1E7D2DC5A9B6
title: Verwenden der Wi-Fi Direct-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8850f5b278a158e32f78118cf5d0d408c123192e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358430"
---
# <a name="using-the-wi-fi-direct-functions"></a>Verwenden der Wi-Fi Direct-Funktionen

In diesem Thema wird gezeigt, wie Sie Wi-Fi Direct-Funktionen in Desktop-Apps verwenden. Ab Windows 8 und Windows Server 2012 wurden der systemeigenen WiFi-API Wi-Fi Direct-Funktionen hinzugefügt.

Die Wi-Fi Direct-Funktion basiert auf der Entwicklung der Wi-Fi Peer-to-Peer Technical Specification v 1.1 von der Wi-Fi Alliance (siehe [veröffentlichte Wi-Fi Alliance-Spezifikationen](https://www.wi-fi.org/)). Das Ziel der Wi-Fi Peer-to-Peer-technischen Spezifikation besteht darin, eine Lösung für die Wi-Fi Geräte-zu-Gerät-Konnektivität bereitzustellen, ohne dass ein drahtloser Zugriffspunkt (Wireless AP) zum Einrichten der Verbindung oder die Verwendung des vorhandenen Wi-Fi Ad-hoc-Mechanismus (IBSS) erforderlich ist.

> [!Note]  
> Der Ad-hoc-Modus ist möglicherweise in zukünftigen Versionen von Windows nicht verfügbar. Beginnen Sie mit Windows 8.1 und Windows Server 2012 R2, und verwenden Sie stattdessen Wi-Fi Direct.

 

Die folgenden Funktionen unterstützen die Wi-Fi Direct-Funktion.

-   [**Wfdcancelopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) : gibt an, dass die APP eine ausstehende [**wfdstartopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) -Funktion abbrechen möchte, die noch nicht abgeschlossen wurde.
-   [**Wfdclosehandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) : schließt ein Handle für den Wi-Fi Direct-Dienst.
-   [**Wfdclosesession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) : schließt eine Sitzung nach einem zuvor erfolgreichen Rückruf der [**wfdstartopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) -Funktion.
-   [**Wfdopenhandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) : öffnet ein Handle für den Wi-Fi Direct-Dienst und aushandiert eine Version der direkten Wi-Fi-API für die Verwendung von.
-   [**WF dopenlegacysession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) : Ruft ein gespeichertes Profil für ein Wi-Fi direktes Legacy Gerät ab und wendet es an.
-   [**Wfdstartopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) : startet eine Bedarfs gesteuerte Verbindung mit einem bestimmten Wi-Fi Direct-Gerät, das zuvor durch die Windows-Kopplung kombiniert wurde.
-   [**WF dupdatedevicevisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) : aktualisiert die Geräte Sichtbarkeit für die Wi-Fi direkte Geräteadresse für einen bestimmten installierten Wi-Fi direkt Geräteknoten.
-   [**WFD \_ \_Sitzung zum \_ abschließen \_ der Sitzung öffnen**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) : definiert die Rückruffunktion, die von der [**wfdstartopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) -Funktion aufgerufen wird, wenn der **wfdstartopensession** -Vorgang abgeschlossen wird.

Für eine Desktop-App erfordert die Wi-Fi Direct-Funktion, dass WLAN-Geräte zuvor vom Benutzer mit der Benutzeroberfläche der Windows-paarweise gekoppelt werden. Nachdem diese Kopplung abgeschlossen ist, wird ein Profil gespeichert, mit dem die Wi-Fi Direct-Funktionen zum Starten einer Wi-Fi direkten Sitzung verwendet werden können, um eine Verbindung zwischen den Wi-Fi direkt Geräten herzustellen.

Um Wi-Fi Direct verwenden zu können, muss eine App zunächst ein Handle für den Wi-Fi Direct-Dienst abrufen, indem Sie die [**wfdopenhandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) -Funktion aufrufen. Das von der **wfdopenhandle** -Funktion zurückgegebene Wi-Fi Direct-handle (WFD) wird für nachfolgende Wi-Fi direkte Funktionsaufrufe verwendet, die an den Wi-Fi Direct-Dienst gesendet werden.

Die [**wfdstartopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) -Funktion startet einen asynchronen Vorgang, um eine Bedarfs gesteuerte Verbindung mit einem bestimmten Wi-Fi Direct-Gerät zu starten. Das Ziel Wi-Fi Gerät muss zuvor mit der Windows-Kopplung gekoppelt sein. Wenn der asynchrone Vorgang abgeschlossen ist, wird die im *pfncallback* -Parameter angegebene Rückruffunktion aufgerufen.

Sobald eine Anwendung mit dem Wi-Fi Direct-Dienst ausgeführt wird, sollte die Anwendung die [**wfdclosehandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) -Funktion so anrufen, dass Sie an den Wi-Fi Direct-Dienst signalisiert, dass die Anwendung mit dem Dienst ausgeführt wird. Dies ermöglicht es dem Wi-Fi Direct-Dienst, von der Anwendung verwendete Ressourcen freizugeben.

Weitere Informationen zu Wi-Fi Direct für die Verwendung in Windows Store-Apps finden Sie unter " [**Peer Erfinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) " und verwandte Klassen im [**Windows. Networking. near**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) -Namespace.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Weitere Ressourcen**
</dt> <dt>

[Informationen zu nativem WiFi](about-native-wifi.md)
</dt> <dt>

[Informationen zur nativen WiFi-API](about-the-native-wifi-api.md)
</dt> <dt>

[Informationen über die Wi-Fi Direct-Funktion](about-the-wi-fi-direct-api.md)
</dt> <dt>

**Verweis**
</dt> <dt>

[**Peer Erfinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[**Rückruf für das Beenden der WFD- \_ \_ Sitzung \_ \_**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[**WF-cancelopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[**WF-CloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[**WF-CloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[**WF-openhandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[**WF-openlegacysession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[**WF-startopensession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[**WF dupdatedevicevisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 
