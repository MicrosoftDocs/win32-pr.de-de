---
description: Informationen zum drahtlos gehosteten Netzwerk
ms.assetid: a6990759-9b84-4644-8f82-75aa63e8197b
title: Informationen zum drahtlos gehosteten Netzwerk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15be48bb5ef10754b11a0b3d4bb7d8e31ace9752
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216553"
---
# <a name="about-the-wireless-hosted-network"></a>Informationen zum drahtlos gehosteten Netzwerk

Das drahtlos gehostete Netzwerk ist ein neues WLAN-Feature, das unter Windows 7 und Windows Server 2008 R2 mit installiertem drahtlosen LAN-Dienst unterstützt wird. Diese Funktion implementiert zwei Hauptfunktionen:

-   Die Virtualisierung eines physischen drahtlosen Adapters in mehr als einem virtuellen drahtlos Adapter, der manchmal auch als virtuelles WLAN bezeichnet wird.
-   Ein softwarebasierter drahtlos Zugriffspunkt (AP), der manchmal als softap bezeichnet wird, der einen designierten virtuellen drahtlosen Adapter verwendet.

Diese beiden Funktionen sind gemeinsam in einem Windows-System vorhanden. Durch das Aktivieren oder Deaktivieren des drahtlos gehosteten Netzwerks werden sowohl virtuelle Wi-Fi als auch softap aktiviert oder deaktiviert. Es ist nicht möglich, diese beiden Funktionen separat in Windows zu aktivieren bzw. zu deaktivieren.

Mit dieser Funktion kann ein Windows-Computer einen einzelnen physischen drahtlosen Adapter verwenden, um eine Verbindung als Client mit einem Hardware Zugriffspunkt (Access Point, AP) herzustellen, während er gleichzeitig als Software-AP fungiert, die anderen drahtlos fähigen Geräten das Herstellen einer Verbindung ermöglicht. Diese Funktion erfordert, dass ein gehosteter netzwerkfähiger drahtlos Adapter auf dem lokalen Computer installiert ist. Der Treiber für den drahtlosen Adapter muss das von Microsoft für die Verwendung unter Windows 7 definierte drahtlose LAN-Gerätetreiber Modell implementieren. Um das Windows 7-Logo zu erhalten, muss ein drahtloser Treiber das Feature für drahtlos gehostete Netzwerke implementieren.

Es ist höchstens ein drahtlos gehosteter Netzwerk auf dem lokalen Computer aktiviert, und es wird nur ein drahtloser Adapter vom drahtlos gehosteten Netzwerk verwendet. Wenn es mehr als einen gehosteten netzwerkfähigen drahtlos Adapter gibt, wählt Windows einen Adapter für die Verwendung mit dem drahtlos gehosteten Netzwerk aus. Wenn die gehosteten Netzwerk-APIs verwendet werden, wird der gehostete netzwerkfähige drahtlos Adapter auf höchstens drei logische Adapter virtualisiert:

-   Ein Stations Adapter (STA) für die Verwendung durch Client-oder Ad-hoc-drahtlos Anwendungen. Der STA-Adapter erbt alle Einstellungen des ursprünglichen physischen drahtlos Adapters und weist das gleiche Verhalten wie der physische Adapter auf. Konzeptionell kann der STA-Adapter nach der Virtualisierung mit dem physischen Adapter identisch angezeigt werden. Der STA-Adapter befindet sich immer im System, solange der zugehörige drahtlose physische Adapter vorhanden ist.
-   Ein AP-Adapter, der vom drahtlos gehosteten Netzwerk zum Hosten von softap verwendet werden soll. Der AP-Adapter ist nur dann im Windows-System vorhanden, wenn das drahtlos gehostete Netzwerk zum ersten Mal aufgerufen wird (wenn die [**wlanhostednetworkstartusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)-, [**wlanhostednetworkforcestart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)-oder [**wlanhostednetworkinitsettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) -Funktion erstmalig aufgerufen wird). Nach der Erstellung verbleibt der AP-Adapter im System, bis das drahtlos gehostete Netzwerk deaktiviert ist. Wenn das drahtlos gehostete Netzwerk zu einem späteren Zeitpunkt aktiviert ist, wird der AP-Adapter erneut im System angezeigt.
-   Ein virtueller Stations Adapter (Virtual Station Adapter, VSTA), der von Hardwareanbietern verwendet wird, um die drahtlos gehostete Netzwerkfunktion in Windows zu erweitern. Der VSTA-Adapter ist optional und kann nur vom entsprechenden IHV-Dienst im System erstellt werden. Im Gegensatz zum AP-Adapter ist der VSTA-Adapter im Windows-System nur ab dem Zeitpunkt vorhanden, zu dem der IHV-Dienst den Adapter initialisiert, bis zum Zeitpunkt, zu dem der IHV-Dienst den Adapter freigibt.

