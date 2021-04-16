---
title: 'Installation und Konfiguration für Windows-Remoteverwaltung '
description: Damit Windows-Remoteverwaltung (WinRM)-Skripts ausgeführt werden und das **WinRM** -Befehlszeilen Tool zum Ausführen von Daten Vorgängen ausgeführt werden kann, muss Windows-Remoteverwaltung (WinRM) installiert und konfiguriert sein.
ms.date: 08/31/2020
ms.assetid: 81c40456-0003-46d0-8695-83bf77432056
ms.topic: article
ms.custom: contperf-fy21q1
ms.openlocfilehash: 4ebe4094984f237a3c8949392e3e9a6b47b8afe6
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/04/2021
ms.locfileid: "104520336"
---
# <a name="installation-and-configuration-for-windows-remote-management"></a>Installation und Konfiguration für Windows-Remoteverwaltung

Damit Windows-Remoteverwaltung (WinRM)-Skripts ausgeführt werden und das **WinRM** -Befehlszeilen Tool zum Ausführen von Daten Vorgängen ausgeführt werden kann, muss Windows-Remoteverwaltung (WinRM) installiert und konfiguriert sein.

Diese Elemente sind auch von der WinRM-Konfiguration abhängig.

- [Windows Remote Shell](./windows-remote-management-glossary.md#w) -Befehlszeilen Tool (**Winrs**).
- [Ereignis Weiterleitung](./windows-remote-management-glossary.md#e).
- Windows PowerShell 2,0-Remoting.

## <a name="where-winrm-is-installed"></a>Wo WinRM installiert ist

WinRM wird automatisch mit allen derzeit unterstützten Versionen des Windows-Betriebssystems installiert.

## <a name="configuration-of-winrm-and-ipmi"></a>Konfiguration von WinRM und IPMI

Diese WinRM-und [Intelligent Platform Management Interface (IPMI)](./windows-remote-management-glossary.md#i) - [WMI-Anbieter](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) Komponenten werden mit dem Betriebssystem installiert.

- Der WinRM-Dienst wird automatisch unter Windows Server 2008 und in den Stationen gestartet (unter Windows Vista müssen Sie den Dienst manuell starten).
- Standardmäßig ist kein WinRM- [Listener](./windows-remote-management-glossary.md#l) konfiguriert. Auch wenn der WinRM-Dienst ausgeführt wird, können WS-Management Protokoll [Nachrichten](./windows-remote-management-glossary.md#m) , die Daten anfordern, nicht empfangen oder gesendet werden.
- Internet Connection Firewall (ICF) blockiert den Zugriff auf die Ports.

Verwenden Sie den **WinRM** -Befehl, um Listener und Adressen zu suchen, indem Sie den folgenden Befehl an einer Eingabeaufforderung eingeben.

```console
winrm e winrm/config/listener
```

Geben Sie den folgenden Befehl ein, um den Status der Konfigurationseinstellungen zu überprüfen.

```console
winrm get winrm/config
```

## <a name="quick-default-configuration"></a>Schnelle Standardkonfiguration

Sie können das WS-Management-Protokoll auf dem lokalen Computer aktivieren und die Standardkonfiguration für die Remote Verwaltung mit dem Befehl einrichten `winrm quickconfig` .

Der `winrm quickconfig` Befehl (oder die abgekürzte Version `winrm qc` ) führt diese Vorgänge aus.

- Startet den WinRM-Dienst und legt den Starttyp des dienstanes auf automatisch starten fest.
- Konfiguriert einen Listener für die Ports, die WS-Management Protokoll [Nachrichten](./windows-remote-management-glossary.md#m) über HTTP oder HTTPS an eine beliebige IP-Adresse senden und empfangen.
- Definiert ICF-Ausnahmen für den WinRM-Dienst und öffnet die Ports für http und HTTPS.

> [!NOTE]
> Der `winrm quickconfig` Befehl erstellt eine Firewallausnahme nur für das aktuelle Benutzerprofil. Wenn das Firewallprofil aus irgendeinem Grund geändert wird, müssen Sie ausführen, `winrm quickconfig` um die Firewallausnahme für das neue Profil zu aktivieren. andernfalls ist die Ausnahme möglicherweise nicht aktiviert.

Zum Abrufen von Informationen zum Anpassen einer Konfiguration geben Sie `winrm help config` an einer Eingabeaufforderung ein.

### <a name="to-configure-winrm-with-default-settings"></a>So konfigurieren Sie WinRM mit Standardeinstellungen

1. Geben Sie `winrm quickconfig` an einer Eingabeaufforderung ein.

   Wenn Sie nicht unter dem Administrator Konto für den lokalen Computer ausgeführt werden, müssen Sie entweder im **Startmenü** **als Administrator ausführen** auswählen oder den Befehl **runas** an einer Eingabeaufforderung verwenden.

2. Wenn das Tool anzeigt, **dass diese Änderungen \[ y/n \] ?** sind, geben Sie **y** ein.

   Wenn die Konfiguration erfolgreich ist, wird die folgende Ausgabe angezeigt.

   ``` syntax
   WinRM has been updated for remote management.

   WinRM service type changed to delayed auto start.
   WinRM service started.
   Created a WinRM listener on https://* to accept WS-Man requests to any IP on this machine.
   ```

3. Behalten Sie die Standardeinstellungen für die Client-und Serverkomponenten von WinRM bei, oder passen Sie Sie an. Beispielsweise müssen Sie möglicherweise bestimmte Remote Computer der Liste der Clientkonfigurations-Kunden Hosts hinzufügen.

   Sie sollten eine Liste vertrauenswürdiger Hosts einrichten, wenn die gegenseitige Authentifizierung nicht festgelegt werden kann. Kerberos ermöglicht die gegenseitige Authentifizierung, kann aber nicht in Domänen verwendet werden, die nur für Arbeitsgruppen gelten &mdash; . Eine bewährte Vorgehensweise beim Einrichten vertrauenswürdiger Hosts für eine Arbeitsgruppe besteht darin, die Liste so eingeschränkt wie möglich zu gestalten.

4. Erstellen Sie einen HTTPS-Listener, indem Sie den Befehl eingeben `winrm quickconfig -transport:https` . Beachten Sie, dass Sie Port 5986 öffnen müssen, damit der HTTPS-Transport funktioniert.

## <a name="listener-and-ws-management-protocol-default-settings"></a>Standardeinstellungen für Listener und WS-Management-Protokoll

Um die Listenerkonfiguration zu erhalten, geben Sie `winrm enumerate winrm/config/listener` an einer Eingabeaufforderung ein. Listener werden durch einen Transport (http oder HTTPS) und eine IPv4-oder IPv6-Adresse definiert.

`winrm quickconfig` erstellt die folgenden Standardeinstellungen für einen Listener. Sie können mehr als einen Listener erstellen. Geben Sie `winrm help config` an einer Eingabeaufforderung ein, um weitere Informationen zu erhalten.

### <a name="address"></a>Adresse

Gibt die Adresse an, für die der Listener erstellt wurde.

### <a name="transport"></a>Transport

Legt den Transport zum Senden und Empfangen von WS-Management-Protokollanforderungen und -antworten fest. Der Wert muss entweder " *http* " oder " *https*" lauten. Der Standardwert ist " *http*".

### <a name="port"></a>Port

Gibt den TCP-Port an, für den der Listener erstellt wird.

**WinRM 2,0:** Der Standard-HTTP-Port ist 5985.

### <a name="hostname"></a>Hostname

Gibt den Hostnamen des Computers an, auf dem der WinRM-Dienst ausgeführt wird. Der Wert muss ein voll qualifizierter Domänen Name, eine IPv4-oder IPv6-Literalzeichenfolge oder ein Platzhalter Zeichen sein.

### <a name="enabled"></a>Aktiviert

Gibt an, ob der Listener aktiviert oder deaktiviert ist. Der Standardwert ist *True*.

### <a name="urlprefix"></a>URLPrefix

Gibt ein URL-Präfix an, über das http-oder HTTPS-Anforderungen akzeptiert werden. Dabei handelt es sich um eine Zeichenfolge, die nur die Zeichen a-z, a-z, 9-0, Unterstrich ( \_ ) und Schrägstrich (/) enthält. Die Zeichenfolge darf nicht mit einem Schrägstrich (/) beginnen oder enden. Wenn der Computername beispielsweise Sample Machine lautet, würde der WinRM-Client https://SampleMachine/< in der Zieladresse *URLPrefix* -> angeben. Das Standard-URL-Präfix lautet "wsman".

### <a name="certificatethumbprint"></a>CertificateThumbprint

Gibt den Fingerabdruck des Dienstzertifikats an. Dieser Wert stellt eine Zeichenfolge aus zweistelligen hexadezimalen Werten dar, die im Feld Fingerabdruck des Zertifikats gefunden werden. Diese Zeichenfolge enthält den SHA-1-Hash des Zertifikats. Zertifikate werden bei der clientzertifikatbasierten Authentifizierung verwendet. Zertifikate können nur lokalen Benutzerkonten zugeordnet werden und funktionieren nicht mit Domänen Konten.

### <a name="listeningon"></a>ListeningOn

Gibt die IPv4-und IPv6-Adressen an, die der Listener verwendet. Beispiel: "111.0.0.1, 111.222.333.444,:: 1, 1000:2000:2C: 3: C19:9ec8: A715:5e24, 3FFE: 8311: FFFF: f70f: 0:5EFE: 111.222.333.444, FE80:: 5EFE: 111.222.333.444% 8, FE80:: C19:9ec8: A715:5e24% 6".

## <a name="protocol-default-settings"></a>Protokoll Standardeinstellungen

Viele der Konfigurationseinstellungen, wie z. b. maxenvelopesizekb oder soaptraceaktivi, bestimmen, wie die WinRM-Client-und-Serverkomponenten mit dem WS-Management Protokoll interagieren. In der folgenden Liste werden die verfügbaren Konfigurationseinstellungen beschrieben.

### <a name="maxenvelopesizekb"></a>MaxEnvelopeSizekb

Gibt die maximalen SOAP (Simple Object Access Protocol)-Daten in Kilobyte an. Der Standardwert ist 150 Kilobyte.

> [!NOTE]  
> Das Verhalten wird nicht unterstützt, wenn für maxenvelopesizekb ein Wert größer als 1039440 festgelegt ist.

### <a name="maxtimeoutms"></a>Maxtimeoutms

Gibt den maximalen Timeout Wert (in Millisekunden) an, der für alle anderen Anforderungen als Pull Requests verwendet werden kann. Der Standardwert ist 60000.

### <a name="maxbatchitems"></a>MaxBatchItems

Gibt die maximale Anzahl von Elementen an, die als Pull-Antwort verwendet werden können. Der Standardwert ist 32000.

### <a name="maxproviderrequests"></a>MaxProviderRequests

Gibt die maximale Anzahl gleichzeitiger Anforderungen vom Dienst an, die zulässig sind. Der Standard ist 25.

**WinRM 2,0:** Diese Einstellung ist veraltet, und wird auf schreibgeschützt festgelegt.

## <a name="winrm-client-default-configuration-settings"></a>Standard Konfigurationseinstellungen für den WinRM-Client

Die Client Version von WinRM verfügt über die folgenden Standard Konfigurationseinstellungen.

### <a name="networkdelayms"></a>Networkdelta-MS

Gibt die Zeit in Millisekunden an, die der Clientcomputer wartet, um der Netzwerk-Verzögerungszeit gerecht zu werden. Der Standardwert ist 5000 Millisekunden.

### <a name="urlprefix"></a>URLPrefix

Gibt ein URL-Präfix an, über das http-oder HTTPS-Anforderungen akzeptiert werden. Das Standard-URL-Präfix lautet "wsman".

### <a name="allowunencrypted"></a>"Zuweisung"

Ermöglicht es dem Clientcomputer, unverschlüsselten Verkehr anzufordern. Standardmäßig ist für den Client Computer verschlüsselter Netzwerkverkehr erforderlich, und diese Einstellung ist *false*.

### <a name="basic"></a>Basic

Ermöglicht es dem Clientcomputer, die Standardauthentifizierung zu verwenden. Standardauthentifizierung ist ein Schema, in dem der Benutzername und das Kennwort in Klartext an den Server oder Proxy gesendet werden. Diese Methode ist die am wenigsten sichere Authentifizierungsmethode. Der Standardwert ist *True*.

### <a name="digest"></a>Digest

Ermöglicht dem Client, Digestauthentifizierung zu verwenden. Die Digestauthentifizierung ist ein Abfrage/Antwort-Schema, das eine serverspezifische Zeichenfolge für die Abfrage verwendet. Nur der Clientcomputer kann eine Anforderung der Digestauthentifizierung initiieren. Der Client Computer sendet eine Anforderung an den Server, um sich zu authentifizieren, und empfängt eine Tokenzeichenfolge vom Server. Anschließend sendet der Client Computer die Ressourcen Anforderung, einschließlich des Benutzernamens und eines kryptografischen Hashs des Kennworts, in Kombination mit der Tokenzeichenfolge. Digestauthentifizierung wird für HTTP und HTTPS unterstützt. WinRM-shellclientskripts und-Anwendungen können die Digestauthentifizierung angeben, aber der WinRM-Dienst akzeptiert keine Digestauthentifizierung. Der Standardwert ist *True*.

> [!NOTE]
> Digestauthentifizierung über HTTP wird nicht als sicher betrachtet.

### <a name="certificate"></a>Zertifikat

Ermöglicht dem Client die Verwendung der Client Zertifikat basierten Authentifizierung. Die Zertifikat basierte Authentifizierung ist ein Schema, bei dem der Server einen Client authentifiziert, der durch ein X509-Zertifikat identifiziert wird. Der Standardwert ist *True*.

### <a name="kerberos"></a>Kerberos

Ermöglicht dem Client, Kerberos-Authentifizierung zu verwenden. Kerberos-Authentifizierung ist ein Schema, in dem sich der Client und Server gegenseitig mit Kerberos-Zertifikaten authentifizieren. Der Standardwert ist *True*.

### <a name="negotiate"></a>Aushandeln

Ermöglicht dem Client, Negotiate-Authentifizierung zu verwenden. Negotiate-Authentifizierung ist ein Schema, in dem der Client eine Anforderung an den zu authentifizierenden Server sendet. Der Server bestimmt, ob Kerberos oder NTLM verwendet wird. Das Kerberos-Protokoll wird zur Authentifizierung eines Domänenkontos ausgewählt und NTLM für lokale Computerkonten. Der Benutzername muss \\ \_ für einen Domänen Benutzer im Format des Domänen Benutzernamens angegeben werden. Der Benutzername muss im Format "Server \_ Name \\ Benutzer \_ Name" für einen lokalen Benutzer auf einem Server Computer angegeben werden. Der Standardwert ist *True*.

### <a name="credssp"></a>CredSSP

Ermöglicht dem Client die Verwendung der Authentifizierung von Credential Security Support Provider (kredssp). Mit "kredssp" kann eine Anwendung die Anmelde Informationen des Benutzers vom Client Computer an den Zielserver delegieren. Der Standardwert ist *False*.

### <a name="defaultports"></a>DefaultPorts

Gibt die Ports an, die vom Client für http oder HTTPS verwendet werden.

**WinRM 2,0:** Der Standard-HTTP-Port ist 5985, und der HTTPS-Standardport ist 5986.

### <a name="trustedhosts"></a>TrustedHosts

Gibt die Liste der Remote Computer an, die als vertrauenswürdig eingestuft werden. Andere Computer in einer Arbeitsgruppe oder Computer in einer anderen Domäne sollten dieser Liste hinzugefügt werden.

> [!Note]
> Die Computer in der Liste "Treuhänder Hosts" sind nicht authentifiziert. Der Client kann Anmelde Informationen an diese Computer senden.

Wenn eine IPv6-Adresse für einen "Treuhänder Host" angegeben wird, muss die Adresse in eckige Klammern eingeschlossen werden, wie im folgenden WinRM Utility-Befehl veranschaulicht: `winrm set winrm/config/client '@{TrustedHosts ="[0:0:0:0:0:0:0:0]"}'` .

Weitere Informationen zum Hinzufügen von Computern zur Liste "Treuhänder Hosts" erhalten Sie, wenn Sie eingeben `winrm help config` .

## <a name="winrm-service-default-configuration-settings"></a>Standard Konfigurationseinstellungen für den WinRM-Dienst

Die Dienst Version von WinRM verfügt über die folgenden Standard Konfigurationseinstellungen.

### <a name="rootsddl"></a>RootSDDL

Gibt die Sicherheits Beschreibung an, die den Remote Zugriff auf den Listener steuert. Der Standardwert ist "o:NSG: schlecht: P (A;; GA;;; BA) (A;; Gr;;; ER) s:p (AU, FA; GA;;; WD) (au; sa; Gwgx;;; WD) ".

### <a name="maxconcurrentoperations"></a>Maxconcurrentoperations

Die maximale Anzahl von gleichzeitigen Vorgängen. Der Standard ist 100.

**WinRM 2,0:** Die maxconcurrentoperations-Einstellung ist veraltet, und wird auf schreibgeschützt festgelegt. Diese Einstellung wurde durch "maxconcurrentoperationsperuser" ersetzt.

### <a name="maxconcurrentoperationsperuser"></a>Maxconcurrentoperationsperuser

Gibt die maximale Anzahl von gleichzeitigen Vorgängen an, die ein Benutzer auf demselben System Remote öffnen kann. Standardmäßig sind 1500 eingestellt.

### <a name="enumerationtimeoutms"></a>Enumerationtimeoutms

Gibt das Leerlauf Timeout in Millisekunden zwischen Pull-Nachrichten an. Der Standardwert ist 60000.

### <a name="maxconnections"></a>MaxConnections

Gibt die maximale Anzahl aktiver Anforderungen an, die der Dienst gleichzeitig verarbeiten kann. Der Standardwert ist 300.

**WinRM 2,0:** Der Standardwert ist 25.

### <a name="maxpacketretrievaltimeseconds"></a>Maxpacketretrievaltimeseconds

Gibt die maximale Zeitspanne in Sekunden an, die der WinRM-Dienst zum Abrufen eines Pakets benötigt. Der Standardwert ist 120 Sekunden.

### <a name="allowunencrypted"></a>"Zuweisung"

Ermöglicht es dem Clientcomputer, unverschlüsselten Verkehr anzufordern. Der Standardwert ist *False*.

### <a name="basic"></a>Basic

Ermöglicht dem WinRM-Dienst die Verwendung der Standard Authentifizierung. Der Standardwert ist *False*.

### <a name="certificate"></a>Zertifikat

Ermöglicht dem WinRM-Dienst die Verwendung der Client Zertifikat basierten Authentifizierung. Der Standardwert ist *False*.

### <a name="kerberos"></a>Kerberos

Ermöglicht dem WinRM-Dienst die Verwendung der Kerberos-Authentifizierung. Der Standardwert ist *True*.

### <a name="negotiate"></a>Aushandeln

Ermöglicht dem WinRM-Dienst die Verwendung der Aushandlungs Authentifizierung. Der Standardwert ist *True*.

### <a name="credssp"></a>CredSSP

Ermöglicht dem WinRM-Dienst die Verwendung der Authentifizierung von Credential Security Support Provider (kredssp). Der Standardwert ist *False*.

### <a name="cbthardeninglevel"></a>CbtHardeningLevel

Legt die Richtlinie für Kanalbindungstoken-Anforderungen in Authentifizierungsanforderungen fest. Der Standardwert ist *gelockert*.

### <a name="defaultports"></a>DefaultPorts

Gibt die Ports an, die vom WinRM-Dienst für http oder HTTPS verwendet werden.

**WinRM 2,0:** Der Standard-HTTP-Port ist 5985, und der HTTPS-Standardport ist 5986.

### <a name="ipv4filter-and-ipv6filter"></a>IPv4Filter und IPv6Filter

Gibt die IPv4-oder IPv6-Adressen an, die Listener verwenden können. Die Standardwerte sind IPv4Filter = \* und IPv6Filter = \* .

**IPv4:** Eine IPv4-Literalzeichenfolge besteht aus vier Dezimalzahlen im Bereich von 0 bis 255. Beispiel: 192.168.0.0.

**IPv6:** Eine IPv6-Literalzeichenfolge wird in eckige Klammern eingeschlossen und enthält hexadezimale Zahlen, die durch Doppelpunkte getrennt sind. Beispiel: \[ :: 1 \] oder \[ 3FFE: FFFF:: 6ecb: 0101 \] .

### <a name="enablecompatibilityhttplistener"></a>Enablecompatibilityhttplistener

Gibt an, ob der Kompatibilitäts-http-Listener aktiviert ist. Wenn diese Einstellung auf *true* festgelegt ist, lauscht der Listener zusätzlich zu Port 5985 an Port 80. Der Standardwert ist *False*.

### <a name="enablecompatibilityhttpslistener"></a>Enablecompatibilityhttpslistener

Gibt an, ob der Kompatibilitäts-HTTPS-Listener aktiviert ist. Wenn diese Einstellung auf *true* festgelegt ist, lauscht der Listener zusätzlich zu Port 5986 an Port 443. Der Standardwert ist *False*.

## <a name="winrs-default-configuration-settings"></a>Winrs-Standard Konfigurationseinstellungen

`winrm quickconfig` konfiguriert auch die **Winrs** -Standardeinstellungen.

### <a name="allowremoteshellaccess"></a>AllowRemoteShellAccess

Ermöglicht den Zugriff auf Remoteshells. Wenn Sie diesen Parameter auf *false* festlegen, werden neue remoteshellverbindungen vom Server abgelehnt. Der Standardwert ist *True*.

### <a name="idletimeout"></a>IdleTimeout

Gibt die maximale Zeit in Millisekunden an, die die Remoteshell geöffnet bleibt, wenn keine Benutzeraktivität in der Remoteshell vorhanden ist. Die Remoteshell wird automatisch nach dem angegebenen Zeitpunkt gelöscht.

**WinRM 2,0:** Der Standardwert ist 180000. Der Minimalwert ist 60000. Wenn dieser Wert niedriger als 60000 festgelegt wird, hat dies keine Auswirkung auf das Timeout.

### <a name="maxconcurrentusers"></a>MaxConcurrentUsers

Gibt die maximale Anzahl von Benutzern an, die gleichzeitig Remotevorgänge auf demselben Computer über eine Remoteshell ausführen können. Neue remoteshellverbindungen werden abgelehnt, wenn Sie den angegebenen Grenzwert überschreiten. Der Standardwert ist 5.

### <a name="maxshellruntime"></a>MaxShellRunTime

Gibt die maximale Zeit in Millisekunden an, für die der Remote Befehl oder das Skript ausgeführt werden darf. Der Standardwert ist 28,8 Millionen.

**WinRM 2,0:** Die maxshellruntime-Einstellung ist auf schreibgeschützt festgelegt. Das Ändern des Werts für maxshellruntime hat keine Auswirkung auf die Remote Shells.

### <a name="maxprocessespershell"></a>MaxProcessesPerShell

Gibt die maximale Anzahl von Prozessen an, die jeder Shellvorgang starten darf. Der Wert 0 ermöglicht eine unbegrenzte Anzahl von Prozessen. Der Standardwert beträgt 15.

### <a name="maxmemorypershellmb"></a>MaxMemoryPerShellMB

Gibt die maximale Menge an Arbeitsspeicher an, die Pro Shell zugeordnet ist, einschließlich der untergeordneten Prozesse der Shell. Der Standardwert ist 150 MB.

### <a name="maxshellsperuser"></a>MaxShellsPerUser

Gibt die maximale Anzahl gleichzeitiger Shells an, die ein Benutzer im Remotebetrieb auf demselben Computer öffnen kann. Wenn diese Richtlinien Einstellung aktiviert ist, kann der Benutzer keine neuen Remoteshells öffnen, wenn die Anzahl den angegebenen Grenzwert überschreitet. Wenn diese Richtlinieneinstellung deaktiviert oder nicht konfiguriert ist, wird der Grenzwert standardmäßig auf fünf (5) Remoteshells pro Benutzer festgelegt.

## <a name="configuring-winrm-with-group-policy"></a>Konfigurieren von WinRM mit Gruppenrichtlinie

Verwenden Sie den Gruppenrichtlinie-Editor, um Windows-Remoteshell und WinRM für Computer in Ihrem Unternehmen zu konfigurieren.

### <a name="to-configure-with-group-policy"></a>So konfigurieren Sie mit Gruppenrichtlinie

1. Öffnen Sie ein Eingabeaufforderungsfenster als ein Administrator.
2. Geben Sie an der Eingabeaufforderung ein `gpedit.msc` . Das **Gruppenrichtlinienobjekt-Editor** Fenster wird geöffnet.
3. Suchen Sie die **Windows-Remoteverwaltung** und **Windows remotesshell** Gruppenrichtlinie Objects (GPO) unter **Computer Konfiguration \\ Administrative Vorlagen \\ Windows-Komponenten**.
4. Wählen Sie auf der Registerkarte **erweitert** eine Einstellung aus, um eine Beschreibung anzuzeigen. Doppelklicken Sie auf eine Einstellung, um Sie zu bearbeiten.

## <a name="windows-firewall-and-winrm-20-ports"></a>Ports für die Windows-Firewall und WinRM 2,0

Ab WinRM 2,0 sind die von konfigurierten Standardüberwachungsports `Winrm quickconfig` Port 5985 für den HTTP-Transport und Port 5986 für HTTPS. WinRM-Listener können an einem beliebigen Port konfiguriert werden.

Wenn ein Computer auf WinRM 2,0 aktualisiert wird, werden die zuvor konfigurierten Listener migriert und empfangen weiterhin Datenverkehr.

## <a name="winrm-installation-and-configuration-notes"></a>WinRM-Installations-und Konfigurations Hinweise

WinRM ist nicht von einem anderen Dienst mit Ausnahme von WinHTTP abhängig. Wenn der IIS-Verwaltungsdienst auf demselben Computer installiert ist, werden möglicherweise Nachrichten angezeigt, die darauf hinweisen, dass WinRM vor Internetinformationsdienste (IIS) nicht geladen werden kann. WinRM ist jedoch nicht von IIS abhängig, &mdash; da diese Nachrichten auftreten, da die Lade Reihenfolge sicherstellt, dass der IIS-Dienst vor dem HTTP-Dienst startet. WinRM erfordert, dass `WinHTTP.dll` registriert wird.

Wenn der ISA2004-Firewall-Client auf dem Computer installiert ist, kann dies dazu führen, dass ein Webdienst für die Verwaltung (WS-Management) nicht mehr reagiert. Installieren Sie ISA2004 Firewall SP1, um dieses Problem zu vermeiden.

Wenn zwei Listener-Dienste mit unterschiedlichen IP-Adressen mit der gleichen Portnummer und dem gleichen Computernamen konfiguriert sind, wird von WinRM nur eine Adresse überwacht oder empfangen. Dies liegt daran, dass die vom WS-Management Protokoll verwendeten URL-Präfixe identisch sind.

## <a name="ipmi-driver-and-provider-installation-notes"></a>Hinweise zur Installation des IPMI-Treibers und-Anbieters

Der Treiber erkennt möglicherweise nicht, dass IPMI-Treiber vorhanden sind, die nicht von Microsoft stammen. Wenn der Treiber nicht gestartet werden kann, müssen Sie ihn möglicherweise deaktivieren.

Wenn die Ressourcen des [Baseboard-Verwaltungs Controllers (BMC)](./windows-remote-management-glossary.md#b) im System-BIOS angezeigt werden, erkennt ACPI (Plug & Play) die BMC-Hardware und installiert automatisch den IPMI-Treiber. Plug & Play-Unterstützung ist möglicherweise nicht in allen BMCs vorhanden. Wenn der BMC von Plug & Play erkannt wird, wird vor der Installation der Hardware Verwaltungs Komponente in Device Manager ein unbekanntes Gerät angezeigt. Wenn der Treiber installiert ist, wird eine neue Komponente, das generische Microsoft ACPI-IPMI-kompatibles Gerät, in Device Manager angezeigt.

Wenn das System den BMC nicht automatisch erkennt und den Treiber installiert, während des Setup Vorgangs aber ein BMC erkannt wurde, müssen Sie das BMC-Gerät erstellen. Geben Sie hierzu an einer Eingabeaufforderung den folgenden Befehl ein: `Rundll32 ipmisetp.dll, AddTheDevice` . Nachdem dieser Befehl ausgeführt wurde, wird das IPMI-Gerät erstellt und in Device Manager angezeigt. Wenn Sie die Hardware Verwaltungs Komponente deinstallieren, wird das Gerät entfernt.

Weitere Informationen finden Sie unter [Einführung in die Hardware Verwaltung](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)).

Der IPMI-Anbieter platziert die Hardware Klassen im **Stamm \\ Hardware** - [Namespace](/windows/desktop/WmiSdk/gloss-n) von WMI. Weitere Informationen zu den Hardware Klassen finden Sie unter [IPMI-Anbieter](/previous-versions/windows/desktop/ipmiprv/ipmi-provider). Weitere Informationen zu WMI- *Namespaces* finden Sie unter [WMI-Architektur](/windows/desktop/WmiSdk/wmi-architecture).

## <a name="wmi-plug-in-configuration-notes"></a>Hinweise zur Konfiguration des WMI-Plug-ins

Ab Windows 8 und Windows Server 2012 verfügen [WMI-Plug-ins](./windows-remote-management-glossary.md#w) über eigene Sicherheits Konfigurationen. Damit ein normaler oder Leistungs basierter Benutzer (nicht Administrator) das *WMI-Plug-in* verwenden kann, müssen Sie den Zugriff für diesen Benutzer aktivieren, nachdem der [Listener](./windows-remote-management-glossary.md#l) konfiguriert wurde. Zunächst müssen Sie den Benutzer mit einem der folgenden Schritte für den Remote Zugriff auf [WMI](./windows-remote-management-glossary.md#w) einrichten.

- Führen Sie `lusrmgr.msc` aus, um den Benutzer der Gruppe **winrmremotewmiusers \_ \_** im Fenster **lokale Benutzer und Gruppen** hinzuzufügen, oder
- Verwenden Sie das **WinRM** -Befehlszeilen Tool, um die Sicherheits Beschreibung für den [*Namespace*](./windows-remote-management-glossary.md#n) des [WMI-Plug-ins](./windows-remote-management-glossary.md#w)wie folgt zu konfigurieren: `winrm configSDDL http://schemas.microsoft.com/wbem/wsman/1/wmi/ WmiNamespace` .

Fügen Sie den Benutzer hinzu, wenn die Benutzeroberfläche angezeigt wird.

Nachdem Sie den Benutzer für den Remote Zugriff auf [WMI](./windows-remote-management-glossary.md#w)eingerichtet haben, müssen Sie *WMI* einrichten, um dem Benutzer den Zugriff auf das Plug-in zu ermöglichen. Führen Sie hierzu aus, `wmimgmt.msc` um die *WMI* -Sicherheit für den [Namespace](./windows-remote-management-glossary.md#n) zu ändern, auf den im **WMI-Steuerungs** Fenster zugegriffen werden soll.

Der Großteil der WMI-Klassen für die Verwaltung ist im **root \\ CIMV2** -Namespace.