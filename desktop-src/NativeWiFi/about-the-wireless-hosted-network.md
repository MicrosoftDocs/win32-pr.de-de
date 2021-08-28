---
description: Informationen zum drahtlos gehosteten Netzwerk
ms.assetid: a6990759-9b84-4644-8f82-75aa63e8197b
title: Informationen zum drahtlos gehosteten Netzwerk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e88af34a1e0df2029c230b7b7800130d3b550dbf
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882770"
---
# <a name="about-the-wireless-hosted-network"></a>Informationen zum drahtlos gehosteten Netzwerk

Das drahtlose gehostete Netzwerk ist ein neues WLAN-Feature, das auf Windows 7 und auf Windows Server 2008 R2 mit installiertem WLAN-Dienst unterstützt wird. Dieses Feature implementiert zwei Hauptfunktionen:

-   Die Virtualisierung eines physischen Drahtlosadapters in mehrere virtuelle Drahtlosadapter, die manchmal als virtuelles WLAN bezeichnet werden.
-   Ein softwarebasierter drahtloser Zugriffspunkt (Wireless Access Point, AP), der manchmal als SoftAP bezeichnet wird und einen festgelegten virtuellen Drahtlosadapter verwendet.

Diese beiden Funktionen sind in einem Windows System gleichzeitig vorhanden. Durch das Aktivieren oder Deaktivieren des drahtlos gehosteten Netzwerks werden sowohl virtuelle Wi-Fi als auch SoftAP aktiviert oder deaktiviert. Es ist nicht möglich, diese beiden Funktionen in Windows separat zu aktivieren oder zu deaktivieren.

Mit diesem Feature kann ein Windows Computer einen einzelnen physischen Drahtlosadapter verwenden, um als Client eine Verbindung mit einem Hardwarezugriffspunkt (AP) herzustellen, während er gleichzeitig als Software-AP fungiert und anderen funkfähigen Geräten ermöglicht, eine Verbindung damit herzustellen. Dieses Feature erfordert, dass ein gehosteter Netzwerkadapter auf dem lokalen Computer installiert ist. Der Treiber für den Drahtlosadapter muss das von Microsoft definierte Wlan-Gerätetreibermodell für die Verwendung auf Windows 7 implementieren. Um das Logo Windows 7 zu erhalten, muss ein Drahtloser Treiber das Drahtlose Gehostete Netzwerkfeature implementieren.

Auf dem lokalen Computer ist höchstens ein drahtloses gehostetes Netzwerk aktiviert, und nur ein Drahtlosadapter wird vom drahtlos gehosteten Netzwerk verwendet. Wenn mehrere Drahtlosadapter für gehostete Netzwerke vorhanden sind, wählen Windows einen Adapter für die Verwendung mit dem drahtlos gehosteten Netzwerk aus. Wenn die Gehosteten Netzwerk-APIs verwendet werden, wird der gehostete Netzwerk-fähige Drahtlosadapter auf höchstens drei logische Adapter virtualisiert:

-   Ein Stationsadapter (STA) zur Verwendung durch Client- oder Ad-hoc-Funkanwendungen. Der STA-Adapter erbt alle Einstellungen des ursprünglichen physischen Drahtlosadapters und weist das gleiche Verhalten wie der physische Adapter auf. Konzeptionell kann der STA-Adapter nach der Virtualisierung als identisch mit dem physischen Adapter angezeigt werden. Der STA-Adapter befindet sich immer im System, solange der entsprechende physische Drahtlosadapter vorhanden ist.
-   Ein AP-Adapter für die Verwendung durch das drahtlos gehostete Netzwerk zum Hosten von SoftAP. Der AP-Adapter ist im Windows System erst vorhanden, nachdem das drahtlos gehostete Netzwerk zum ersten Mal aufgerufen wurde (wenn zuerst die [**WlanHostedNetworkStartUsing-,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) [**WlanHostedNetworkForceStart-**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)oder [**WlanHostedNetworkInitSettings-Funktion**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) aufgerufen wird). Nach der Erstellung verbleibt der AP-Adapter im System, bis das drahtlos gehostete Netzwerk deaktiviert ist. Wenn das drahtlos gehostete Netzwerk zu einem späteren Zeitpunkt aktiviert ist, wird der AP-Adapter erneut im System angezeigt.
-   Ein virtueller Stationsadapter (Virtual Station Adapter, VSTA), der von Hardwareanbietern verwendet werden kann, um die Drahtlose Hosted Network-Funktion in Windows zu erweitern. Der VSTA-Adapter ist optional und kann nur vom entsprechenden IHV-Dienst im System erstellt werden. Im Gegensatz zum AP-Adapter ist der VSTA-Adapter im Windows System nur ab dem Zeitpunkt vorhanden, zu dem der IHV-Dienst den Adapter initialisiert, bis der IHV-Dienst den Adapter freigibt.