Virtuelle Wi-Fi ordnet die logischen Adapter NDIS-Ports zu. Die Bindung der STA-, AP-und VSTA-Adapter an bestimmte NDIS-Ports wird von Windows getroffen. Der STA-Adapter ist immer an Port 0 gebunden. Der AP-Adapter wird beim Start der Virtualisierung an den nächsten verfügbaren NDIS-Port gebunden, und die Bindung bleibt unverändert, bis die Virtualisierung beendet ist, wenn das drahtlos gehostete Netzwerk deaktiviert ist. Der VSTA-Adapter ist an den nächsten verfügbaren NDIS-Port gebunden, wenn er vom entsprechenden IHV-Dienst initialisiert wird, und die Bindung bleibt unverändert, bis Sie vom IHV-Dienst veröffentlicht wird.

Der VSTA-Adapter kann für die Verwendung durch IHVs erstellt werden, ohne dass der softap-Adapter erstellt wird.

Die folgenden Kombinationen gelten für einen physischen Adapter mit Virtualisierung:

-   STA-Adapter.
-   STA-und AP-Adapter.
-   STA-und VSTA-Adapter.
-   STA-, AP-und VSTA-Adapter.

Mit Ausnahme des STA-Adapter Falls sind alle anderen Kombinationen nur gültig, wenn das drahtlos gehostete Netzwerk aktiviert ist. Wie bei einem einzelnen STA-Adapter Fall ist dies der physische Adapter, wenn das drahtlos gehostete Netzwerk deaktiviert ist. Wenn das drahtlos gehostete Netzwerk aktiviert ist, ist es der STA-Adapter, wenn das drahtlos gehostete Netzwerk nie im System aufgerufen wurde.

Layer 2-Bridging ist zwischen dem AP-Adapter und anderen Adaptern im System unzulässig. Die gleiche Einschränkung gilt für den VSTA-Adapter, wenn er im System vorhanden ist.

Das Feature für drahtlos gehostete Netzwerke in Windows implementiert einen softap. Diese softap ist jedoch nicht zum Ersetzen von hardwarebasierten drahtlosen AP-Geräten konzipiert. Insbesondere, wenn das drahtlos gehostete Netzwerk ausgeführt wird, wenn der Computer in den Standbymodus (Standby), Ruhezustand oder vor dem Neustart des Computers wechselt, wird das drahtlos gehostete Netzwerk angehalten. Das drahtlos gehostete Netzwerk wird nicht automatisch neu gestartet, nachdem der Computer aus dem Standbymodus, Ruhezustand oder Neustarts fortgesetzt wurde. Außerdem bietet softap keine DNS-Auflösung. Wenn ein externer DNS-Server nicht über die gemeinsame Nutzung der Internet Verbindung zur Verfügung gestellt wird (siehe Erörterung der folgenden ICS), voll qualifizierte Domänen Namen (Fully Qualified Domain Name, FQDN) zwischen zwei Computern oder Geräten, die mit dem softap verbunden sind, einschließlich des Computers, der als Host für den softap verwendet wird, funktionieren nur, wenn beide Entitäten den Netzwerktyp des softap-Netzwerks als privat markieren (Home oder work in der Netzwerk Kategorie Popup). Da der Computer, auf dem die softap gehostet wird, immer den softap-Netzwerktyp als privat kennzeichnet, müssen nur die mit softap verbundenen Computer oder Geräte den softap-Netzwerktyp als privat markieren, damit die FQDN-Auflösung funktioniert.

