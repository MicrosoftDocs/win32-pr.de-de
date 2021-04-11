---
title: Verwenden von drahtlos gehosteten Netzwerken, Freigabe von Internet Verbindungen
description: Verwenden von drahtlos gehosteter Netzwerk-und Internet Verbindungs Freigabe
ms.assetid: 56e86ef8-f759-4e56-a591-74e03430125a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972774e921199e32eb70841c74c7478e2178cda9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959650"
---
# <a name="use-wireless-hosted-network-internet-connection-sharing"></a>Verwenden von drahtlos gehosteten Netzwerken, Freigabe von Internet Verbindungen

Das drahtlos gehostete Netzwerk ist ein neues WLAN-Feature, das unter Windows 7 und Windows 8 unterstützt wird. Sie wird auch unter Windows Server 2012 und Windows Server 2008 R2 mit installiertem drahtlosen LAN-Dienst unterstützt. Diese Funktion implementiert zwei Hauptfunktionen:

-   Die Virtualisierung eines physischen drahtlosen Adapters in mehr als einem virtuellen drahtlos Adapter, der manchmal auch als virtuelles WLAN bezeichnet wird.
-   Ein softwarebasierter drahtlos Zugriffspunkt (AP), der manchmal als softap bezeichnet wird, der einen designierten virtuellen drahtlosen Adapter verwendet.

Internet Connection Sharing (ICS) ist ein Feature in Windows, das über den SharedAccess-Dienst bereitgestellt wird. Mit Share daccess wird die Netzwerkfreigabe über einen Computer ermöglicht, auf dem der Zugriff auf das Internet nicht zwingend notwendig ist. In diesem Abschnitt wird der Begriff "ICS" und "SharedAccess" austauschbar verwendet, da die gemeinsame Nutzung der Internet Verbindung ein wichtiges Szenario für das drahtlos gehostete Netzwerk ist und der ICS-Begriff der Benutzer Community besser bekannt ist.

Das drahtlos gehostete Netzwerk ist eng an ICS gebunden, um sowohl das drahtlose Personal Area Network (Pan) als auch das Internet Freigabe Szenario zu ermöglichen. In diesem Abschnitt finden Sie allgemeine Empfehlungen für Anwendungsentwickler zum Integrieren von drahtlos gehosteten Netzwerken und ICS mithilfe des öffentlichen drahtlos gehosteten Netzwerks und der ICS-APIs.

## <a name="internet-connection-sharing"></a>Gemeinsame Nutzung der Internetverbindung

Der ICS-Dienst wird in einem der beiden möglichen Modi betrieben:

-   Eigenständiger Modus

    Nur die DHCPv4-Server Funktion wird ausgeführt, wenn der ICS-Dienst aufgerufen wird. Dabei handelt es sich um einen speziellen Betriebsmodus für ICS, der nur über das drahtlos gehostete Netzwerk verfügbar gemacht wird. Ein Benutzer oder eine Anwendung kann eigenständige ICS nicht direkt über öffentliche ICS-APIs oder **netsh** -Befehle starten und verhindern. Das Starten des drahtlos gehosteten Netzwerks umfasst in der Regel das Starten von ICS im eigenständigen Modus, damit die DHCPv4-Server Funktion private IPv4-Adressen für verbundene Geräte bereitstellt. Die Netzwerkkommunikation für die verbundenen Geräte ist auf das Senden und empfangen von Netzwerk Paketen zwischen einem verbundenen Gerät und dem lokalen Computer, der das drahtlos gehostete Netzwerk hostet, und den verbundenen Geräten selbst beschränkt. Dadurch wird das Netzwerkszenario für drahtlose Netzwerke für das drahtlos gehostete Netzwerk effektiv ermöglicht.

-   Vollständiger Modus

    Alle Features von ICS werden ausgeführt, wenn der Dienst aufgerufen wird, z. b. Netzwerk Adressübersetzung und DHCP-Serverfunktionen sowohl für IPv4 als auch für IPv6. Dies ist der normale Betriebsmodus für ICS. Ein Benutzer oder eine Anwendung kann den vollständigen ICS-Modus über öffentliche APIs oder NetShell-Befehle starten und Abbrechen. Dieser Dienst kann z. b. mithilfe von NET Stopp SharedAccess über eine Eingabeaufforderung mit erhöhten Rechten beendet werden. Durch die Kombination eines drahtlos gehosteten Netzwerks mit vollständigen ICS ist die Netzwerkkommunikation für die verbundenen Geräte nicht auf die drahtlose schwenken beschränkt. Alle verbundenen Geräte haben Zugriff auf das Netzwerk (z. b. das Internet) über die freigegebene Netzwerkverbindung des Computers, auf dem das drahtlos gehostete Netzwerk ausgeführt wird. Dadurch wird das Netzwerkfreigabe Szenario für das drahtlos gehostete Netzwerk effektiv ermöglicht.