Virtuelle Wi-Fi ordnet die logischen Adapter NDIS-Ports zu. Die Bindung der STA-, AP- und VSTA-Adapter an bestimmte NDIS-Ports wird durch Windows festgelegt. Der STA-Adapter ist immer an Port 0 gebunden. Der AP-Adapter wird beim Starten der Virtualisierung an den nächsten verfügbaren NDIS-Port gebunden, und die Bindung bleibt bis zum Ende der Virtualisierung gleich, wenn das drahtlos gehostete Netzwerk deaktiviert ist. Der VSTA-Adapter wird an den nächsten verfügbaren NDIS-Port gebunden, wenn er vom entsprechenden IHV-Dienst initialisiert wird und die Bindung so lange unverändert bleibt, bis sie vom IHV-Dienst freigegeben wird.

Es ist möglich, dass der VSTA-Adapter für die Verwendung durch IHVs erstellt wird, ohne den SoftAP-Adapter zu erstellen.

Die folgenden Kombinationen sind für einen physischen Adapter mit Virtualisierung gültig:

-   STA-Adapter.
-   STA- und AP-Adapter.
-   STA- und VSTA-Adapter.
-   STA-, AP- und VSTA-Adapter.

Mit Ausnahme des STA-Adapterfalls sind alle anderen Kombinationen nur gültig, wenn das drahtlos gehostete Netzwerk aktiviert ist. Wie bei einem einzelnen STA-Adapter handelt es sich um den physischen Adapter, wenn das drahtlos gehostete Netzwerk deaktiviert ist. Wenn das drahtlose gehostete Netzwerk aktiviert ist, ist es der STA-Adapter, wenn das drahtlos gehostete Netzwerk im System noch nie aufgerufen wurde.

Layer 2-Bridging ist zwischen dem AP-Adapter und anderen Adaptern im System nicht zulässig. Die gleiche Einschränkung gilt für den VSTA-Adapter, wenn er im System vorhanden ist.

Das Drahtlose Gehostete Netzwerkfeature in Windows implementiert ein SoftAP. Dieses SoftAP ist jedoch nicht dafür konzipiert, hardwarebasierte Drahtlos-AP-Geräte zu ersetzen. Insbesondere wenn das drahtlose gehostete Netzwerk ausgeführt wird, wenn der Computer in den Standbymodus wechselt, in den Ruhezustand versetzt wird oder bevor der Computer neu gestartet wird, wird das drahtlos gehostete Netzwerk beendet. Das drahtlos gehostete Netzwerk wird nicht automatisch neu gestartet, nachdem der Computer aus dem Standbymodus, ruhen oder neu gestartet wurde. Darüber hinaus stellt SoftAP die DNS-Auflösung nicht bereit. Wenn ein externer DNS-Server nicht über die Internetverbindungsfreigabe zur Verfügung gestellt wird (siehe ICS weiter unten), funktioniert die auflösung des vollqualifizierten Domänennamens (FQDN) zwischen zwei Computern oder Geräten, die mit softAP verbunden sind, einschließlich des Computers, auf dem die SoftAP gehostet wird, nur, wenn beide Entitäten den Netzwerktyp des SoftAP-Netzwerks als PRIVATE (HOME oder WORK in der Netzwerkkategorie pop-up) markieren. Da der Computer, auf dem SoftAP gehostet wird, den SoftAP-Netzwerktyp immer als PRIVATE markiert, müssen nur die Computer oder Geräte, die mit SoftAP verbunden sind, den SoftAP-Netzwerktyp als PRIVATE markieren, damit die FQDN-Auflösung funktioniert.

