---
title: Einrichten eines von der Quelle initiierten Abonnements
description: Mit Quellen initiierten Abonnements können Sie ein Abonnement auf einem Ereignis Sammler Computer definieren, ohne die Ereignis Quellcomputer zu definieren. Anschließend können mehrere Remote Ereignis Quellcomputer eingerichtet werden (mithilfe einer Gruppenrichtlinien Einstellung), um Ereignisse an den Ereignis Sammler Computer weiterzuleiten.
ms.assetid: c02b5075-d685-44cf-937f-a1edfd2550ca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: de31b23821fb1315a690612e5b337c5bb47a016d
ms.sourcegitcommit: 39a48585ed40e1cb466dcbf085847d0eb10f0da7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/04/2020
ms.locfileid: "104390116"
---
# <a name="setting-up-a-source-initiated-subscription"></a>Einrichten eines von der Quelle initiierten Abonnements

Mit Quellen initiierten Abonnements können Sie ein Abonnement auf einem Ereignis Sammler Computer definieren, ohne die Ereignis Quellcomputer zu definieren. Anschließend können mehrere Remote Ereignis Quellcomputer eingerichtet werden (mithilfe einer Gruppenrichtlinien Einstellung), um Ereignisse an den Ereignis Sammler Computer weiterzuleiten. Dies unterscheidet sich von einem vom Collector initiierten Abonnement, da der Ereignis Sammler im vom Collector initiierten Abonnement Modell alle Ereignis Quellen im Ereignis Abonnement definieren muss.

Beachten Sie beim Einrichten eines von der Quelle initiierten Abonnements, ob sich die Ereignis Quellcomputer in derselben Domäne wie der Ereignis Sammler Computer befinden. In den folgenden Abschnitten werden die Schritte beschrieben, die befolgt werden müssen, wenn sich die Ereignis Quellen in derselben Domäne oder nicht in derselben Domäne wie der Ereignis Sammler Computer befinden.

> [!Note]  
> Jeder Computer in einer Domäne, lokal oder Remote, kann ein Ereignis Sammler sein. Bei der Auswahl eines Ereignis Sammlers ist es jedoch wichtig, einen Computer auszuwählen, der in der Nähe der Mehrzahl der Ereignisse liegt. Das Senden von Ereignissen an einen Computer an einem entfernten Netzwerk Speicherort in einem WAN kann die Gesamtleistung und Effizienz bei der Ereignis Erfassung verringern.

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-in-the-same-domain-as-the-event-collector-computer"></a>Einrichten eines von der Quelle initiierten Abonnements, in dem sich die Ereignis Quellen in derselben Domäne wie der Ereignis Sammler Computer befinden

Die Ereignis Quellcomputer und der Ereignis Sammler Computer müssen so konfiguriert werden, dass ein von der Quelle initiiertes Abonnement eingerichtet wird.

> [!Note]  
> Bei diesen Anweisungen wird vorausgesetzt, dass Sie über Administrator Zugriff auf den Windows Server-Domänen Controller verfügen, der für die Domäne zuständig ist, in der der Remote Computer für die Erfassung von Ereignissen konfiguriert wird

### <a name="configuring-the-event-source-computer"></a>Konfigurieren des Ereignis Quell Computers

1. Führen Sie den folgenden Befehl an einer Eingabeaufforderung mit erhöhten Rechten auf dem Windows Server-Domänen Controller aus, um Windows-Remoteverwaltung zu konfigurieren:

    **WinRM-QC-q**

2. Starten Sie die Gruppenrichtlinie, indem Sie den folgenden Befehl ausführen:

    **% Systemroot% \\ system32 \\ gpeer dit. msc**

3. Erweitern Sie unter dem Knoten **Computer Konfiguration** den Knoten **Administrative Vorlagen** , erweitern Sie dann den Knoten **Windows-Komponenten** , und wählen Sie dann den Knoten **Ereignis Weiterleitung** aus.

4. Klicken Sie mit der rechten Maustaste auf die Einstellung **Abonnement-Manager** , und wählen Sie **Eigenschaften** aus. Aktivieren Sie die Einstellung " **Abonnement-Manager** ", und klicken Sie auf die Schaltfläche **anzeigen** , um der Einstellung eine Server Adresse hinzuzufügen. Fügen Sie mindestens eine Einstellung hinzu, die den Ereignis Sammler Computer angibt. Das **Eigenschaften** Fenster für den Abonnement-Manager enthält eine Registerkarte " **Erklärung** ", die die Syntax der Einstellung beschreibt.

