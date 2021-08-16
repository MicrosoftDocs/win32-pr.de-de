---
title: Einrichten eines von der Quelle initiierten Abonnements
description: Mit quellenin initiierten Abonnements können Sie ein Abonnement auf einem Ereignissammlercomputer definieren, ohne die Ereignisquellencomputer zu definieren. Anschließend können mehrere Remoteereignisquellencomputer (mithilfe einer Gruppenrichtlinieneinstellung) eingerichtet werden, um Ereignisse an den Ereignissammlercomputer weiter zu übertragen.
ms.assetid: c02b5075-d685-44cf-937f-a1edfd2550ca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: f9d0ade037c0332f390bbea4c9f126f78f4172879fc50465fcf9e329e89fa23d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620650"
---
# <a name="setting-up-a-source-initiated-subscription"></a>Einrichten eines von der Quelle initiierten Abonnements

Mit quellenin initiierten Abonnements können Sie ein Abonnement auf einem Ereignissammlercomputer definieren, ohne die Ereignisquellencomputer zu definieren. Anschließend können mehrere Remoteereignisquellencomputer (mithilfe einer Gruppenrichtlinieneinstellung) eingerichtet werden, um Ereignisse an den Ereignissammlercomputer weiter zu übertragen. Dies unterscheidet sich von einem vom Collector initiierten Abonnement, da der Ereignissammler im vom Collector initiierten Abonnementmodell alle Ereignisquellen im Ereignisabonnement definieren muss.

Berücksichtigen Sie beim Einrichten eines von der Quelle initiierten Abonnements, ob sich die Ereignisquellencomputer in derselben Domäne wie der Ereignissammlercomputer befinden. In den folgenden Abschnitten werden die Schritte beschrieben, die sie ausführen müssen, wenn sich die Ereignisquellen in derselben Domäne oder nicht in derselben Domäne wie der Ereignissammlercomputer befinden.

> [!Note]  
> Jeder Computer in einer Domäne (lokal oder remote) kann ein Ereignissammler sein. Wenn Sie jedoch einen Ereignissammler auswählen, ist es wichtig, einen Computer auszuwählen, der sich topologisch in der Nähe des Orts befindet, an dem der Großteil der Ereignisse generiert wird. Das Senden von Ereignissen an einen Computer an einem entfernten Netzwerkstandort in einem WAN kann die Gesamtleistung und Effizienz bei der Ereignissammlung verringern.

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-in-the-same-domain-as-the-event-collector-computer"></a>Einrichten eines von der Quelle initiierten Abonnements, bei dem sich die Ereignisquellen in derselben Domäne wie der Ereignissammlercomputer befinden

Sowohl die Ereignisquellencomputer als auch der Ereignissammlercomputer müssen so konfiguriert werden, dass sie ein von der Quelle initiiertes Abonnement einrichten.

> [!Note]  
> Bei diesen Anweisungen wird davon ausgegangen, dass Sie Administratorzugriff auf den Windows Server-Domänencontroller haben, der die Domäne bedient, in der die Remotecomputer für die Erfassung von Ereignissen konfiguriert werden.

### <a name="configuring-the-event-source-computer"></a>Konfigurieren des Ereignisquellencomputers

1. Führen Sie den folgenden Befehl an einer Eingabeaufforderung mit erhöhten Rechten auf dem Windows Server-Domänencontroller aus, um Windows Remoteverwaltung zu konfigurieren:

    **winrm qc -q**

2. Starten Sie die Gruppenrichtlinie, indem Sie den folgenden Befehl ausführen:

    **%SYSTEMROOT% \\ System32 \\ gpedit.msc**

3. Erweitern Sie unter dem  Knoten **Computerkonfiguration** den Knoten Administrative Vorlagen Knoten , erweitern Sie dann den Knoten Windows **Komponenten,** und wählen Sie dann den Knoten **Ereignisweiterleitung** aus.

4. Klicken Sie mit der rechten Maustaste **auf die SubscriptionManager-Einstellung,** und wählen Sie **Eigenschaften aus.** Aktivieren Sie die **SubscriptionManager-Einstellung,** und klicken Sie auf **die Schaltfläche Anzeigen,** um der Einstellung eine Serveradresse hinzuzufügen. Fügen Sie mindestens eine Einstellung hinzu, die den Ereignissammlercomputer angibt. Das **Fenster SubscriptionManager-Eigenschaften** enthält eine **Registerkarte Erläuterung,** auf der die Syntax für die Einstellung beschrieben wird.