In diesem Abschnitt verwenden wir den Begriff "vollständige ICS", um den Fall zu verwenden, in dem alle ICS-Funktionen im ICS-Dienst aufgerufen werden, um den Zugriff auf alle vollständigen ICS-Features mit dem drahtlos gehosteten Netzwerk zu ermöglichen.

Die zwei ICS-Betriebsmodi schließen sich gegenseitig aus, wenn vollständige ICS eine höhere Rangfolge hat. Der ICS-Dienst kann vom eigenständigen zum vollständigen Modus übergehen, jedoch nicht vom vollständigen zum eigenständigen Modus. Der eigenständige ICS-Modus wurde in Windows 7 und unter Windows Server 2008 R2 eingeführt, und der drahtlose LAN-Dienst wurde zusammen mit dem Feature für drahtlos gehostete Netzwerke installiert. Es ist in früheren Versionen von Windows nicht verfügbar.

Jeder vollständige ICS-Vorgang umfasst zwei verschiedene Netzwerkadapter im System:

-   Die öffentliche Schnittstelle. Dies ist die Netzwerkschnittstelle mit Zugriff auf das Internet. Dies ist die Schnittstelle, die der lokale Computer, auf dem ICS ausgeführt wird, verwendet, um das Internet für Clients und Geräte freizugeben, die per softap eine Verbindung
-   Die private Schnittstelle. Dies ist die Netzwerkschnittstelle, mit der andere Geräte eine Verbindung mit dem lokalen Computer herstellen, auf dem ICS ausgeführt wird. Auf dieser privaten Schnittstelle wird ein DHCPv4-Server ausgeführt, um den anderen Remote Computern private lokale IP-Adressen bereitzustellen.

Wenn die öffentliche Schnittstelle keinen Internet Zugriff hat, stellt der DHCP-Server auf der privaten Schnittstelle weiterhin lokale IP-Adressen für die verbundenen Geräte bereit. Eigenständige ICs beinhaltet nur die private Schnittstelle, auf der softap ausgeführt wird. Es umfasst keine öffentliche Schnittstelle.

Es ist höchstens eine Instanz der vollständigen ICS auf dem lokalen Computer vorhanden. Wenn bereits vollständige ICS auf dem lokalen Computer ausgeführt wird, zeigt das Starten einer anderen vollständigen ICS die folgenden funktionalen Verhaltensweisen an:

-   Wenn die öffentlichen und privaten Schnittstellen der neuen vollständigen ICS mit den vorhandenen vollständigen ICS identisch sind, ist das Starten der zweiten vollständigen ICS gleichbedeutend mit einem No-op-Vorgang.
-   Wenn sich die neue öffentliche Schnittstelle von der alten öffentlichen Schnittstelle unterscheidet, aber die neue private Schnittstelle mit der alten privaten Oberfläche identisch ist, hat das Starten einer zweiten vollständigen ICS wenig Auswirkungen auf die verbundenen Geräte auf derselben privaten Schnittstelle. Die Möglichkeit, auf das Internet zuzugreifen, kann sich mit der neuen öffentlichen Schnittstelle ändern.
-   Wenn sich die neue private Oberfläche von der alten privaten Schnittstelle unterscheidet, funktionieren die ICS-Funktionen nicht mehr an der alten privaten Oberfläche und wenden sich an die neue private Schnittstelle. Alle Remote Geräte, die über die alte Private Oberfläche eine Verbindung mit dem lokalen Computer herstellen, verlieren die IP-Konnektivität mit dem lokalen Computer.

Wenn vollständige ICS bereits ausgeführt wird, ist das Aufrufen einer zweiten vollständigen ICS eine Remote Verbindung mit Geräten, die die alte Private Oberfläche verwenden, solange die zweite ICS-Integration eine andere neue private Oberfläche verwendet.