5. Nachdem die Einstellung für den **Abonnement-Manager** hinzugefügt wurde, führen Sie den folgenden Befehl aus, um sicherzustellen, dass die Richtlinie angewendet wird:

    **gpupdate /force**

### <a name="configuring-the-event-collector-computer"></a>Konfigurieren des Ereignis Sammler Computers

1. Führen Sie den folgenden Befehl an einer Eingabeaufforderung mit erhöhten Rechten auf dem Windows Server-Domänen Controller aus, um Windows-Remoteverwaltung zu konfigurieren:

    **WinRM-QC-q**

2. Führen Sie den folgenden Befehl aus, um den Event Collector-Dienst zu konfigurieren:

    **wecutil QC/q**

3. Erstellen eines von der Quelle initiierten Abonnements Dies kann entweder Programm gesteuert, mithilfe des Ereignisanzeige oder mithilfe [**Wecutil.exe**](wecutil.md)erfolgen. Weitere Informationen zum programmgesteuerten Erstellen des Abonnements finden Sie im Codebeispiel unter [Erstellen eines von der Quelle initiierten Abonnements](creating-a-source-initiated-subscription.md). Wenn Sie Wecutil.exe verwenden, müssen Sie eine XML-Datei mit Ereignis Abonnements erstellen und den folgenden Befehl verwenden:

    **wecutil** - *configurationFile.xml*

    Der folgende XML-Code ist ein Beispiel für den Inhalt einer Abonnement Konfigurationsdatei, die ein von der Quelle initiiertes Abonnement erstellt, um Ereignisse aus dem Anwendungs Ereignisprotokoll eines Remote Computers an das ForwardedEvents-Protokoll auf dem Ereignis Sammler Computer weiterzuleiten.

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
    > Beim Erstellen eines von der Quelle initiierten Abonnements, wenn "zugswedsourcedomaincomputers", "zugswedsourcenondomaincomputers/issuercalist", "zugswedsubjetlist" und "deniedsubjetlist" leer sind, dann "o:NSG: nsd: (a;; GA;;;D C) (A;; GA;;; NS) "wird als Standard Sicherheits Beschreibung für" zustellwedsourcedomaincomputers "verwendet. Der Standard Deskriptor gewährt Mitgliedern der Domänen Gruppe Domänen Computer sowie der Gruppe lokaler Netzwerkdienst (für die lokale Weiterleitung) die Möglichkeit, Ereignisse für dieses Abonnement zu erhöhen.

### <a name="to-validate-that-the-subscription-works-correctly"></a>So überprüfen Sie, ob das Abonnement ordnungsgemäß funktioniert

1. Führen Sie auf dem Computer mit dem Ereignis Sammler die folgenden Schritte aus:

    1. Führen Sie den folgenden Befehl an einer Eingabeaufforderung mit erhöhten Rechten auf dem Windows Server-Domänen Controller aus, um den Lauf Zeit Status des Abonnements zu erhalten:

        *&lt; Abonnement-ID &gt;* für **wecutil GR**

    2. Überprüfen Sie, ob die Ereignis Quelle verbunden ist. Möglicherweise müssen Sie warten, bis das Aktualisierungs Intervall, das in der Richtlinie angegeben ist, übersteigt, nachdem Sie das Abonnement erstellt haben, damit die Ereignis Quelle verbunden werden kann.
    3. Führen Sie den folgenden Befehl aus, um die Abonnement Informationen zu erhalten:

        *&lt; Abonnement-ID &gt;* für **wecutil GS**

    4. Den Wert deliverymaxitems aus den Abonnement Informationen erhalten.

2. Stellen Sie auf dem Ereignis Quellcomputer die Ereignisse aus dem Ereignis Abonnement aus, die der Abfrage entsprechen. Die Anzahl der deliverymaxitems-Ereignisse muss ausgelöst werden, damit die Ereignisse weitergeleitet werden.
3. Überprüfen Sie auf dem Ereignis Sammler Computer, ob die Ereignisse an das Protokoll ForwardedEvents oder an das im Abonnement angegebene Protokoll weitergeleitet wurden.

## <a name="forwarding-the-security-log"></a>Weiterleiten des Sicherheitsprotokolls