Softap-und Ad-hoc-Netzwerke schließen sich gegenseitig auf demselben physischen Adapter aus. Wenn softap auf dem AP-Adapter ausgeführt wird und ein Benutzer oder eine Anwendung Ad-hoc-Netzwerke auf dem STA-Adapter startet, wird softap heruntergefahren. Wenn das Ad-hoc-Netzwerk auf dem STA-Adapter ausgeführt wird, schlägt der Versuch fehl, das softap auf dem AP-Adapter zu starten.

Zum Schutz der Funkkommunikation zwischen dem Computer, der softap hostet, und den Geräten, die eine Verbindung mit dem softap herstellen, erfordert das drahtlos gehostete Netzwerk, dass alle Geräte mit der WPA2-PSK/AES-Verschlüsselungs Sammlung verbunden sind. Der gemeinsam verwendete Schlüssel ist ein 63-Zeichen Wert, der von Windows generiert wird, wenn das drahtlos gehostete Netzwerk zum ersten Mal aufgerufen wird (beim ersten Aufrufen der [**wlanhostednetworkstartusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)-, [**wlanhostednetworkforcestart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)-oder [**wlanhostednetworkinitsettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) -Funktion). Ein Benutzer oder eine Anwendung kann den Wert dieses gemeinsam genutzten Schlüssels nicht ändern. eine Anwendung kann jedoch anfordern, dass das Betriebssystem einen neuen Schlüssel erneut generiert, indem Sie die [**wlanhostednetworkrefreshsecuritysettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings) -Funktion aufrufen, oder ein Benutzer kann anfordern, dass das Betriebssystem einen neuen Schlüssel mithilfe von **Netsh WLAN** -Befehlen neu generieren kann. Dieser gemeinsam verwendete Schlüssel wird als primär-oder Systemschlüssel für das drahtlos gehostete Netzwerk bezeichnet und ist für das Starten und Beenden des drahtlos gehosteten Netzwerks persistent. Dieser Primärschlüssel wird in **Netsh WLAN** -Befehlen als "System Sicherheitsschlüssel" bezeichnet.

Um die Benutzerfreundlichkeit zu vereinfachen, unterstützt das drahtlos gehostete Netzwerk auch das Konzept eines sekundären oder Benutzer Sicherheits Schlüssels, der benutzerfreundlicher ist, aber weniger sicher ist. Dieser sekundäre Schlüssel wird in **Netsh WLAN** -Befehlen als "Benutzer Sicherheitsschlüssel" bezeichnet. Der sekundäre Schlüssel wird nicht von Windows generiert. Der Benutzer muss den Wert für diesen Schlüssel angeben. Ein Benutzer oder eine Anwendung kann den Schlüsselwert durch Aufrufen der [**wlanhostednetworksetsecondarykey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey) -Funktion oder mithilfe der **Netsh WLAN** -Befehle festlegen oder ändern. Der sekundäre Schlüssel kann als persistent oder temporär festgelegt werden. Wenn das drahtlos gehostete Netzwerk bereits ausgeführt wird, ist der sekundäre Schlüssel für einen temporären Schlüssel gültig, bis das drahtlos gehostete Netzwerk angehalten wird. Wenn das drahtlos gehostete Netzwerk nicht ausgeführt wird, ist es für einen temporären Schlüssel nur zwischen dem nächsten drahtlosen gehosteten Netzwerkstart und-Ende gültig.

Es gibt genau einen Primärschlüssel und höchstens einen sekundären Schlüssel für die drahtlos gehostete hetwork auf jedem Computer. Alle Geräte, die über Wi-Fi geschütztes Setup (WPS) bereitgestellt werden, erhalten den Primärschlüssel. Andere manuell konfigurierte Geräte können einen der beiden Schlüssel verwenden. Wenn ein Schlüssel geändert wird, kann jedes Gerät mit dem alten Schlüsselwert keine Verbindung mit dem drahtlos gehosteten Netzwerk herstellen, ohne dass der neue Schlüssel erneut bereitgestellt wird. Geräte mit dem anderen unveränderten Schlüssel können jedoch weiterhin eine Verbindung mit dem drahtlos gehosteten Netzwerk herstellen.