Zum Verwalten und Verwenden des ICS-Dienstanbieter zur Unterstützung der ICS-Integration in drahtlos gehosteten Netzwerk muss eine Software Anwendung zunächst eine [**inetsharingmanager**](/windows/win32/api/netcon/nn-netcon-inetsharingmanager) -Schnittstelle abrufen. Die **inetsharingmanager** -Schnittstelle ermöglicht den direkten oder indirekten Zugriff auf alle anderen COM-Schnittstellen in der ICS-API. Die Methode " [**get \_ sharinginstem;**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_sharinginstalled) " in der **inetsharingmanager** -Schnittstelle meldet, ob der lokale Computer die Freigabe von Verbindungen unterstützt. Mit der [**get \_ enumeveryconnection**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_enumeveryconnection) -Methode für die **inetsharingmanager** -Schnittstelle wird eine Enumerationsschnittstelle für alle Verbindungen im Ordner "Connections" abgerufen. Die [**get \_ inetsharingconfigurationforinetconnection**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection) -Methode ruft eine [**inetsharingconfiguration**](/windows/win32/api/netcon/nn-netcon-inetsharingconfiguration) -Schnittstelle für die angegebene Verbindung ab. Methoden in der **inetsharingconfiguration** -Schnittstelle können zum Abfragen und Ändern von ICS-Einstellungen verwendet werden.

Das drahtlos gehostete Netzwerk muss gestartet werden, bevor die [**get \_ enumeveryconnection**](/windows/win32/api/netcon/nf-netcon-inetsharingmanager-get_enumeveryconnection) -Methode für die [**inetsharingmanager**](/windows/win32/api/netcon/nn-netcon-inetsharingmanager) -Schnittstelle aufgerufen wird, um alle Verbindungen im Ordner "Connections" aufzulisten.

Informationen zu ICS und den öffentlichen Schnittstellen und Methoden, die zum Abfragen und Ändern von ICS-Einstellungen verwendet werden können, finden Sie in der Dokumentation zur [gemeinsamen Nutzung der Internetverbindung und der Internet Verbindungs Firewall](/previous-versions/windows/desktop/ics/about-internet-connection-sharing-and-internet-connection-firewall).

## <a name="hosted-network-and-ics-integration"></a>Integration von gehosteten Netzwerken und ICS

Wenn vollständige ICS nicht ausgeführt wird, wird beim Starten eines drahtlos gehosteten Netzwerks der ICS-Dienst auch intern im eigenständigen Modus gestartet, wobei nur die DHCPv4-Server Funktion verwendet wird, um IP-Adressen für die verbundenen Geräte in der drahtlos gehosteten Netzwerkschnittstelle zuzuordnen Der Subnetzadressbereich für den eigenständigen DHCPv4-Server ist 192.168.173.0/24. Dies unterscheidet sich vom Subnetzbereich von 192.168.137.0/24, der mit vollständigen ICS verwendet wird.

Das Starten eines drahtlos gehosteten Netzwerks mit vollständiger ICS verwendet die folgende Logik:

-   Wenn vollständige ICS nicht bereits ausgeführt wird, wird durch das Starten eines drahtlos gehosteten Netzwerks auch der ICS-Dienst mit einem eigenständigen DHCPv4-Server gestartet.
-   Wenn bereits vollständige ICS ausgeführt wird und die private Schnittstelle die drahtlos gehostete Netzwerkschnittstelle ist, starten Sie einfach das drahtlos gehostete Netzwerk.
-   Wenn bereits vollständige ICS ausgeführt werden, die private Schnittstelle jedoch nicht die drahtlos gehostete Netzwerkschnittstelle ist, wird das drahtlos gehostete Netzwerk ohne die DHCPv4-Server Funktion auf der drahtlos gehosteten Netzwerkschnittstelle gestartet.

Die Auswirkung der obigen Logik verdeutlicht die folgenden Fakten:

-   ICS wechselt nicht vom vollständigen in den eigenständigen Modus.
-   Der eigenständige Modus kann nur vom drahtlos gehosteten Netzwerk aufgerufen werden, wenn ICS nicht im vollständigen Modus ausgeführt wird.
-   Wenn ICS im eigenständigen Modus ausgeführt wird, wird es vorzeitig in den vollständigen Modus verschoben, wenn ein Benutzer oder eine Anwendung ICS im vollständigen Modus startet.
-   Der Übergang von einem eigenständigen in den vollständigen Modus in ICS unterscheidet sich von verbundenen Geräten in der drahtlos schwenken, wenn die private Schnittstelle von vollständigen ICS nicht mit der von softap übereinstimmt.

Es dauert eine Weile, bis der ICS-Dienst auf dem lokalen Computer im vollständigen oder im eigenständigen Modus gestartet oder angehalten wird. Eine Anwendung sollte den Status des ICS-Dienstanbieter überprüfen, indem Sie die **NotifyServiceStatusChange** -Funktion verwendet, um sicherzustellen, dass der ICS-Dienst nicht vor dem Starten oder Beenden des drahtlos gehosteten Netzwerks für die Verwendung mit der ICS-Integration den Status Start/Stop Pending aufweist

## <a name="starting-and-stopping-the-wireless-hosted-network"></a>Starten und Beenden des drahtlos gehosteten Netzwerks

Windows stellt eine Plattform bereit, auf der mehrere gleichzeitige Anwendungen gleichzeitig ein drahtlos gehostetes Netzwerk verwalten dürfen. Insbesondere kann jede Anwendung das drahtlos gehostete Netzwerk eigenständig starten und unterbinden, ohne vorherige Kenntnisse über andere Anwendungen.

Es gibt zwei Sätze von Funktionen zum Starten und Abbrechen eines gehosteten Netzwerks.

Mehrere Anwendungen erfordern möglicherweise die Verwendung des drahtlos gehosteten Netzwerks. Die Funktionen [**wlanhostednetworkstartusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) und [**wlanhostednetworkstopusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) starten und beenden eine drahtlos gehostete Netzwerk eingehend eine Methode, die mit anderen gleichzeitigen Anwendungen kompatibel ist. Mit den Funktionen **wlanhostednetworkstartusing** und **wlanhostednetworkstopusing** kann eine Anwendung einen Verweis auf das drahtlos gehostete Netzwerk erhalten. Dieser Mechanismus sorgt dafür, dass das drahtlos gehostete Netzwerk ausgeführt wird, vorausgesetzt, dass mindestens eine andere Anwendung über einen aktuellen Verweis auf das drahtlos gehostete Netzwerk verfügt. Jeder Benutzer kann diese Funktionen aufzurufen. Erfolgreiche Aufrufe von **wlanhostednetworkstartusing** müssen durch Aufrufe der **wlanhostednetworkstopusing** -Funktion abgeglichen werden. Alle von der **wlanhostednetworkstartusing** -Funktion verursachten Änderungen des gehosteten Netzwerk Zustands werden automatisch rückgängig gemacht, wenn die aufrufende Anwendung das aufrufende handle schließt (indem [**wlanclosehandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle) mit dem gleichen *hclienthandle* -Parameter aufgerufen wird, der an **wlanhostednetworkstartusing** übergeben wurde) oder wenn der Prozess beendet wird.

Die Funktionen [**wlanhostednetworkforcestart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) und [**wlanhostednetworkforcestop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) erzwingen das Starten und Abbrechen eines drahtlos gehosteten Netzwerks. Diese Funktionen können nur aufgerufen werden, wenn der Benutzer über die entsprechende Berechtigung verfügt. Erfolgreiche Aufrufe von **wlanhostednetworkforcestart** können letztendlich durch einen Aufruf der **wlanhostednetworkforcestop** -Funktion in Abhängigkeit vom Anwendungs Entwurf abgeglichen werden. Diese Funktionen übertragen den drahtlos gehosteten Netzwerk Zustand, ohne die Anforderung dem aufrufenden Handle der Anwendung zuzuordnen. Alle von der **wlanhostednetworkforcestart** -Funktion verursachten Änderungen des gehosteten Netzwerk Zustands werden nicht automatisch rückgängig gemacht, wenn die aufrufende Anwendung das aufrufende handle schließt (durch Aufrufen von [**wlanclosehandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle) mit dem gleichen *hclienthandle* -Parameter, der an [**wlanhostednetworkstartusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)übergeben wird) oder wenn der Prozess beendet wird. Wenn die Anwendung, die die **wlanhostednetworkforcestart** -Funktion aufgerufen hat, geschlossen wird, ohne eine der Funktionen zum Abbrechen des drahtlos gehosteten Netzwerks aufzurufen, wird das gehostete Netzwerk weiterhin ausgeführt. Eine Anwendung kann die **wlanhostednetworkforcestart** -Funktion aufrufen, nachdem sichergestellt wurde, dass ein erhöhter Systembenutzer die erhöhten Energieanforderungen an die Ausführung des drahtlos gehosteten Netzwerks über einen längeren Zeitraum annimmt.