Um das Sicherheitsprotokoll weiterleiten zu können, müssen Sie das Netzwerkdienst Konto der Gruppe "EventLog Readers" hinzufügen.

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-not-in-the-same-domain-as-the-event-collector-computer"></a>Einrichten eines von der Quelle initiierten Abonnements, in dem sich die Ereignis Quellen nicht in derselben Domäne wie der Ereignis Sammler Computer befinden

> [!Note]  
> Bei diesen Anweisungen wird davon ausgegangen, dass Sie über Administrator Zugriff auf einen Windows Server-Domänen Controller verfügen. Da sich die Computer oder Computer der Remote-Ereignis Sammlung nicht in der vom Domänen Controller bereitgestellten Domäne befinden, müssen Sie in diesem Fall einen einzelnen Client starten, indem Sie Windows-Remoteverwaltung mithilfe der Dienste (Services. msc) auf "automatisch" festlegen. Alternativ können Sie "WinRM quickconfig" auf jedem Remote Client ausführen.

Die folgenden Voraussetzungen müssen erfüllt sein, bevor das Abonnement erstellt wird.

1. Führen Sie auf dem Ereignis Sammler Computer die folgenden Befehle an einer Eingabeaufforderung mit erhöhten Rechten aus, um Windows-Remoteverwaltung und den Ereignis Sammlungs Dienst zu konfigurieren:

    **WinRM-QC-q**

    **wecutil QC/q**

2. Der Collector-Computer muss über ein Server Authentifizierungszertifikat (Zertifikat mit einem Server Authentifizierungs Zweck) in einem Zertifikat Speicher des lokalen Computers verfügen.
3. Führen Sie auf dem Ereignis Quellcomputer den folgenden Befehl aus, um Windows-Remoteverwaltung zu konfigurieren:

    **WinRM-QC-q**

4. Der Quellcomputer muss ein Client Authentifizierungszertifikat (Zertifikat mit einem Client Authentifizierungs Zweck) in einem Zertifikat Speicher des lokalen Computers haben.
5. Port 5986 wird auf dem Ereignis Sammler Computer geöffnet. Um diesen Port zu öffnen, führen Sie den folgenden Befehl aus:

    **netsh Firewall Add portopening TCP 5986 "WinRM HTTPS Remote Management"**

### <a name="certificates-requirements"></a>Zertifikat Anforderungen

- Auf dem Ereignis Sammler Computer muss ein Server Authentifizierungszertifikat im persönlichen Speicher des lokalen Computers installiert sein. Der Betreff dieses Zertifikats muss dem FQDN des Sammlers entsprechen.
- Ein Client Authentifizierungszertifikat muss auf den Ereignis Quell Computern im persönlichen Speicher des lokalen Computers installiert werden. Der Betreff dieses Zertifikats muss dem FQDN des Computers entsprechen.
- Wenn das Client Zertifikat von einer anderen Zertifizierungsstelle als der Ereignis Sammlung ausgestellt wurde, müssen die Stamm-und zwischen Zertifikate ebenfalls auf dem Ereignis Sammler installiert werden.
- Wenn das Client Zertifikat von einer zwischen Zertifizierungsstelle ausgestellt wurde und auf dem Collector Windows 2012 oder höher ausgeführt wird, müssen Sie den folgenden Registrierungsschlüssel konfigurieren:

    **HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**
 
- Vergewissern Sie sich, dass sowohl der Server als auch der Client den Sperr Status für alle Zertifikate erfolgreich überprüfen können. Die Verwendung des **certutil** -Befehls kann bei der Problembehandlung hilfreich sein.

Weitere Informationen finden Sie in diesem Artikel: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx

### <a name="setup-the-listener-on-the-event-collector"></a>Einrichten des Listener auf dem Ereignis Sammler

1. Legen Sie die Zertifikat Authentifizierung mit dem folgenden Befehl fest:

    **WinRM Set WinRM/config/Service/auth @ {Certificate = "true"}**

2. Ein WinRM-HTTPS-Listener mit dem Fingerabdruck des Zertifikats für die Server Authentifizierung sollte auf dem Ereignis Sammler Computer vorhanden sein. Dies kann mit dem folgenden Befehl überprüft werden:

    **WinRM e WinRM/config/Listener**