Eine Anwendung kann für drahtlos gehostete Netzwerk Benachrichtigungen registrieren, sodass eine WLAN-Benachrichtigung an den Anwendungs Rückruf gesendet wird, wenn sich die Eigenschaften im drahtlos gehosteten Netzwerk ändern. Eine Anwendung registriert sich für drahtlos gehostete Netzwerk Benachrichtigungen durch Aufrufen von [**wlanregisternotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification) mit dem Parameter *dwnotifsource* , um das \_ \_ hnwk-Bit der WLAN-Benachrichtigung einzuschließen \_ .

Windows bietet zwei Möglichkeiten für IT-Administratoren, das Feature für drahtlos gehostete Netzwerke zu verwalten. Für Computer, die Mitglieder einer Domäne sind, können Administratoren das drahtlos gehostete Netzwerk mithilfe der Gruppenrichtlinie nicht zulassen. Mithilfe von **Netsh WLAN** -Befehlen kann ein Administrator das drahtlos gehostete Netzwerk lokal auf dem Computer aktivieren bzw. deaktivieren.

## <a name="supported-scenarios-for-wireless-hosted-network"></a>Unterstützte Szenarien für drahtlos gehostete Netzwerke

Das drahtlos gehostete Netzwerk ermöglicht zwei Haupt Szenarien für Windows-Computer:

• Die Möglichkeit, ein drahtloses privates Netzwerk (drahtlos Schwenken) für die Verwendung mit verschiedenen anderen drahtlos Geräten bereitzustellen.

• Freigabe von Netzwerkverbindungen für die Verwendung durch andere Computer und Geräte.

Die drahtlos schwenken ist das primäre Szenario, das durch das drahtlos gehostete Netzwerk eigenständig aktiviert wird. Sobald das drahtlos gehostete Netzwerk auf einem Computer gestartet wurde, können alle drahtlos fähigen Geräte, die WPA2-PSK/AES unterstützen, mit dem softap verbinden, als ob eine Verbindung mit einer regulären Hardware-AP hergestellt werden soll. Geräte, die mit dem drahtlos gehosteten Netzwerk verbunden sind, bilden einen drahtlosen Schwenk, bei dem Sie Informationen mit dem Windows-Computer austauschen können, auf dem die softap-Funktionen gehostet werden.

Die Freigabe von Netzwerkverbindungen für die Verwendung durch andere Computer und Geräte erfordert die Verwendung von Internet Connection Sharing (ICS). In diesem Szenario ist die öffentliche Schnittstelle von ICS die gemeinsame Verbindung, während die private Schnittstelle der virtuelle Adapter ist, der die softap hostet. Bei der gemeinsam genutzten Verbindung kann es sich um eine Ethernet-, drahtlose LAN-oder drahtlose WAN-Verbindung handeln. Bei einer drahtlosen LAN-Verbindung kann die öffentliche Schnittstelle von ICS entweder von einem anderen drahtlosen LAN-Adapter oder vom virtuellen Stations Adapter auf demselben physischen drahtlosen Adapter, der die softap hostet, erfolgen. Die häufigste Verwendung für die Netzwerkfreigabe ist die gemeinsame Nutzung einer Internet Verbindung, bei der das Netzwerk auf der öffentlichen Schnittstelle von ICS Zugriff auf das Internet hat.

Das drahtlos gehostete Netzwerk interagiert mit Wi-Fi geschütztem Setup (WPS), einem weiteren wichtigen neuen Feature in Windows 7 und Windows Server 2008 R2 mit installiertem drahtlosen LAN-Dienst. Das drahtlos gehostete Netzwerk und WPS unterstützen ein Szenario, das ein WPS-fähiges Gerät für eine nicht-WPS-fähige Hardware-AP bereitstellt. In diesem Fall wird der auf Windows gehostete softap im Hintergrund aufgerufen, um das Hardware-AP-Profil auf das WPS-fähige Gerät zu überbringen.

## <a name="user-and-application-access-to-wireless-hosted-network"></a>Benutzer-und Anwendungs Zugriff auf drahtlos gehostete Netzwerke

