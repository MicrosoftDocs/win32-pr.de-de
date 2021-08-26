---
title: 'Installation und Konfiguration für Windows-Remoteverwaltung '
description: Damit Windows-Skripts für die Remoteverwaltung (WinRM)  und das Winrm-Befehlszeilentool Datenvorgänge ausführen können, muss Windows-Remoteverwaltung (WinRM) sowohl installiert als auch konfiguriert sein.
ms.date: 08/31/2020
ms.assetid: 81c40456-0003-46d0-8695-83bf77432056
ms.topic: article
ms.custom: contperf-fy21q1
ms.openlocfilehash: c031ad9b9d9c888385527c227b102c64bb4dfb65eaea340e52eac3fb9595e591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997620"
---
# <a name="installation-and-configuration-for-windows-remote-management"></a>Installation und Konfiguration für Windows Remoteverwaltung

Damit Windows-Skripts für die Remoteverwaltung (WinRM)  und das Winrm-Befehlszeilentool Datenvorgänge ausführen können, muss Windows-Remoteverwaltung (WinRM) sowohl installiert als auch konfiguriert sein.

Diese Elemente hängen auch von der WinRM-Konfiguration ab.

- Das Windows Remote Shell-Befehlszeilentool (**Winrs**). [](./windows-remote-management-glossary.md#w)
- [Ereignisweiterleitung.](./windows-remote-management-glossary.md#e)
- Windows PowerShell 2.0-Remoting.

## <a name="where-winrm-is-installed"></a>Wo WinRM installiert ist

WinRM wird automatisch mit allen derzeit unterstützten Versionen des betriebssystembasierten Windows installiert.

## <a name="configuration-of-winrm-and-ipmi"></a>Konfiguration von WinRM und IPMI

Diese [WMI-Anbieterkomponenten](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) [(WinRM und Intelligent Platform Management Interface, IPMI)](./windows-remote-management-glossary.md#i) werden mit dem Betriebssystem installiert.

- Der WinRM-Dienst wird automatisch auf Windows Server 2008 und auf Wards gestartet (unter Windows Vista müssen Sie den Dienst manuell starten).
- Standardmäßig ist kein [WinRM-Listener](./windows-remote-management-glossary.md#l) konfiguriert. Selbst wenn der WinRM-Dienst ausgeführt wird, WS-Management Protokollmeldungen, die Daten anfordern, weder empfangen noch gesendet werden. [](./windows-remote-management-glossary.md#m)
- Internet Connection Firewall (ICF) blockiert den Zugriff auf Ports.

Verwenden Sie **den Winrm-Befehl,** um listeners und die Adressen zu suchen, indem Sie den folgenden Befehl an einer Eingabeaufforderung eingeben.

```console
winrm e winrm/config/listener
```

Geben Sie den folgenden Befehl ein, um den Status der Konfigurationseinstellungen zu überprüfen.

```console
winrm get winrm/config
```

## <a name="quick-default-configuration"></a>Schnelle Standardkonfiguration

Sie können das WS-Management auf dem lokalen Computer aktivieren und die Standardkonfiguration für die Remoteverwaltung mit dem Befehl `winrm quickconfig` einrichten.

Der `winrm quickconfig` Befehl (oder die abgekürzte Version `winrm qc` ) führt diese Vorgänge aus.

- Startet den WinRM-Dienst und legt den Starttyp des Diensts auf automatischen Start fest.
- Konfiguriert einen Listener für die Ports, die Protokollnachrichten WS-Management http oder HTTPS für eine beliebige IP-Adresse senden und empfangen. [](./windows-remote-management-glossary.md#m)
- Definiert ICF-Ausnahmen für den WinRM-Dienst und öffnet die Ports für HTTP und HTTPS.

> [!NOTE]
> Der `winrm quickconfig` Befehl erstellt eine Firewallausnahme nur für das aktuelle Benutzerprofil. Wenn das Firewallprofil aus irgendeinem Grund geändert wird, sollten Sie ausführen, um die Firewallausnahme für das neue Profil zu aktivieren. Andernfalls ist die Ausnahme `winrm quickconfig` möglicherweise nicht aktiviert.

Um Informationen zum Anpassen einer Konfiguration abzurufen, geben Sie `winrm help config` an einer Eingabeaufforderung ein.

### <a name="to-configure-winrm-with-default-settings"></a>So konfigurieren Sie WinRM mit Standardeinstellungen

1. Geben Sie `winrm quickconfig` an einer Eingabeaufforderung ein.

   Wenn Sie nicht unter dem Administratorkonto des lokalen Computers ausführen, müssen Sie entweder als **Administrator** ausführen im **Startmenü** auswählen oder den **Befehl Runas** an einer Eingabeaufforderung verwenden.

2. Wenn das Tool **Diese Änderungen vornehmen \[ y/n \] ?** anzeigt, geben Sie **y ein.**

   Wenn die Konfiguration erfolgreich ist, wird die folgende Ausgabe angezeigt.

   ``` syntax
   WinRM has been updated for remote management.

   WinRM service type changed to delayed auto start.
   WinRM service started.
   Created a WinRM listener on https://* to accept WS-Man requests to any IP on this machine.
   ```

3. Behalten Sie die Standardeinstellungen für Client- und Serverkomponenten von WinRM bei, oder passen Sie sie an. Beispielsweise müssen Sie der Liste trustedHosts der Clientkonfiguration möglicherweise bestimmte Remotecomputer hinzufügen.

   Sie sollten eine Liste vertrauenswürdiger Hosts einrichten, wenn keine gegenseitige Authentifizierung eingerichtet werden kann. Kerberos ermöglicht die gegenseitige Authentifizierung, kann aber nicht nur in Arbeitsgruppendomänen &mdash; verwendet werden. Eine bewährte Methode beim Einrichten vertrauenswürdiger Hosts für eine Arbeitsgruppe besteht in der möglichst eingeschränkten Liste.

4. Erstellen Sie einen HTTPS-Listener, indem Sie den Befehl `winrm quickconfig -transport:https` eingeben. Beachten Sie, dass Sie Port 5986 öffnen müssen, damit der HTTPS-Transport funktioniert.

## <a name="listener-and-ws-management-protocol-default-settings"></a>Standardeinstellungen WS-Management Listener- und Protokollprotokolls

Geben Sie an einer Eingabeaufforderung ein, um `winrm enumerate winrm/config/listener` die Listenerkonfiguration zu erhalten. Listener werden durch einen Transport (HTTP oder HTTPS) und eine IPv4- oder IPv6-Adresse definiert.

`winrm quickconfig` erstellt die folgenden Standardeinstellungen für einen Listener. Sie können mehrere Listener erstellen. Geben Sie an einer `winrm help config` Eingabeaufforderung ein, um weitere Informationen zu erhalten.

### <a name="address"></a>Adresse

Gibt die Adresse an, für die der Listener erstellt wurde.

### <a name="transport"></a>Transport

Legt den Transport zum Senden und Empfangen von WS-Management-Protokollanforderungen und -antworten fest. Der Wert muss entweder *HTTP oder* *HTTPS sein.* Der Standardwert ist *HTTP.*

### <a name="port"></a>Port

Gibt den TCP-Port an, für den der Listener erstellt wird.

**WinRM 2.0:** Der HTTP-Standardport ist 5985.

### <a name="hostname"></a>Hostname

Gibt den Hostnamen des Computers an, auf dem der WinRM-Dienst ausgeführt wird. Der Wert muss ein vollqualifizierter Domänenname, eine IPv4- oder IPv6-Literalzeichenfolge oder ein Platzhalterzeichen sein.

### <a name="enabled"></a>Aktiviert

Gibt an, ob der Listener aktiviert oder deaktiviert ist. Der Standardwert ist *True*.

### <a name="urlprefix"></a>URLPrefix

Gibt ein URL-Präfix an, für das HTTP- oder HTTPS-Anforderungen akzeptiert werden. Dies ist eine Zeichenfolge, die nur die Zeichen a-z, A-Z, 9-0, Unterstrich ( \_ ) und Schrägstrich (/) enthält. Die Zeichenfolge darf nicht mit einem Schrägstrich (/) beginnen oder mit diesem enden. Wenn der Computername beispielsweise SampleMachine ist, gibt der WinRM-Client https://SampleMachine/< *URLPrefix*> zieladresse an. Das Standard-URL-Präfix ist "wsman".

### <a name="certificatethumbprint"></a>CertificateThumbprint

Gibt den Fingerabdruck des Dienstzertifikats an. Dieser Wert stellt eine Zeichenfolge mit zweistelligen Hexadezimalwerten dar, die im Feld Fingerabdruck des Zertifikats gefunden werden. Diese Zeichenfolge enthält den SHA-1-Hash des Zertifikats. Zertifikate werden bei der clientzertifikatbasierten Authentifizierung verwendet. Zertifikate können nur lokalen Benutzerkonten zugeordnet werden und funktionieren nicht mit Domänenkonten.

### <a name="listeningon"></a>ListeningOn

Gibt die IPv4- und IPv6-Adressen an, die der Listener verwendet. Beispiel: "111.0.0.1, 111.222.333.444, ::1, 1000:2000:2c:3:c19:9ec8:a715:5e24, 3ffe:8311:ffff:f70f:0:5efe:111.222.333.444, fe80::5efe:111.222.333.444%8, fe80::c19:9ec8:a715:5e24%6".

## <a name="protocol-default-settings"></a>Standardeinstellungen des Protokolls

Viele der Konfigurationseinstellungen, z. B. MaxEnveizeSizekb oder SoapTraceEnabled, bestimmen, wie die WinRM-Client- und -Serverkomponenten mit dem WS-Management interagieren. In der folgenden Liste werden die verfügbaren Konfigurationseinstellungen beschrieben.

### <a name="maxenvelopesizekb"></a>MaxEnvelopeSizekb

Gibt die maximalen SOAP-Daten (Simple Object Access Protocol) in Kilobytes an. Der Standardwert ist 150 KB.

> [!NOTE]  
> Das Verhalten wird nicht unterstützt, wenn MaxEnveizeSizekb auf einen Wert festgelegt ist, der größer als 1039440.

### <a name="maxtimeoutms"></a>MaxTimeoutms

Gibt das maximale Time out in Millisekunden an, das für alle Anforderungen außer Pull Requests verwendet werden kann. Der Standardwert ist 60000.

### <a name="maxbatchitems"></a>MaxBatchItems

Gibt die maximale Anzahl von Elementen an, die als Pull-Antwort verwendet werden können. Der Standardwert ist 32000.

### <a name="maxproviderrequests"></a>MaxProviderRequests

Gibt die maximale Anzahl gleichzeitiger Anforderungen vom Dienst an, die zulässig sind. Der Standard ist 25.

**WinRM 2.0:** Diese Einstellung ist veraltet und auf schreibgeschützt festgelegt.

## <a name="winrm-client-default-configuration-settings"></a>Standardkonfigurationseinstellungen für den WinRM-Client

Die Clientversion von WinRM verfügt über die folgenden Standardkonfigurationseinstellungen.

### <a name="networkdelayms"></a>NetworkDelayms

Gibt die Zeit in Millisekunden an, die der Clientcomputer wartet, um der Netzwerk-Verzögerungszeit gerecht zu werden. Der Standardwert ist 5.000 Millisekunden.

### <a name="urlprefix"></a>URLPrefix

Gibt ein URL-Präfix an, für das HTTP- oder HTTPS-Anforderungen akzeptiert werden. Das Standard-URL-Präfix ist "wsman".

### <a name="allowunencrypted"></a>AllowUnencrypted

Ermöglicht es dem Clientcomputer, unverschlüsselten Verkehr anzufordern. Standardmäßig erfordert der Clientcomputer verschlüsselten Netzwerkdatenverkehr, und diese Einstellung ist *False.*

### <a name="basic"></a>Basic

Ermöglicht es dem Clientcomputer, die Standardauthentifizierung zu verwenden. Standardauthentifizierung ist ein Schema, in dem der Benutzername und das Kennwort in Klartext an den Server oder Proxy gesendet werden. Diese Methode ist die am wenigsten sichere Authentifizierungsmethode. Der Standardwert ist *True*.

### <a name="digest"></a>Digest

Ermöglicht dem Client, Digestauthentifizierung zu verwenden. Die Digestauthentifizierung ist ein Abfrage/Antwort-Schema, das eine serverspezifische Zeichenfolge für die Abfrage verwendet. Nur der Clientcomputer kann eine Anforderung der Digestauthentifizierung initiieren. Der Clientcomputer sendet eine Authentifizierungsanforderung an den Server und empfängt eine Tokenzeichenfolge vom Server. Anschließend sendet der Clientcomputer die Ressourcenanforderung, einschließlich des Benutzernamens und eines kryptografischen Hashs des Kennworts in Kombination mit der Tokenzeichenfolge. Digestauthentifizierung wird für HTTP und HTTPS unterstützt. WinRM Shell-Clientskripts und -Anwendungen können die Digestauthentifizierung angeben, aber der WinRM-Dienst akzeptiert keine Digestauthentifizierung. Der Standardwert ist *True*.

> [!NOTE]
> Digestauthentifizierung über HTTP wird nicht als sicher betrachtet.

### <a name="certificate"></a>Zertifikat

Ermöglicht dem Client die Verwendung der zertifikatbasierten Clientauthentifizierung. Die zertifikatbasierte Authentifizierung ist ein Schema, in dem der Server einen Client authentifiziert, der durch ein X509-Zertifikat identifiziert wird. Der Standardwert ist *True*.

### <a name="kerberos"></a>Kerberos

Ermöglicht dem Client, Kerberos-Authentifizierung zu verwenden. Kerberos-Authentifizierung ist ein Schema, in dem sich der Client und Server gegenseitig mit Kerberos-Zertifikaten authentifizieren. Der Standardwert ist *True*.

### <a name="negotiate"></a>Aushandeln

Ermöglicht dem Client, Negotiate-Authentifizierung zu verwenden. Negotiate-Authentifizierung ist ein Schema, in dem der Client eine Anforderung an den zu authentifizierenden Server sendet. Der Server bestimmt, ob Kerberos oder NTLM verwendet wird. Das Kerberos-Protokoll wird zur Authentifizierung eines Domänenkontos ausgewählt und NTLM für lokale Computerkonten. Der Benutzername muss für \\ einen Domänenbenutzer im Domänenbenutzernamenformat angegeben \_ werden. Der Benutzername muss für einen lokalen Benutzer auf einem Servercomputer im Format "Servername Benutzername" angegeben \_ \\ \_ werden. Der Standardwert ist *True*.

### <a name="credssp"></a>CredSSP

Ermöglicht dem Client die Verwendung der CredSSP-Authentifizierung (Credential Security Support Provider). CredSSP ermöglicht einer Anwendung, die Anmeldeinformationen des Benutzers vom Clientcomputer an den Zielserver zu delegieren. Der Standardwert ist *False*.

### <a name="defaultports"></a>DefaultPorts

Gibt die Ports an, die der Client für HTTP oder HTTPS verwendet.

**WinRM 2.0:** Der HTTP-Standardport ist 5985 und der HTTPS-Standardport 5986.

### <a name="trustedhosts"></a>TrustedHosts

Gibt die Liste der vertrauenswürdigen Remotecomputer an. Andere Computer in einer Arbeitsgruppe oder Computer in einer anderen Domäne sollten dieser Liste hinzugefügt werden.

> [!Note]
> Die Computer in der Liste TrustedHosts sind nicht authentifiziert. Der Client kann Anmeldeinformationen an diese Computer senden.

Wenn eine IPv6-Adresse für einen TrustedHost angegeben wird, muss die Adresse in eckige Klammern eingeschlossen werden, wie der folgende WinRM-Hilfsprogrammbefehl zeigt: `winrm set winrm/config/client '@{TrustedHosts ="[0:0:0:0:0:0:0:0]"}'` .

Geben Sie ein, um weitere Informationen zum Hinzufügen von Computern zur TrustedHosts-Liste zu `winrm help config` erhalten.

## <a name="winrm-service-default-configuration-settings"></a>Standardkonfigurationseinstellungen für den WinRM-Dienst

Die Dienstversion von WinRM verfügt über die folgenden Standardkonfigurationseinstellungen.

### <a name="rootsddl"></a>RootSDDL

Gibt die Sicherheitsbeschreibung an, die den Remotezugriff auf den Listener steuert. Der Standardwert ist "O:NSG:BAD:P(A;; GA;;; BA)(A;; GR;;; ER)S:P(AU;FA; GA;;; WD)(AU;SA; GWGX;;; WD)".

### <a name="maxconcurrentoperations"></a>MaxConcurrentOperations

Die maximale Anzahl gleichzeitiger Vorgänge. Der Standardwert ist 100.

**WinRM 2.0:** Die Einstellung MaxConcurrentOperations ist veraltet und auf schreibgeschützt festgelegt. Diese Einstellung wurde durch MaxConcurrentOperationsPerUser ersetzt.

### <a name="maxconcurrentoperationsperuser"></a>MaxConcurrentOperationsPerUser

Gibt die maximale Anzahl gleichzeitiger Vorgänge an, die jeder Benutzer remote auf demselben System öffnen kann. Standardmäßig sind 1500 eingestellt.

### <a name="enumerationtimeoutms"></a>EnumerationTimeoutms

Gibt das Leerlauftime out in Millisekunden zwischen Pullnachrichten an. Der Standardwert ist 60000.

### <a name="maxconnections"></a>MaxConnections

Gibt die maximale Anzahl aktiver Anforderungen an, die der Dienst gleichzeitig verarbeiten kann. Der Standardwert ist 300.

**WinRM 2.0:** Der Standardwert ist 25.

### <a name="maxpacketretrievaltimeseconds"></a>MaxPacketRetrievalTimeSeconds

Gibt die maximale Zeitdauer in Sekunden an, die der WinRM-Dienst zum Abrufen eines Pakets benötigt. Der Standardwert ist 120 Sekunden.

### <a name="allowunencrypted"></a>AllowUnencrypted

Ermöglicht es dem Clientcomputer, unverschlüsselten Verkehr anzufordern. Der Standardwert ist *False*.

### <a name="basic"></a>Basic

Ermöglicht dem WinRM-Dienst die Verwendung der Standardauthentifizierung. Der Standardwert ist *False*.

### <a name="certificate"></a>Zertifikat

Ermöglicht dem WinRM-Dienst die Verwendung der clientzertifikatbasierten Authentifizierung. Der Standardwert ist *False*.

### <a name="kerberos"></a>Kerberos

Ermöglicht dem WinRM-Dienst die Verwendung der Kerberos-Authentifizierung. Der Standardwert ist *True*.

### <a name="negotiate"></a>Aushandeln

Ermöglicht dem WinRM-Dienst die Verwendung der Negotiate-Authentifizierung. Der Standardwert ist *True*.

### <a name="credssp"></a>CredSSP

Ermöglicht dem WinRM-Dienst die Verwendung der CredSSP-Authentifizierung (Credential Security Support Provider). Der Standardwert ist *False*.

### <a name="cbthardeninglevel"></a>CbtHardeningLevel

Legt die Richtlinie für Kanalbindungstoken-Anforderungen in Authentifizierungsanforderungen fest. Der Standardwert ist *Gelockert.*

### <a name="defaultports"></a>DefaultPorts

Gibt die Ports an, die der WinRM-Dienst für HTTP oder HTTPS verwendet.

**WinRM 2.0:** Der HTTP-Standardport ist 5985 und der HTTPS-Standardport 5986.

### <a name="ipv4filter-and-ipv6filter"></a>IPv4Filter und IPv6Filter

Gibt die IPv4- oder IPv6-Adressen an, die Listener verwenden können. Die Standardwerte sind IPv4Filter = \* und IPv6Filter = \* .

**IPv4:** Eine IPv4-Literalzeichenfolge besteht aus vier gepunkteten Dezimalzahlen, die jeweils im Bereich von 0 bis 255 liegen. Beispiel: 192.168.0.0.

**IPv6:** Eine IPv6-Literalzeichenfolge ist in eckige Klammern eingeschlossen und enthält hexadezimale Zahlen, die durch Doppelpunkte getrennt sind. Beispiel: \[ ::1 \] oder \[ 3ffe:ffff::6ECB:0101 \] .

### <a name="enablecompatibilityhttplistener"></a>EnableCompatibilityHttpListener

Gibt an, ob der KOMPATIBILITÄTS-HTTP-Listener aktiviert ist. Wenn diese Einstellung *true ist,* lausingt der Listener zusätzlich zu Port 5985 an Port 80. Der Standardwert ist *False*.

### <a name="enablecompatibilityhttpslistener"></a>EnableCompatibilityHttpsListener

Gibt an, ob der KOMPATIBILITÄTS-HTTPS-Listener aktiviert ist. Wenn diese Einstellung *true ist,* lausingt der Listener zusätzlich zu Port 5986 an Port 443. Der Standardwert ist *False*.

## <a name="winrs-default-configuration-settings"></a>Winrs-Standardkonfigurations-Einstellungen

`winrm quickconfig`konfiguriert auch **die Winrs-Standardeinstellungen.**

### <a name="allowremoteshellaccess"></a>AllowRemoteShellAccess

Ermöglicht den Zugriff auf Remoteshells. Wenn Sie diesen Parameter auf *False festlegen,* werden neue Remoteshellverbindungen vom Server abgelehnt. Der Standardwert ist *True*.

### <a name="idletimeout"></a>IdleTimeout

Gibt die maximale Zeit in Millisekunden an, die die Remoteshell geöffnet bleibt, wenn keine Benutzeraktivität in der Remoteshell vorhanden ist. Die Remoteshell wird automatisch nach dem angegebenen Zeitpunkt gelöscht.

**WinRM 2.0:** Der Standardwert ist 180000. Der Mindestwert ist 60000. Das Festlegen dieses Werts unter 60.000 hat keine Auswirkungen auf das Time out.

### <a name="maxconcurrentusers"></a>MaxConcurrentUsers

Gibt die maximale Anzahl von Benutzern an, die gleichzeitig Remotevorgänge auf demselben Computer über eine Remoteshell ausführen können. Neue Remoteshellverbindungen werden abgelehnt, wenn sie den angegebenen Grenzwert überschreiten. Der Standardwert ist 5.

### <a name="maxshellruntime"></a>MaxShellRunTime

Gibt die maximale Zeit in Millisekunden an, die der Remotebefehl oder das Remoteskript ausführen darf. Der Standardwert ist 28800000.

**WinRM 2.0:** Die Einstellung MaxShellRunTime ist auf schreibgeschützt festgelegt. Das Ändern des Werts für MaxShellRunTime hat keine Auswirkungen auf die Remoteshells.

### <a name="maxprocessespershell"></a>MaxProcessesPerShell

Gibt die maximale Anzahl von Prozessen an, die jeder Shellvorgang starten darf. Der Wert 0 ermöglicht eine unbegrenzte Anzahl von Prozessen. Der Standardwert beträgt 15.

### <a name="maxmemorypershellmb"></a>MaxMemoryPerShellMB

Gibt die maximale Menge an Arbeitsspeicher an, die pro Shell zugeordnet ist, einschließlich der untergeordneten Prozesse der Shell. Der Standardwert ist 150 MB.

### <a name="maxshellsperuser"></a>MaxShellsPerUser

Gibt die maximale Anzahl gleichzeitiger Shells an, die ein Benutzer im Remotebetrieb auf demselben Computer öffnen kann. Wenn diese Richtlinieneinstellung aktiviert ist, kann der Benutzer keine neuen Remoteshells öffnen, wenn die Anzahl den angegebenen Grenzwert überschreitet. Wenn diese Richtlinieneinstellung deaktiviert oder nicht konfiguriert ist, wird der Grenzwert standardmäßig auf fünf (5) Remoteshells pro Benutzer festgelegt.

## <a name="configuring-winrm-with-group-policy"></a>Konfigurieren von WinRM mit Gruppenrichtlinie

Verwenden Sie den Gruppenrichtlinie-Editor, um Windows Remote Shell und WinRM für Computer in Ihrem Unternehmen zu konfigurieren.

### <a name="to-configure-with-group-policy"></a>So konfigurieren Sie Gruppenrichtlinie

1. Öffnen Sie ein Eingabeaufforderungsfenster als ein Administrator.
2. Geben Sie an der Eingabeaufforderung `gpedit.msc` ein. Das **Gruppenrichtlinienobjekt-Editor** wird geöffnet.
3. Suchen Sie **Windows remote management** and Windows Remote **Shell** Gruppenrichtlinie Objects (GPO) unter Computer Configuration Administrative Vorlagen **Windows \\ \\ Components**(Computerkonfigurationskomponenten).
4. Wählen Sie **auf der** Registerkarte Erweitert eine Einstellung aus, um eine Beschreibung zu sehen. Doppelklicken Sie auf eine Einstellung, um sie zu bearbeiten.

## <a name="windows-firewall-and-winrm-20-ports"></a>Windows Firewall- und WinRM 2.0-Ports

Ab WinRM 2.0 sind die von konfigurierten Standardlistenerports Port `Winrm quickconfig` 5985 für HTTP-Transport und Port 5986 für HTTPS. WinRM-Listener können auf jedem beliebigen Port konfiguriert werden.

Wenn ein Computer auf WinRM 2.0 aktualisiert wird, werden die zuvor konfigurierten Listener migriert und empfangen weiterhin Datenverkehr.

## <a name="winrm-installation-and-configuration-notes"></a>Hinweise zur WinRM-Installation und -Konfiguration

WinRM ist nicht von einem anderen Dienst mit Ausnahme von WinHttp abhängig. Wenn der IIS-Administratordienst auf demselben Computer installiert ist, werden möglicherweise Meldungen angezeigt, die darauf hinweisen, dass WinRM nicht vor dem Internetinformationsdienste (IIS) geladen werden kann. WinRM hängt jedoch nicht tatsächlich von IIS ab, da die Lade reihenfolge sicherstellt, dass der IIS-Dienst vor dem &mdash; HTTP-Dienst gestartet wird. WinRM erfordert, dass `WinHTTP.dll` registriert wird.

Wenn der ISA2004-Firewallclient auf dem Computer installiert ist, kann dies dazu führen, dass ein WS-Management-Client (Web Services for Management) nicht mehr reagiert. Installieren Sie ISA2004 Firewall SP1, um dieses Problem zu vermeiden.

Wenn zwei Listenerdienste mit unterschiedlichen IP-Adressen mit der gleichen Portnummer und demselben Computernamen konfiguriert sind, lausingt oder empfängt WinRM Nachrichten nur an einer Adresse. Dies liegt daran, dass die url-Präfixe, die WS-Management Protokoll verwendet werden, identisch sind.

## <a name="ipmi-driver-and-provider-installation-notes"></a>Installationshinweise zum IPMI-Treiber und -Anbieter

Der Treiber erkennt möglicherweise nicht das Vorhandensein von IPMI-Treibern, die nicht von Microsoft kommen. Wenn der Treiber nicht gestartet werden kann, müssen Sie ihn möglicherweise deaktivieren.

If the [baseboard management controller (BMC)](./windows-remote-management-glossary.md#b) resources appear in the system BIOS, then ACPI (Plug and Play) detects the BMC hardware, and automatically installs the IPMI driver. Plug & Play unterstützung ist möglicherweise nicht in allen BMCs vorhanden. Wenn der BMC von der Plug & Play erkannt wird, wird ein unbekanntes Gerät in Geräte-Manager angezeigt, bevor die Hardwareverwaltungskomponente installiert wird. Wenn der Treiber installiert ist, wird eine neue Komponente, das Microsoft ACPI Generic IPMI Compliant Device, in Geräte-Manager.

Wenn Ihr System den BMC nicht automatisch erkennt und den Treiber installiert, während des Setupvorgangs jedoch ein BMC erkannt wurde, müssen Sie das BMC-Gerät erstellen. Geben Sie dazu den folgenden Befehl an einer Eingabeaufforderung ein: `Rundll32 ipmisetp.dll, AddTheDevice` . Nachdem dieser Befehl ausgeführt wurde, wird das IPMI-Gerät erstellt und in der Geräte-Manager. Wenn Sie die Hardwareverwaltungskomponente deinstallieren, wird das Gerät entfernt.

Weitere Informationen finden Sie unter [Einführung in die Hardwareverwaltung.](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10))

Der IPMI-Anbieter platziert die Hardwareklassen im **\\ Stammhardwarenamespace** von WMI. [](/windows/desktop/WmiSdk/gloss-n) Weitere Informationen zu den Hardwareklassen finden Sie unter [IPMI-Anbieter.](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) Weitere Informationen zu *WMI-Namespaces finden* Sie unter [WMI-Architektur](/windows/desktop/WmiSdk/wmi-architecture).

## <a name="wmi-plug-in-configuration-notes"></a>Konfigurationshinweise zum WMI-Plug-In

Ab Windows 8 und Windows Server 2012 [verfügen WMI-Plug-Ins](./windows-remote-management-glossary.md#w) über eigene Sicherheitskonfigurationen. Damit ein normaler Oder-Power-Benutzer (kein Administrator) das *WMI-Plug-In* verwenden kann, [](./windows-remote-management-glossary.md#l) müssen Sie den Zugriff für diesen Benutzer aktivieren, nachdem der Listener konfiguriert wurde. Zunächst müssen Sie den Benutzer mit einem dieser Schritte für den Remotezugriff auf [WMI](./windows-remote-management-glossary.md#w) einrichten.

- Führen `lusrmgr.msc` Sie aus, um den Benutzer der **Gruppe \_ \_ WinRMRemoteWMIUsers** im Fenster **Lokale Benutzer** und Gruppen hinzuzufügen, oder
- Verwenden Sie **das Befehlszeilentool winrm,** um die [](./windows-remote-management-glossary.md#n) Sicherheitsbeschreibung für den Namespace des [WMI-Plug-Ins](./windows-remote-management-glossary.md#w)wie folgt zu konfigurieren: `winrm configSDDL http://schemas.microsoft.com/wbem/wsman/1/wmi/ WmiNamespace` .

Wenn die Benutzeroberfläche angezeigt wird, fügen Sie den Benutzer hinzu.

Nachdem Sie den Benutzer für den Remotezugriff auf [WMI](./windows-remote-management-glossary.md#w)eingerichtet haben, müssen Sie *WMI* einrichten, damit der Benutzer auf das Plug-In zugreifen kann. Führen Sie hierzu aus, um die WMI-Sicherheit für den Namespace zu ändern, auf den im `wmimgmt.msc` **Fenster WMI-Steuerung zugegriffen werden** soll.  [](./windows-remote-management-glossary.md#n)

Die meisten WMI-Klassen für die Verwaltung befinden sich im **\\ Cimv2-Stammnamespace.**