SoftAP- und Ad-hoc-Netzwerke schließen sich auf demselben physischen Adapter gegenseitig aus. Wenn SoftAP auf dem AP-Adapter ausgeführt wird und ein Benutzer oder eine Anwendung Ad-hoc-Netzwerke auf dem STA-Adapter startet, wird SoftAP heruntergefahren. Iif Ad-hoc-Netzwerke werden auf dem STA-Adapter ausgeführt. Ein Versuch, SoftAP auf dem AP-Adapter zu starten, schlägt fehl.

Um Schutz für die drahtlose Kommunikation zwischen dem Computer, auf dem SoftAP gehostet wird, und den Geräten, die eine Verbindung mit SoftAP herstellen, zu gewährleisten, erfordert das drahtlos gehostete Netzwerk, dass alle verbundenen Geräte die Cipher Suite WPA2-PSK/AES verwenden. Der gemeinsam verwendete Schlüssel ist ein 63-Zeichen-Wert, der von Windows generiert wird, wenn das drahtlos gehostete Netzwerk zum ersten Mal aufgerufen wird (wenn die [**WlanHostedNetworkStartUsing-,**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) [**WlanHostedNetworkForceStart-**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)oder [**WlanHostedNetworkInitSettings-Funktion**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) zuerst aufgerufen wird). Ein Benutzer oder eine Anwendung kann den Wert dieses gemeinsam verwendeten Schlüssels nicht ändern, aber eine Anwendung kann das Betriebssystem anfordern, einen neuen Schlüssel erneut zu generieren, indem sie die [**Funktion WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings) aufruft, oder ein Benutzer kann das Betriebssystem anfordern, einen neuen Schlüssel mit **netsh** wlan-Befehlen neu zu generieren. Dieser gemeinsam genutzte Schlüssel wird als Primär- oder Systemschlüssel für das drahtlos gehostete Netzwerk bezeichnet und ist beim Starten und Beenden des drahtlos gehosteten Netzwerks persistent. Dieser Primärschlüssel wird in **netsh** wlan-Befehlen als "Systemsicherheitsschlüssel" bezeichnet.

Zur Vereinfachung unterstützt das drahtlos gehostete Netzwerk auch das Konzept eines sekundären oder Benutzersicherheitsschlüssels, der benutzerfreundlicher, aber möglicherweise weniger sicher ist. Dieser sekundäre Schlüssel wird in **netsh** wlan-Befehlen als "Benutzersicherheitsschlüssel" bezeichnet. Der sekundäre Schlüssel wird nicht von Windows generiert. Der Benutzer muss den Wert für diesen Schlüssel bereitstellen. Ein Benutzer oder eine Anwendung kann den Schlüsselwert festlegen oder ändern, indem er die [**WlanHostedNetworkSetSecondaryKey-Funktion aufruft**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey) oder die **netsh wlan-Befehle** verwendet. Der sekundäre Schlüssel kann als persistent oder temporär festgelegt werden. Wenn das drahtlos gehostete Netzwerk bereits ausgeführt wird, ist der sekundäre Schlüssel für einen temporären Schlüssel gültig, bis das drahtlos gehostete Netzwerk beendet wird. Wenn das drahtlos gehostete Netzwerk für einen temporären Schlüssel nicht ausgeführt wird, ist es nur zwischen dem start- und stop-Start des nächsten drahtlos gehosteten Netzwerks gültig.