3. Wenn der HTTPS-Listener nicht angezeigt wird, oder wenn der Thumb-Fingerabdruck des HTTPS-Listener nicht mit dem Fingerabdruck des Server Authentifizierungs Zertifikats auf dem Collector-Computer identisch ist, können Sie diesen Listener löschen und einen neuen mit dem richtigen Thumb-Druck erstellen. Um den HTTPS-Listener zu löschen, verwenden Sie den folgenden Befehl:

    **WinRM-DELETE WinRM/config/Listener? Address = * + Transport = HTTPS**

    Verwenden Sie den folgenden Befehl, um einen neuen Listener zu erstellen:

    **WinRM erstellt WinRM/config/Listener? Address =&#42;+ Transport = HTTPS @ {Hostname = "** voll &lt; _qualifizierter Name des Sammlers_ &gt; **"; Certificatethbibprint = "** &lt; _Thumb Print des Server Authentifizierungs Zertifikats_ &gt; **"}**

### <a name="configure-certificate-mapping-on-the-event-collector"></a>Konfigurieren der Zertifikat Zuordnung für den Ereignis Sammler

1. Erstellen Sie einen neuen lokalen Benutzer, und fügen Sie ihn der lokalen Administrator Gruppe hinzu.
2. Erstellen Sie die Zertifikat Zuordnung mithilfe eines Zertifikats, das auf dem Computer "Vertrauenswürdige Stamm Zertifizierungsstellen" oder "zwischen Zertifizierungsstellen" vorhanden ist.

    Dabei handelt es sich um das Zertifikat der Stamm-oder zwischen Zertifizierungsstelle, die die auf den Ereignis Quell Computern installierten Zertifikate ausgestellt *hat (um Verwirrung zu vermeiden, ist dies die Zertifizierungsstelle, die sich direkt oberhalb des Zertifikats in der Zertifikat Kette befindet)*:

    **WinRM erstellt WinRM/config/Service/certmapping? Aussteller** = &lt; _Fingerabdruck des ausstellenden Zertifizierungsstellen Zertifikats_ &gt; **+ Betreff =&#42;+ URI =&#42; @ {username = "** &lt; _username_ &gt; **"; Password = "** &lt; _Password_ &gt; **"}-Remote: localhost**

3. Testen Sie den Listener und die Zertifikat Zuordnung von einem Client mit dem folgenden Befehl:

    **WinRM g WinRM/config-r:https://** &lt; _Ereignis Sammler_ &gt; -voll qualifizierten Namen **: 5986-a:Certificate-Certificate: "** &lt; Finger _Abdruck des Client Authentifizierungs Zertifikats_ &gt; **"**

    Dadurch sollte die WinRM-Konfiguration des Ereignis Sammlers zurückgegeben werden. Verschieben Sie diesen Schritt **nicht** , wenn die Konfiguration nicht angezeigt wird.

    **Was geschieht in diesem Schritt?**
    - Der Client stellt eine Verbindung mit dem Ereignis Sammler her und sendet das angegebene Zertifikat.
    - Die Ereignis Sammlung sucht nach der ausstellenden Zertifizierungsstelle und überprüft, ob eine übereinstimmende Zertifikat Zuordnung ist.
    - Der Ereignis Sammler überprüft die Client Zertifikatskette und den Status der Widerruf enden Daten.
    - Wenn die oben genannten Schritte erfolgreich sind, ist die Authentifizierung abgeschlossen.

> [!NOTE]
> Möglicherweise erhalten Sie den Fehler "Zugriff verweigert", der sich über die Authentifizierungsmethode beschwert, was irreführend sein könnte. Um Probleme zu beheben, überprüfen Sie das CAPI-Protokoll auf dem Ereignis Sammler.

4. Listet die konfigurierten certmapping-Einträge mit dem folgenden Befehl auf: **WinRM Enumeration WinRM/config/Service/certmapping**

### <a name="event-source-computer-configuration"></a>Konfiguration der Ereignis Quellcomputer

1. Melden Sie sich mit einem Administrator Konto an, und öffnen Sie die Editor für lokale Gruppenrichtlinien (gpeer dit. msc).
2. Navigieren Sie zum lokalen Computer policy\computerkonfiguration\administrative Vorlagen\Windows-komponents\ereignisweiterleitung.
3. Öffnen Sie die Richtlinie zum Konfigurieren der Server Adresse, des Aktualisierungs Intervalls und der Aussteller Zertifizierungsstelle einer Ziel Abonnement-Manager-Richtlinie.
4. Aktivieren Sie die Richtlinie, und klicken Sie auf Abonnement-Manager "anzeigen...". gedrückt.
5. Geben Sie im Fenster "Abonnement-Manager" die folgende Zeichenfolge ein:

    **Server = https://** &lt; Voll _qualifizierter Name des Ereignis Sammler Servers_ &gt; **: 5986/WSMAN/Abonnement-Manager/WEC, Refresh =** &lt; _Aktualisierungs Intervall in Sekunden_ &gt; **, Issuerca =** &lt; Finger _Abdruck des ausstellenden Zertifizierungsstellen Zertifikats_&gt;