5. Nachdem die **SubscriptionManager-Einstellung** hinzugefügt wurde, führen Sie den folgenden Befehl aus, um sicherzustellen, dass die Richtlinie angewendet wird:

    **gpupdate /force**

### <a name="configuring-the-event-collector-computer"></a>Konfigurieren des Ereignissammlercomputers

1. Führen Sie den folgenden Befehl an einer Eingabeaufforderung mit erhöhten Rechten auf dem Windows Server-Domänencontroller aus, um Windows Remoteverwaltung zu konfigurieren:

    **winrm qc -q**

2. Führen Sie den folgenden Befehl aus, um den Event Collector-Dienst zu konfigurieren:

    **wecutil qc /q**

3. Erstellen Sie ein von der Quelle initiiertes Abonnement. Dies kann entweder programmgesteuert, mithilfe der -Ereignisanzeige oder mithilfe von [**Wecutil.exe.**](wecutil.md) Weitere Informationen zum programmgesteuerten Erstellen des Abonnements finden Sie im Codebeispiel unter [Creating a Source Initiated Subscription](creating-a-source-initiated-subscription.md). Wenn Sie Wecutil.exe verwenden, müssen Sie eine XML-Ereignisabonnementdatei erstellen und den folgenden Befehl verwenden:

    **wecutil cs** *configurationFile.xml*

    Der folgende XML-Code ist ein Beispiel für den Inhalt einer Abonnementkonfigurationsdatei, die ein von der Quelle initiiertes Abonnement erstellt, um Ereignisse aus dem Anwendungsereignisprotokoll eines Remotecomputers an das ForwardedEvents-Protokoll auf dem Ereignissammlercomputer weiter zu senden.

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <SubscriptionId>SampleSISubscription</SubscriptionId>
        <SubscriptionType>SourceInitiated</SubscriptionType>
        <Description>Source Initiated Subscription Sample</Description>
        <Enabled>true</Enabled>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

        <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
        <ConfigurationMode>Custom</ConfigurationMode>

        <Delivery Mode="Push">
            <Batching>
                <MaxItems>1</MaxItems>
                <MaxLatencyTime>1000</MaxLatencyTime>
            </Batching>
            <PushSettings>
                <Heartbeat Interval="60000"/>
            </PushSettings>
        </Delivery>

        <Expires>2018-01-01T00:00:00.000Z</Expires>

        <Query>
            <![CDATA[
                <QueryList>
                    <Query Path="Application">
                        <Select>Event[System/EventID='999']</Select>
                    </Query>
                </QueryList>
            ]]>
        </Query>

        <ReadExistingEvents>true</ReadExistingEvents>
        <TransportName>http</TransportName>
        <ContentFormat>RenderedText</ContentFormat>
        <Locale Language="en-US"/>
        <LogFile>ForwardedEvents</LogFile>
        <AllowedSourceNonDomainComputers></AllowedSourceNonDomainComputers>
        <AllowedSourceDomainComputers>O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)</AllowedSourceDomainComputers>
    </Subscription>
    ```

    > [!Note]  
    > Wenn allowedSourceDomainComputers, AllowedSourceNonDomainComputers/IssuerCAList, AllowedSubjectList und DeniedSubjectList beim Erstellen eines Quellabonnements leer sind, dann "O:NSG:NSD:(A;; GA;;;D C)(A;; ALLGEMEINES;;; NS)" wird als Standardsicherheitsdeskriptor für AllowedSourceDomainComputers verwendet. Der Standarddeskriptor gewährt Mitgliedern der Domänengruppe Domänencomputer sowie der lokalen Netzwerkdienstgruppe (für die lokale Weitergeleitete) die Möglichkeit, Ereignisse für dieses Abonnement zu erstellen.

### <a name="to-validate-that-the-subscription-works-correctly"></a>So überprüfen Sie, ob das Abonnement ordnungsgemäß funktioniert

1. Führen Sie auf dem Ereignissammlercomputer die folgenden Schritte aus:

    1. Führen Sie den folgenden Befehl an einer Eingabeaufforderung mit erhöhten Rechten auf dem Windows Server-Domänencontroller aus, um den Laufzeitstatus des Abonnements zu erhalten:

        **wecutil gr** *&lt; subscriptionID &gt;*

    2. Stellen Sie sicher, dass die Ereignisquelle verbunden ist. Möglicherweise müssen Sie warten, bis das in der Richtlinie angegebene Aktualisierungsintervall beendet ist, nachdem Sie das Abonnement für die Zu verbindende Ereignisquelle erstellt haben.
    3. Führen Sie den folgenden Befehl aus, um die Abonnementinformationen zu erhalten:

        **wecutil gs** *&lt; subscriptionID &gt;*

    4. Erhalten Sie den DeliveryMaxItems-Wert aus den Abonnementinformationen.

2. Geben Sie auf dem Ereignisquellencomputer die Ereignisse aus, die der Abfrage aus dem Ereignisabonnement entsprechen. Die DeliveryMaxItems-Anzahl von Ereignissen muss ausgelöst werden, damit die Ereignisse weitergeleitet werden.
3. Überprüfen Sie auf dem Ereignissammlercomputer, ob die Ereignisse an das ForwardedEvents-Protokoll oder an das im Abonnement angegebene Protokoll weitergeleitet wurden.

## <a name="forwarding-the-security-log"></a>Weiterleiten des Sicherheitsprotokolls

Um das Sicherheitsprotokoll weitergeleitet zu können, müssen Sie das NETWORK SERVICE-Konto der Gruppe EventLog-Leser hinzufügen.

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-not-in-the-same-domain-as-the-event-collector-computer"></a>Einrichten eines von der Quelle initiierten Abonnements, bei dem sich die Ereignisquellen nicht in derselben Domäne wie der Ereignissammlercomputer befinden

> [!Note]  
> Bei diesen Anweisungen wird davon ausgegangen, dass Sie über Administratorzugriff auf einen Windows Server-Domänencontroller verfügen. Da sich der oder die Remoteereignissammlercomputer in diesem Fall nicht in der Domäne befinden, die vom Domänencontroller bedient wird, ist es wichtig, einen einzelnen Client zu starten, indem Sie Windows Remoteverwaltung mithilfe von Diensten (services.msc) auf "automatisch" festlegen. Alternativ können Sie "winrm quickconfig" auf jedem Remoteclient ausführen.

Die folgenden Voraussetzungen müssen erfüllt sein, bevor das Abonnement erstellt wird.

1. Führen Sie auf dem Ereignissammlercomputer die folgenden Befehle an einer Eingabeaufforderung mit erhöhten Rechten aus, um Windows Remoteverwaltung und den Ereignissammlerdienst zu konfigurieren:

    **winrm qc -q**

    **wecutil qc /q**

2. Der Collectorcomputer muss über ein Serverauthentifizierungszertifikat (Zertifikat mit einem Serverauthentifizierungszweck) in einem Zertifikatspeicher des lokalen Computers verfügen.
3. Führen Sie auf dem Ereignisquellencomputer den folgenden Befehl aus, um Windows Remoteverwaltung zu konfigurieren:

    **winrm qc -q**

4. Der Quellcomputer muss über ein Clientauthentifizierungszertifikat (Zertifikat mit einem Clientauthentifizierungszweck) in einem Zertifikatspeicher des lokalen Computers verfügen.
5. Port 5986 wird auf dem Ereignissammlercomputer geöffnet. Führen Sie den folgenden Befehl aus, um diesen Port zu öffnen:

    **Netsh Firewall fügt TCP 5986 "Winrm HTTPS-Remoteverwaltung" hinzu**

### <a name="certificates-requirements"></a>Zertifikatanforderungen

- Ein Serverauthentifizierungszertifikat muss auf dem Event Collector-Computer im persönlichen Speicher des lokalen Computers installiert werden. Der Betreff dieses Zertifikats muss mit dem FQDN des Collectors übereinstimmen.
- Ein Clientauthentifizierungszertifikat muss auf den Ereignisquellencomputern im persönlichen Speicher des lokalen Computers installiert werden. Der Betreff dieses Zertifikats muss mit dem FQDN des Computers übereinstimmen.
- Wenn das Clientzertifikat von einer anderen Zertifizierungsstelle als dem ereignissammler ausgestellt wurde, müssen diese Stamm- und Zwischenzertifikate auch auf dem Ereignissammler installiert werden.
- Wenn das Clientzertifikat von einer Zwischenzertifizierungsstelle ausgestellt wurde und der Collector Windows 2012 oder höher ausgeführt wird, müssen Sie den folgenden Registrierungsschlüssel konfigurieren:

    **HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**
 
- Stellen Sie sicher, dass sowohl der Server als auch der Client den Sperrstatus für alle Zertifikate erfolgreich überprüfen können. Die Verwendung des **Befehls certutil** kann bei der Problembehandlung von Fehlern helfen.

Weitere Informationen finden Sie in diesem Artikel: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx

### <a name="setup-the-listener-on-the-event-collector"></a>Einrichten des Listeners auf dem Ereignissammler

1. Legen Sie die Zertifikatauthentifizierung mit dem folgenden Befehl fest:

    **winrm set winrm/config/service/auth @{Certificate="true"}**

2. Auf dem Ereignissammlercomputer sollte ein WinRM-HTTPS-Listener mit dem Fingerabdruck des Serverauthentifizierungszertifikats vorhanden sein. Dies kann mit dem folgenden Befehl überprüft werden:

    **winrm e winrm/config/listener**

3. Wenn der HTTPS-Listener nicht oder der Fingerabdruck des HTTPS-Listeners nicht mit dem Fingerabdruck des Serverauthentifizierungszertifikats auf dem Collectorcomputer identisch ist, können Sie diesen Listener löschen und einen neuen mit dem richtigen Fingerabdruck erstellen. Verwenden Sie den folgenden Befehl, um den HTTPS-Listener zu löschen:

    **winrm delete winrm/config/Listener? Address=*+Transport=HTTPS**

    Verwenden Sie den folgenden Befehl, um einen neuen Listener zu erstellen:

    **winrm create winrm/config/Listener? Address=&#42;+Transport=HTTPS @{Hostname="** &lt; _FQDN des Collectors_ &gt; **"; CertificateThumbprint="** &lt; _Fingerabdruck des Serverauthentifizierungszertifikats_ &gt; **"}**

### <a name="configure-certificate-mapping-on-the-event-collector"></a>Konfigurieren der Zertifikatzuordnung für den Ereignissammler

1. Erstellen Sie einen neuen lokalen Benutzer, und fügen Sie ihn der lokalen Gruppe Administratoren hinzu.
2. Erstellen Sie die Zertifikatzuordnung mithilfe eines Zertifikats, das im "Vertrauenswürdige Stammzertifizierungsstellen" oder "Zwischenzertifizierungsstellen" des Computers vorhanden ist.

    Dies ist das Zertifikat der Stamm- oder Zwischenzertifizierungsstelle, die die auf den Ereignisquellencomputern installierten Zertifikate ausgestellt hat (um Verwirrung zu vermeiden, ist dies die Zertifizierungsstelle direkt über dem Zertifikat in der *Zertifikatkette):*

    **winrm create winrm/config/service/certmapping?** Ausstellerfingerabdruck des ausstellenden Zertifizierungsstellenzertifikats = &lt;  &gt; **+Subject=&#42;+URI=&#42; @{UserName="** &lt; _username_ &gt; **"; Password="** &lt; _password_ &gt; **"} -remote:localhost**

3. Testen Sie auf einem Client den Listener und die Zertifikatzuordnung mit dem folgenden Befehl:

    **winrm g winrm/config -r:https://** &lt; _FQDN des Ereignissammlers_ &gt; **:5986 -a:certificate -certificate:"** &lt; _Fingerabdruck des Clientauthentifizierungszertifikats_ &gt; **"**

    Dadurch sollte die WinRM-Konfiguration des Ereignissammlers zurückgeben werden. **Verschieben Sie diesen** Schritt nicht, wenn die Konfiguration nicht angezeigt wird.

    **Was geschieht in diesem Schritt?**
    - Der Client stellt eine Verbindung mit dem Ereignissammler und sendet das angegebene Zertifikat.
    - Der Ereignissammler sucht nach der ausstellenden Zertifizierungsstelle und überprüft, ob die eine übereinstimmende Zertifikatzuordnung ist.
    - Der Ereignissammler überprüft die Clientzertifikatkette und den Sperrstatus.
    - Wenn die oben genannten Schritte erfolgreich sind, wird die Authentifizierung abgeschlossen.

> [!NOTE]
> Möglicherweise erhalten Sie einen Fehler Vom Zugriff verweigert, der sich über die Authentifizierungsmethode beschwert, was irreführend sein könnte. Überprüfen Sie zur Problembehandlung das CAPI-Protokoll beim Ereignissammler.

4. Listen Sie die konfigurierten Zertifikateinträge mit dem Befehl **winrm enum winrm/config/service/certmapping** auf.

### <a name="event-source-computer-configuration"></a>Konfiguration des Ereignisquellencomputers

1. Melden Sie sich mit einem Administratorkonto an, und öffnen Sie die Editor für lokale Gruppenrichtlinien (gpedit.msc).
2. Navigieren Sie zu Richtlinie für lokalen Computer\Computerkonfiguration\Administrative Vorlagen\Windows Komponenten\Ereignisweiterleitung.
3. Öffnen Sie die Richtlinie "Konfigurieren der Serveradresse, des Aktualisierungsintervalls und der Zertifizierungsstelle des Zertifikatausstellers eines Zielabonnement-Managers".
4. Aktivieren Sie die Richtlinie, und klicken Sie auf SubscriptionManagers "Show...". Schaltfläche.
5. Geben Sie im Fenster SubscriptionManagers die folgende Zeichenfolge ein:

    **Server=HTTPS://** &lt; _FQDN des Ereignissammlerservers_ &gt; **:5986/wsman/SubscriptionManager/WEC,Refresh=** &lt; _Aktualisierungsintervall in Sekunden_ &gt; **,IssuerCA=** &lt; _Fingerabdruck des ausstellenden Zertifizierungsstellenzertifikats_&gt;

6. Führen Sie die folgende Befehlszeile aus, um lokale Gruppenrichtlinie einstellungen zu aktualisieren:Gpupdate /force
7. Diese Schritte sollten das Ereignis 104 auf Ihrem Quellcomputer Ereignisanzeige Anwendungs- und Dienstprotokolle\Microsoft\Windows\Eventlog-ForwardingPlugin\Operational log mit der folgenden Meldung erzeugen:

    "Die Weiterleitung hat erfolgreich eine Verbindung mit dem Abonnement-Manager unter dem &lt; Adress-FQDN &gt; hergestellt, gefolgt von Ereignis 100 mit der Folgenden: "Das Abonnement &lt; sub_name wurde erfolgreich &gt; erstellt."

8. Auf dem Ereignissammler zeigt der Abonnementlaufzeitstatus jetzt 1 Aktiver Computer an.
9. Öffnen Sie das ForwardedEvents-Protokoll im Ereignissammler, und überprüfen Sie, ob die Ereignisse von den Quellcomputern weitergeleitet wurden.

### <a name="grant-permission-on-the-private-key-of-the-client-certificate-on-the-event-source"></a>Erteilen der Berechtigung für den privaten Schlüssel des Clientzertifikats für die Ereignisquelle

1. Öffnen Sie die Zertifikatverwaltungskonsole für Lokaler Computer auf dem Ereignisquellencomputer.
2. Klicken Sie mit der rechten Maustaste auf das Clientzertifikat und dann auf Private Schlüssel verwalten.
3. Erteilen Sie dem NETZWERKDIENSTbenutzer die Berechtigung Lesen.

### <a name="event-subscription-configuration"></a>Konfiguration des Ereignisabonnements

1. Öffnen Sie Ereignisanzeige im Ereignissammler, und navigieren Sie zum Knoten Abonnements.
2. Klicken Sie mit der rechten Maustaste auf Abonnements, und wählen Sie "Abonnement erstellen..." aus.
3. Geben Sie einen Namen und eine optionale Beschreibung für das neue Abonnement an.
4. Wählen Sie die Option "Quellcomputer initiiert" aus, und klicken Sie auf "Computergruppen auswählen...".
5. Klicken Sie unter Computergruppen auf "Domänenfremde Computer hinzufügen...". und geben Sie den Hostnamen der Ereignisquelle ein.
6. Klicken Sie auf "Zertifikate hinzufügen...". und fügen Sie das Zertifikat der Zertifizierungsstelle hinzu, die die Clientzertifikate ausstellt. Sie können auf Zertifikat anzeigen klicken, um das Zertifikat zu überprüfen.
7. Klicken Sie unter Zertifizierungsstellen auf OK, um das Zertifikat hinzuzufügen.
8. Klicken Sie nach Abschluss des Hinzufügens von Computer auf OK.
9. Kehren Sie zu den Abonnementeigenschaften zurück, und klicken Sie auf Ereignisse auswählen...
10. Konfigurieren Sie den Ereignisabfragefilter, indem Sie die Ereignisebenen, Ereignisprotokolle oder Ereignisquellen, die Ereignis-IDs und alle anderen Filteroptionen angeben.
11. Kehren Sie zu den Abonnementeigenschaften zurück, und klicken Sie auf Erweitert...
12. Wählen Sie eine der Optimierungsoptionen für die Ereignisübermittlung aus dem Quellereignis an den Ereignissammler aus, oder belassen Sie die Standardeinstellung Normal: 
    1. **Bandbreite minimieren:** Ereignisse werden übermittelt, um Bandbreite zu sparen.
    2. **Latenz minimieren:** Ereignisse werden übermittelt, sobald sie auftreten, um die Ereignislatenz zu reduzieren.
13. Ändern Sie das Protokoll in HTTPS, und klicken Sie auf OK.
14. Klicken Sie auf OK, um das neue Abonnement zu erstellen.
15. Überprüfen Sie den Laufzeitstatus des Abonnements, indem Sie mit der rechten Maustaste klicken und "Laufzeitstatus" auswählen.