Die allgemeinen Empfehlungen, welche Funktionen zum Starten und Abbrechen eines drahtlos gehosteten Netzwerks aufgerufen werden müssen, lauten wie folgt:

-   Verwenden Sie die Funktionen [**wlanhostednetworkstartusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) und [**wlanhostednetworkstopusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) innerhalb einer Anwendung, um ein drahtlos gehostetes Netzwerk zu starten und zu beenden.
-   Verwenden Sie die [**wlanhostednetworkforcestart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) -Funktion nicht, um ein drahtlos gehostetes Netzwerk zu starten, es sei denn, es ist für die Anwendung unbedingt erforderlich. Die **wlanhostednetworkforcestart** -Funktion erfordert auch erhöhte Berechtigungen.
-   Verwenden Sie nur die [**wlanhostednetworkforcestop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) -Funktion als Wiederherstellungsmethode. Die Funktion **wlanhostednetworkforcestop** bewirkt, dass ein drahtlos gehostetes Netzwerk sofort beendet wird. Andere Anwendungen, die auf drahtlos gehostete Netzwerk Benachrichtigungen lauschen, müssen möglicherweise Wiederherstellungs Aktionen durchführen. Weitere Informationen finden Sie in der folgenden Erörterung der Wiederherstellungs Sequenz für drahtlos gehostete Netzwerke.

## <a name="start-sequence-for-wireless-hosted-network"></a>Start Sequenz für drahtlos gehostete Netzwerke

Für eine Anwendung, die ein drahtlos gehostetes Netzwerk mit vollständigem ICS startet, empfiehlt es sich, das drahtlos gehostete Netzwerk zu starten und dann vollständige ICS zu starten. Wenn bereits ein drahtlos gehosteter Netzwerk ausgeführt wird, sollte eine Anwendung die [**wlanhostednetworkforcestop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) -Funktion verwenden, um das drahtlos gehostete Netzwerk nur zu beenden, wenn vollständige ICS erforderlich ist, aber noch nicht aktiviert wurde, bevor das gehostete Netzwerk gestartet wurde. Dies ermöglicht es anderen Anwendungen, nach möglichen Störungen wieder hergestellt zu werden, die durch den Beginn vollständiger ICS verursacht werden. Weitere Informationen finden Sie in der folgenden Erörterung der Wiederherstellungs Sequenz für drahtlos gehostete Netzwerke. Der kombinierte Vorgang sollte erfolgreich sein und als Ganzes fehlschlagen.

> [!Note]  
> Das drahtlos gehostete Netzwerk muss gestartet werden, bevor versucht wird, den entsprechenden Adapter mithilfe der [**ienumnetsharingeveryconnection**](/windows/win32/api/netcon/nn-netcon-ienumnetsharingeveryconnection) -Schnittstelle aufzulisten.

 

Die folgenden geordneten Schritte sind die empfohlene Start Reihenfolge in einer Anwendung, die ein drahtlos gehostetes Netzwerk mit vollständiger ICS verwendet:

-   Wenden Sie die [**wlanhostednetworkinitsettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings) -Funktion an, um sicherzustellen, dass das drahtlos gehostete Netzwerk konfiguriert und einsatzbereit ist.
-   Wenden Sie die Funktionen [**wlanhostednetworkquerystatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus) und [**wlanhostednetworkqueryproperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty) an, um zu bestimmen, ob das drahtlos gehostete Netzwerk zugelassen und verfügbar ist. Wenn das drahtlos gehostete Netzwerk nicht zulässig und nicht verfügbar ist, wird ein Fehler zurückgegeben.
-   Überprüfen Sie, ob der für vollständige ICS verwendete ICS-Dienst zulässig ist. Wenn der ICS-Dienst nicht gestartet werden kann, wird ein Fehler zurückgegeben.
-   Aufrufen der [**wlanhostednetworkforcestop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) -Funktion, um eine Beendigung des drahtlos gehosteten Netzwerks zu erzwingen.
-   Rufen Sie die [**wlanhostednetworkstartusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) -Funktion auf, um das drahtlos gehostete Netzwerk zu starten.
-   Wenn das drahtlos gehostete Netzwerk nicht gestartet werden kann, wird ein Fehler zurückgegeben.
-   Wenn vollständige ICS bereits ausgeführt wird und sich die aktuelle öffentliche oder private Schnittstelle von der zu verwendenden neuen Schnittstelle unterscheidet, können Sie die aktuellen öffentlichen und privaten Schnittstellen Zwischenspeichern. Eine Anwendung kann auch einen Fehler zurückgeben oder den Benutzer auffordern, wenn die ICS-Integration bereits ausgeführt wird.
-   Starten Sie vollständige ICS mit den neuen Einstellungen für die öffentlichen und privaten Schnittstellen.
-   Wenn vollständige ICS mit diesen Einstellungen nicht gestartet werden kann, versuchen Sie, den vollständigen ICS-Dienst mit den zwischengespeicherten öffentlichen und privaten Schnittstellen zu starten, wenn vollständige ICS zuvor ausgeführt wurde Aufrufen der [**wlanhostednetworkforcestop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) -Funktion zum Beenden des drahtlos gehosteten Netzwerks und Zurückgeben eines Fehlers.
-   Zurückgeben, dass das drahtlos gehostete Netzwerk und die vollständige ICS erfolgreich sind.

## <a name="stop-sequence-for-wireless-hosted-network"></a>Sequenz für drahtlos gehosteten Netzwerk Vorgang abbrechen

Bei der Verwendung eines drahtlos gehosteten Netzwerks mit vollständigem ICS kann eine Anwendung, deren Arbeit abgeschlossen ist, das drahtlos gehostete Netzwerk und den für vollständige ICS verwendeten ICS-Dienst beenden. In diesem Fall wird empfohlen, dass die [**wlanhostednetworkforcestop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) -Funktion aufgerufen wird, um das gehostete Netzwerk zu beenden, anstatt die [**wlanhostednetworkstopusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) -Funktion aufzurufen. Die **wlanhostednetworkforcestop** -Funktion hält das drahtlos gehostete Netzwerk an und ermöglicht es auch, andere Anwendungen wiederherzustellen. Weitere Informationen finden Sie in der folgenden Erörterung der Wiederherstellungs Sequenz für drahtlos gehostete Netzwerke.

Die folgenden geordneten Schritte sind die empfohlene Endzeit in einer Anwendung, die drahtlos gehostete Netzwerke und vollständige ICS verwendet:

-   Beendet vollständige ICS.
-   Aufrufen der [**wlanhostednetworkforcestop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) -Funktion zum Abbrechen des drahtlos gehosteten Netzwerks.

Eine Anwendung, die drahtlos gehostete Netzwerke ohne vollständige ICS verwendet, die mit der Arbeit fertig sind, muss lediglich die [**wlanhostednetworkstopusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing) -oder [**wlanhostednetworkforcestop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop) -Funktion aufrufen, um das drahtlos gehostete Netzwerk anzuhalten. Wenn die [**wlanhostednetworkstartusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) -Funktion aufgerufen wurde, um das drahtlos gehostete Netzwerk zu starten, sollte die Anwendung die **wlanhostednetworkstopusing** -Funktion aufrufen, um das drahtlos gehostete Netzwerk zu beenden. Wenn das drahtlos gehostete Netzwerk bereits gestartet wurde, bevor die Anwendung oder die Anwendung die [**wlanhostednetworkforcestart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) -Funktion aufgerufen hat, um den Start des drahtlos gehosteten Netzwerks zu erzwingen, kann die Anwendung die **wlanhostednetworkforcestop** -Funktion aufrufen, um das drahtlos gehostete Netzwerk anzuhalten, oder es kann keine Aktion durchführen, wenn das drahtlos

## <a name="recovery-sequence-for-wireless-hosted-network"></a>Wiederherstellungs Sequenz für drahtlos gehostete Netzwerke