6. Führen Sie die folgende Befehlszeile aus, um die lokalen Gruppenrichtlinie Einstellungen zu aktualisieren: gpupdate/force
7. Diese Schritte sollten das Ereignis 104 auf dem Quellcomputer Ereignisanzeige Anwendungs-und dienstprotokolle\microsoft\windows\eventlog-forwardingplugin\operational Log mit folgender Meldung erstellen:

    "Die Weiterleitung hat erfolgreich eine Verbindung mit dem Abonnement-Manager am Adress- &lt; FQDN &gt; gefolgt von Ereignis 100 mit der folgenden Meldung hergestellt:" das Abonnement &lt; sub_name &gt; erfolgreich erstellt. "

8. Auf dem Ereignis Sammler wird der Abonnement Lauf Zeit Status jetzt 1 aktiver Computer angezeigt.
9. Öffnen Sie das Protokoll ForwardedEvents auf dem Ereignis Sammler, und überprüfen Sie, ob die Ereignisse von den Quell Computern weitergeleitet wurden.

### <a name="grant-permission-on-the-private-key-of-the-client-certificate-on-the-event-source"></a>Erteilen Sie die Berechtigung für den privaten Schlüssel des Client Zertifikats für die Ereignis Quelle.

1. Öffnen Sie die Zertifikat Verwaltungskonsole für den lokalen Computer auf dem Ereignis Quellcomputer.
2. Klicken Sie mit der rechten Maustaste auf das Client Zertifikat, und verwalten Sie private Schlüssel
3. Erteilen Sie dem Netzwerkdienst Benutzer Leseberechtigungen.

### <a name="event-subscription-configuration"></a>Konfiguration des Ereignis Abonnements

1. Öffnen Sie Ereignisanzeige in der Ereignis Sammlung, und navigieren Sie zum Knoten "Abonnements".
2. Klicken Sie mit der rechten Maustaste auf Abonnements, und wählen Sie Abonnement erstellen... aus.
3. Benennen Sie einen Namen und eine optionale Beschreibung für das neue Abonnement.
4. Wählen Sie die Option "Quellcomputer initiiert" aus, und klicken Sie auf "Computer Gruppen auswählen...".
5. Klicken Sie in Computer Gruppen auf "nicht-Domänen Computer hinzufügen...". und geben den Ereignis Quell Hostnamen ein.
6. Klicken Sie auf "Zertifikate hinzufügen". Fügen Sie das Zertifikat der Zertifizierungsstelle hinzu, von der die Client Zertifikate ausgestellt werden. Sie können in Zertifikat anzeigen klicken, um das Zertifikat zu überprüfen.
7. Klicken Sie in den Zertifizierungsstellen auf OK, um das Zertifikat hinzuzufügen.
8. Klicken Sie nach dem Hinzufügen von Computern auf OK.
9. Klicken Sie zurück zu den Abonnement Eigenschaften, und klicken Sie auf Ereignisse auswählen...
10. Konfigurieren Sie den Abfrage Filter Ereignisse, indem Sie die Ereignis Ebene (n), das Ereignisprotokoll (n) oder die Ereignis Quelle (en), die Ereignis-ID (en) und andere Filteroptionen angeben.
11. Klicken Sie zurück zu den Abonnement Eigenschaften, und klicken Sie auf erweitert...
12. Wählen Sie eine der Optimierungs Optionen für die Ereignis Übermittlung vom Quell Ereignis an den Ereignis Sammler aus, oder überlassen Sie die Standardeinstellung: 
    1. **Bandbreite minimieren**: die übermittelten Ereignisse werden weniger häufig verwendet, um Bandbreite zu sparen.
    2. **Minimieren der Latenz**: Ereignisse werden bereitgestellt, sobald sie auftreten, um die Latenz von Ereignissen zu verringern.
13. Ändern Sie das Protokoll in HTTPS, und klicken Sie auf OK.
14. Klicken Sie auf OK, um das neue Abonnement zu erstellen.
15. Überprüfen Sie den Lauf Zeit Status des Abonnements, indem Sie mit der rechten Maustaste klicken und "Lauf Zeit Status" auswählen