Es gibt genau einen Primärschlüssel und höchstens einen sekundären Schlüssel für das drahtlos gehostete Hetwork auf jedem Computer. Jedes Gerät, das über Wi-Fi Protected Setup (WPS) bereitgestellt wird, erhält den Primärschlüssel. Andere manuell konfigurierte Geräte können beide Schlüssel verwenden. Wenn ein Schlüssel geändert wird, kann jedes Gerät mit dem alten Schlüsselwert keine Verbindung mit dem drahtlos gehosteten Netzwerk herstellen, ohne mit dem neuen Schlüssel erneut bereitgestellt zu werden. Geräte mit dem anderen unveränderten Schlüssel müssen jedoch weiterhin eine Verbindung mit dem drahtlos gehosteten Netzwerk herstellen können.

Eine Anwendung kann sich für drahtlose Gehostete Netzwerkbenachrichtigungen registrieren, sodass eine WLAN-Benachrichtigung an den Anwendungsrückruf gesendet wird, wenn sich die Eigenschaften im drahtlos gehosteten Netzwerk ändern. Eine Anwendung registriert sich für drahtlose Gehostete Netzwerkbenachrichtigungen, indem sie [**wlanRegisterNotification aufruft,**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification) wobei der *dwNotifSource-Parameter* so festgelegt ist, dass er das WLAN \_ NOTIFICATION SOURCE \_ \_ HNWK-Bit enthält.

Windows bietet IT-Administratoren zwei Möglichkeiten, das Feature "Gehostetes Drahtlosnetzwerk" zu verwalten. Für Computer, die Mitglieder einer Domäne sind, können Administratoren gruppenrichtlinien verwenden, um das drahtlose gehostete Netzwerk zu verbieten. Mithilfe von **netsh** wlan-Befehlen kann ein Administrator das drahtlos gehostete Netzwerk lokal auf dem Computer aktivieren oder deaktivieren.

## <a name="supported-scenarios-for-wireless-hosted-network"></a>Unterstützte Szenarien für drahtlos gehostete Netzwerke

Das drahtlos gehostete Netzwerk ermöglicht zwei Hauptszenarien für Windows Computer:

• Die Möglichkeit, ein drahtloses Personal Area Network (Wireless PAN) für die Verwendung mit verschiedenen anderen Drahtlosen Geräten bereitzustellen.

• Gemeinsame Nutzung von Netzwerkverbindungen für andere Computer und Geräte.

Die drahtlose PAN ist das primäre Szenario, das vom drahtlos gehosteten Netzwerk selbst aktiviert wird. Sobald das drahtlose gehostete Netzwerk auf einem Computer gestartet wurde, kann jedes drahtlos fähige Gerät, das WPA2-PSK/AES unterstützt, eine Verbindung mit dem SoftAP herstellen, als ob es eine Verbindung mit einer regulären Hardware-AP herstellen würde. Geräte, die mit dem drahtlosen gehosteten Netzwerk verbunden sind, bilden eine drahtlose PAN, in der sie Informationen mit dem Windows Computer austauschen können, auf dem softAP gehostet wird, sowie untereinander.

Die Gemeinsame Nutzung von Netzwerkverbindungen für andere Computer und Geräte erfordert die Verwendung der Internetverbindungsfreigabe (Internet Connection Sharing, ICS). In diesem Szenario ist die öffentliche Schnittstelle von ICS die freigegebene Verbindung, während die private Schnittstelle der virtuelle Adapter ist, der softAP hostet. Bei der gemeinsam genutzten Verbindung kann es sich um eine Ethernet-, WLAN- oder WLAN-Verbindung handelt. Bei einer WLAN-Verbindung kann die öffentliche Schnittstelle von ICS entweder von einem anderen WLAN-Adapter oder vom virtuellen Stationsadapter auf demselben physischen Drahtlosadapter stammen, der softAP hostet. Die gängigste Verwendung für die Netzwerkfreigabe ist die Gemeinsame Nutzung einer Internetverbindung, bei der das Netzwerk an der öffentlichen Schnittstelle von ICS Zugriff auf das Internet hat.

Das drahtlos gehostete Netzwerk interagiert mit Wi-Fi Protected Setup (WPS), einem weiteren wichtigen neuen Feature in Windows 7 und Windows Server 2008 R2 mit installiertem WLAN-Dienst. Das drahtlos gehostete Netzwerk und WPS unterstützen ein Szenario, in dem ein WPS-fähiges Gerät für eine nicht WPS-fähige Hardware-AP bereitgestellt wird. In diesem Fall wird das auf Windows gehostete SoftAP im Hintergrund aufgerufen, um das Hardware-AP-Profil per Push auf das WPS-fähige Gerät zu übertragen.