Eine Anwendung, die das drahtlos gehostete Netzwerk verwendet, kann von den Aktionen anderer Anwendungen betroffen sein. Der ICS-Dienst und die-Schnittstellen für die Verwaltung von ICS bieten keine Methode, mit der eine Anwendung für ICS-Änderungs Benachrichtigungen registriert wird. Wenn eine andere Anwendung die Methoden [**enablesharing**](/windows/win32/api/netcon/nf-netcon-inetsharingconfiguration-enablesharing) oder [**DisableSharing**](/windows/win32/api/netcon/nf-netcon-inetsharingconfiguration-disablesharing) in der [**inetsharingconfiguration**](/windows/win32/api/netcon/nn-netcon-inetsharingconfiguration) -Schnittstelle aufruft, um die Freigabe für eine Verbindung zu aktivieren oder zu deaktivieren, wird eine Meldung an die Benutzeroberfläche (der Bildschirm) auf dem lokalen Computer gesendet, nicht an andere Anwendungen. Daher muss sich eine Anwendung auf die drahtlos gehosteten Netzwerk Benachrichtigungen stützen, um Wiederherstellungs Aktionen auszuführen, wenn ICS oder drahtlos gehostete Netzwerk Änderungen auftreten.

Eine Anwendung, die das drahtlos gehostete Netzwerk verwendet, sollte sich für drahtlos gehostete Netzwerk Benachrichtigungen registrieren, indem [**wlanregisternotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)aufgerufen wird. Wenn nur Benachrichtigungen für drahtlos gehostete Netzwerke erforderlich sind, sollte die Anwendung die **WLAN- \_ Benachrichtigungs \_ Quelle \_ hnwk** im *dwnotifsource* -Parameter übergeben, der an **wlanregisternotification** übergeben wird. Wenn auch andere drahtlose Benachrichtigungen erforderlich sind, muss die **WLAN- \_ Benachrichtigungs \_ Quelle- \_ hnwk** mit den Benachrichtigungs Quellen Konstanten für andere Typen von drahtlos Benachrichtigungen kombiniert werden, und dieser Wert wird im *dwnotifsource* -Parameter übergeben.

Die Wiederherstellungs Sequenz ist für Anwendungen mit oder ohne vollständige ICS identisch und geht davon aus, dass Anwendungen den ICS-Dienst nicht erneut starten möchten. Gehen Sie nach dem Empfang einer drahtlosen gehosteten Netzwerk Benachrichtigung, dass das gehostete Netzwerk beendet wurde, wie folgt vor:

-   Wenn die Anwendung [**wlanhostednetworkforcestart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart) aufgerufen hat, um das drahtlos gehostete Netzwerk zu starten, starten Sie das gehostete Netzwerk durch Aufrufen von **wlanhostednetworkforcestart** neu. Rufen Sie andernfalls [**wlanhostednetworkstartusing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing) auf, um das drahtlos gehostete Netzwerk neu zu starten.

## <a name="recovery-sequence-for-connected-devices"></a>Wiederherstellungs Sequenz für verbundene Geräte

Remote Geräte oder Computer, die mit dem drahtlos gehosteten Netzwerk verbunden sind, können von den Aktionen anderer Anwendungen betroffen sein, die sich auf ICS und das drahtlos gehostete Netzwerk auswirken. Glücklicherweise haben die meisten Geräte eine Wiederholungs Logik in der Geräte Anwendung erstellt, um einen vorübergehenden Ausfall von Signal oder Roaming zu umgehen.

Eine mögliche Wiederherstellungs Sequenz für Geräte oder Computer, die mit dem drahtlos gehosteten Netzwerk verbunden sind, das den Kontakt verliert, ist folgender:

-   Der Treiber für drahtlose Geräte gibt an, dass ein Medium die Verbindung mit den oberen Ebenen des Netzwerk Stapels auf dem Gerät trennt.
-   Die Geräte Anwendung startet regelmäßige Überprüfungen auf die Verfügbarkeit des drahtlos gehosteten Netzwerks.
-   Sobald die Geräte Anwendung das drahtlos gehostete Netzwerk wieder erkennt, initiiert das Gerät eine drahtlos Verbindung.
-   Bei einer erfolgreichen Verbindung mit dem drahtlos gehosteten Netzwerk werden die IP-Einstellungen von der Geräte Anwendung entsprechend aktualisiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum drahtlos gehosteten Netzwerk](about-the-wireless-hosted-network.md)
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

 

 