Endbenutzer interagieren mit dem Feature für drahtlos gehostete Netzwerke in Windows mithilfe von Anwendungen von Drittanbietern oder **netsh** -Befehlen. Zurzeit gibt es keine systemeigene Benutzeroberfläche zum Konfigurieren oder Verwalten des drahtlos gehosteten Netzwerks unter Windows 7 oder Windows Server 2008 R2 mit installiertem drahtlosen LAN-Dienst.

Anwendungen von Drittanbietern und die **netsh** -Befehle basieren auf der Verwendung der öffentlichen drahtlos gehosteten Netzwerkfunktionen. Dieser Funktions Satz bietet einen umfassenden Satz von Funktionen zur Verwaltung des drahtlos gehosteten Netzwerks unter Windows 7 und Windows Server 2008 R2 mit installiertem drahtlosen LAN-Dienst.

Im folgenden finden Sie eine Liste der drahtlosen gehosteten Netzwerkfunktionen und die allgemeinen Aktionen von einem Endbenutzer-Standpunkt aus, die für die Funktion verwendet werden, die für verwendet wird:



| Verwendete Funktionen                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | BESCHREIBUNG                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WlanHostedNetworkForceStart_____WlanHostedNetworkStartUsing"></span><span id="wlanhostednetworkforcestart_____wlanhostednetworkstartusing"></span><span id="WLANHOSTEDNETWORKFORCESTART_____WLANHOSTEDNETWORKSTARTUSING"></span>[**Wlanhustednetworkforcestart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart), [ **wlanhustednetworkstartusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)<br/>                                                                                                                                                                                                                                                       | Starten Sie das drahtlos gehostete Netzwerk.<br/>                                                                                                                 |
| <span id="WlanHostedNetworkForceStop__WlanHostedNetworkStopUsing"></span><span id="wlanhostednetworkforcestop__wlanhostednetworkstopusing"></span><span id="WLANHOSTEDNETWORKFORCESTOP__WLANHOSTEDNETWORKSTOPUSING"></span>[**Wlanhustednetworkforcestop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop), [ **wlanhustednetworkstopusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)<br/>                                                                                                                                                                                                                                                                          | Hält das drahtlos gehostete Netzwerk an.<br/>                                                                                                                  |
| <span id="WlanHostedNetworkInitSettings__WlanHostedNetworkSetSecondaryKey__WlanHostedNetworkRefreshSecuritySettings"></span><span id="wlanhostednetworkinitsettings__wlanhostednetworksetsecondarykey__wlanhostednetworkrefreshsecuritysettings"></span><span id="WLANHOSTEDNETWORKINITSETTINGS__WLANHOSTEDNETWORKSETSECONDARYKEY__WLANHOSTEDNETWORKREFRESHSECURITYSETTINGS"></span>[**Wlanhustednetworkinitsettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings), [**wlanhustednetworksetsecondarykey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey), [**wlanhustednetworkrefreshsecuritysettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)<br/> | Konfigurieren Sie Einstellungen für drahtlos gehostete Netzwerke (ändern Sie die SSID, ändern Sie den sekundären Schlüssel, oder fordern Sie an, dass der Primärschlüssel erneut generiert wird).<br/>            |
| <span id="WlanHostedNetworkQueryStatus__WlanHostedNetworkQuerySecondaryKey__WlanHostedNetworkQueryProperty"></span><span id="wlanhostednetworkquerystatus__wlanhostednetworkquerysecondarykey__wlanhostednetworkqueryproperty"></span><span id="WLANHOSTEDNETWORKQUERYSTATUS__WLANHOSTEDNETWORKQUERYSECONDARYKEY__WLANHOSTEDNETWORKQUERYPROPERTY"></span>[**Wlanhustednetworkquerystatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus), [**wlanhustednetworkquerysecondarykey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey), [**wlanhustednetworkqueryproperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)<br/>                                              | Fragen Sie die Einstellungen und Informationen des drahtlos gehosteten Netzwerks ab (Status, SSID, Sekundär Schlüssel, Primärschlüssel oder eine Liste der Geräte, die derzeit verbunden sind).<br/> |



 

Die **netsh** -Befehle sind für die Verwendung durch erweiterte Benutzer oder Administratoren vorgesehen.