## <a name="user-and-application-access-to-wireless-hosted-network"></a>Benutzer- und Anwendungszugriff auf drahtlos gehostetes Netzwerk

Endbenutzer interagieren in Windows mithilfe von Anwendungen von Drittanbietern oder **netsh-Befehlen** mit dem Feature "Gehostetes Drahtlosnetzwerk". Es gibt derzeit keine native Benutzeroberfläche zum Konfigurieren oder Verwalten des gehosteten Drahtlosnetzwerks auf Windows 7 oder auf Windows Server 2008 R2 mit installiertem Wlan-Dienst.

Anwendungen von Drittanbietern und die **Netsh-Befehle** basieren auf der Verwendung der Funktionen des öffentlichen drahtlos gehosteten Netzwerks. Dieser Satz von Funktionen bietet einen vollständigen Satz von Funktionen zum Verwalten des gehosteten Drahtlosnetzwerks auf Windows 7 und auf Windows Server 2008 R2 mit installiertem WLAN-Dienst.

Im Folgenden finden Sie eine Liste der drahtlos gehosteten Netzwerkfunktionen und der allgemeinen Aktionen aus Sicht des Endbenutzers, für die die Funktion verwendet wird:



| Verwendete Funktionen                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Beschreibung                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WlanHostedNetworkForceStart_____WlanHostedNetworkStartUsing"></span><span id="wlanhostednetworkforcestart_____wlanhostednetworkstartusing"></span><span id="WLANHOSTEDNETWORKFORCESTART_____WLANHOSTEDNETWORKSTARTUSING"></span>[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart), [ **WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)<br/>                                                                                                                                                                                                                                                       | Starten Sie das drahtlos gehostete Netzwerk.<br/>                                                                                                                 |
| <span id="WlanHostedNetworkForceStop__WlanHostedNetworkStopUsing"></span><span id="wlanhostednetworkforcestop__wlanhostednetworkstopusing"></span><span id="WLANHOSTEDNETWORKFORCESTOP__WLANHOSTEDNETWORKSTOPUSING"></span>[**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop), [ **WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)<br/>                                                                                                                                                                                                                                                                          | Beenden Sie das drahtlos gehostete Netzwerk.<br/>                                                                                                                  |
| <span id="WlanHostedNetworkInitSettings__WlanHostedNetworkSetSecondaryKey__WlanHostedNetworkRefreshSecuritySettings"></span><span id="wlanhostednetworkinitsettings__wlanhostednetworksetsecondarykey__wlanhostednetworkrefreshsecuritysettings"></span><span id="WLANHOSTEDNETWORKINITSETTINGS__WLANHOSTEDNETWORKSETSECONDARYKEY__WLANHOSTEDNETWORKREFRESHSECURITYSETTINGS"></span>[**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings), [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey), [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)<br/> | Konfigurieren Sie einstellungen für drahtlos gehostete Netzwerke (ändern Sie die SSID, ändern Sie den sekundären Schlüssel, oder fordern Sie an, dass der Primärschlüssel neu generiert wird).<br/>            |
| <span id="WlanHostedNetworkQueryStatus__WlanHostedNetworkQuerySecondaryKey__WlanHostedNetworkQueryProperty"></span><span id="wlanhostednetworkquerystatus__wlanhostednetworkquerysecondarykey__wlanhostednetworkqueryproperty"></span><span id="WLANHOSTEDNETWORKQUERYSTATUS__WLANHOSTEDNETWORKQUERYSECONDARYKEY__WLANHOSTEDNETWORKQUERYPROPERTY"></span>[**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus), [**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey), [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)<br/>                                              | Fragen Sie die Einstellungen und Informationen des gehosteten Drahtlosnetzwerks ab (Status, SSID, sekundärer Schlüssel, Primärschlüssel oder eine Liste der derzeit verbundenen Geräte).<br/> |



 