*Netsh.exe* verfügt über viele Unterbefehle für Drahtlos LAN. Eine umfassende Liste der Optionen für **netsh** und Wireless LAN finden Sie in der Eingabeaufforderung, indem Sie Folgendes eingeben:

**Netsh WLAN/?**

Die Dokumentation zu allen Netsh-Befehlen für Wireless LAN ist auch online auf TechNet verfügbar. Weitere Informationen finden Sie unter [Netsh Commands for Wireless Local Area Network (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).

Im folgenden finden Sie einige **netsh** -Befehle, die häufig mit für Drahtlos LAN und das drahtlos gehostete Netzwerk verwendet werden, obwohl andere Kombinationen von Befehlen unterstützt werden:



| Get-Help                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | BESCHREIBUNG                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="netsh_wlan_start_hostednetwork"></span><span id="NETSH_WLAN_START_HOSTEDNETWORK"></span>**Netsh WLAN starten von Host Network**<br/>                                                                                                                                                                                                                                                                                                                                     | Starten Sie das drahtlos gehostete Netzwerk.<br/>              |
| <span id="netsh_wlan_stop_hostednetwork"></span><span id="NETSH_WLAN_STOP_HOSTEDNETWORK"></span>**Netsh WLAN stoppt Host Netzwerk**<br/>                                                                                                                                                                                                                                                                                                                                        | Hält das drahtlos gehostete Netzwerk an.<br/>               |
| <span id="netsh_wlan_set_hostednetwork__mode__allow_disallow"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__MODE__ALLOW_DISALLOW"></span>**Netsh WLAN Set hustednetwork \[ Mode = \] Allow \| unallow**<br/>                                                                                                                                                                                                                                                                      | Aktivieren oder Deaktivieren des drahtlos gehosteten Netzwerks.<br/>  |
| <span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyUsage__persistent_temporary_"></span><span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyusage__persistent_temporary_"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__SSID___SSID___KEY___PASSPHRASE___KEYUSAGE__PERSISTENT_TEMPORARY_"></span>**Netsh WLAN Set Host Network \[ SSID = \] <ssid> \[ Key = \] <passphrase> \[ KeyUsage = \] persistent \| temporär** <br/> | Konfigurieren Sie die Einstellungen des drahtlos gehosteten Netzwerks.<br/> |
| <span id="netsh_wlan_refresh_hostednetwork___data___key"></span><span id="NETSH_WLAN_REFRESH_HOSTEDNETWORK___DATA___KEY"></span>**Netsh WLAN Refresh Host Network \[ Data = \] Key**<br/>                                                                                                                                                                                                                                                                                       | Aktualisieren Sie den Schlüssel des drahtlos gehosteten Netzwerks.<br/>        |
| <span id="netsh_wlan_show_hostednetwork___setting__security_"></span><span id="NETSH_WLAN_SHOW_HOSTEDNETWORK___SETTING__SECURITY_"></span>**Netsh WLAN Show Host Network \[ \[ Setting = \] Security\]**<br/>                                                                                                                                                                                                                                                                     | Anzeigen von Informationen zu drahtlosen gehosteten Netzwerken<br/>    |
| <span id="netsh_wlan_show_settings"></span><span id="NETSH_WLAN_SHOW_SETTINGS"></span>**Netsh WLAN-Anzeigeeinstellungen**<br/>                                                                                                                                                                                                                                                                                                                                                       | Anzeigen der globalen Einstellungen für Drahtlos LAN.<br/>           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von drahtlos gehosteter Netzwerk-und Internet Verbindungs Freigabe](using-hosted-network-and-internet-connection-sharing.md)
</dt> <dt>

[Beispiel für drahtlos gehostete Netzwerke](wireless-hosted-network-sample.md)
</dt> <dt>

[**Wlanhustednetworkforcestart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[**Wlanhustednetworkinitsettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[**Wlanhustednetworkqueryproperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[**Wlanhustednetworkquerysecondarykey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[**Wlanhustednetworkquerystatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[**Wlanhustednetworkrefreshsecuritysettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[**Wlanhustednetworksetproperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[**Wlanhustednetworksetsecondarykey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[**Wlanhustednetworkstartusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[**Wlanhustednetworkstopusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[**Wlanregistervirtualstationnotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 