Die **netsh-Befehle** sind für die Verwendung durch fortgeschrittene Benutzer oder Administratoren vorgesehen.

*Netsh.exe* verfügt über viele Unterkombinationen für WLAN. Eine vollständige Liste der Optionen für **Netsh** und WLAN finden Sie an der Eingabeaufforderung, indem Sie Folgendes eingeben:

**netsh wlan /?**

Die Dokumentation zu allen Netsh-Befehlen für WLAN ist auch online auf Technet verfügbar. Weitere Informationen finden Sie unter [Netsh-Befehle für Wlan (Wireless Local Area Network).](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))

Im Folgenden sind einige **netsh-Befehle,** die häufig mit für Wlan und das drahtlos gehostete Netzwerk verwendet werden, obwohl andere Kombinationen von Befehlen unterstützt werden:



| Befehl                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Beschreibung                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="netsh_wlan_start_hostednetwork"></span><span id="NETSH_WLAN_START_HOSTEDNETWORK"></span>**netsh wlan start hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                     | Starten Sie das drahtlos gehostete Netzwerk.<br/>              |
| <span id="netsh_wlan_stop_hostednetwork"></span><span id="NETSH_WLAN_STOP_HOSTEDNETWORK"></span>**netsh wlan stop hostednetwork**<br/>                                                                                                                                                                                                                                                                                                                                        | Beenden Sie das drahtlos gehostete Netzwerk.<br/>               |
| <span id="netsh_wlan_set_hostednetwork__mode__allow_disallow"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__MODE__ALLOW_DISALLOW"></span>**netsh wlan set hostednetwork \[ mode= \] allow \| disallow**<br/>                                                                                                                                                                                                                                                                      | Aktivieren oder deaktivieren Sie das drahtlos gehostete Netzwerk.<br/>  |
| <span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyUsage__persistent_temporary_"></span><span id="netsh_wlan_set_hostednetwork__ssid___ssid___key___passphrase___keyusage__persistent_temporary_"></span><span id="NETSH_WLAN_SET_HOSTEDNETWORK__SSID___SSID___KEY___PASSPHRASE___KEYUSAGE__PERSISTENT_TEMPORARY_"></span>**netsh wlan set hostednetwork \[ ssid= \] &lt; ssid &gt; \[ key= \] &lt; passphrase &gt; \[ keyUsage= \] persistent \| temporary** <br/> | Konfigurieren Sie die Einstellungen für das drahtlos gehostete Netzwerk.<br/> |
| <span id="netsh_wlan_refresh_hostednetwork___data___key"></span><span id="NETSH_WLAN_REFRESH_HOSTEDNETWORK___DATA___KEY"></span>**netsh wlan refresh hostednetwork \[ data= \] key**<br/>                                                                                                                                                                                                                                                                                       | Aktualisieren Sie den drahtlos gehosteten Netzwerkschlüssel.<br/>        |
| <span id="netsh_wlan_show_hostednetwork___setting__security_"></span><span id="NETSH_WLAN_SHOW_HOSTEDNETWORK___SETTING__SECURITY_"></span>**netsh wlan show hostednetwork \[ \[ setting= \] security\]**<br/>                                                                                                                                                                                                                                                                     | Anzeigen von Drahtlosinformationen zum gehosteten Netzwerk.<br/>    |
| <span id="netsh_wlan_show_settings"></span><span id="NETSH_WLAN_SHOW_SETTINGS"></span>**netsh wlan show settings**<br/>                                                                                                                                                                                                                                                                                                                                                       | Anzeigen der globalen Wlan-Einstellungen.<br/>           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von drahtlos gehosteten Netzwerken und Freigabe von Internetverbindung](using-hosted-network-and-internet-connection-sharing.md)
</dt> <dt>

[Beispiel für drahtlos gehostetes Netzwerk](wireless-hosted-network-sample.md)
</dt> <dt>

[**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[**WlanHostedNetworkSetProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[**WLANRegisterVirtualStationNotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 
