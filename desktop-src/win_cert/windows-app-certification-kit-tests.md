---
title: Tests im Zertifizierungskit für Windows-Apps
description: Im Folgenden finden Sie Testdetails zum Zertifizieren von Dekstop-Apps.
ms.assetid: FA160F46-C266-4F89-B77F-166FEA9ED96B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b251104418e8eeff88d4d0188e34628b5ec1bf3b54015550084d4a0e9df567e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086563"
---
# <a name="windows-app-certification-kit-tests"></a>Tests im Zertifizierungskit für Windows-Apps

Im Folgenden finden Sie Testdetails zum Zertifizieren von Dekstop-Apps. Weitere Informationen finden Sie unter [Verwenden des Windows App Certification Kits.](using-the-windows-app-certification-kit.md)

-   [Bereinige umkehrbare Installation](#clean-reversible-install)
-   [Installieren im richtigen Ordnertest](#install-to-the-correct-folders-test)
-   [Digital signierter Dateitest](#digitally-signed-file-test)
-   [Support x64 Windows test](#support-x64-windows-test)
-   [Test zur Überprüfung der Betriebssystemversion](#os-version-checking-test)
-   [Test der Benutzerkontensteuerung (User Account Control, UAC)](#user-account-control-uac-test)
-   [Befolgen von Systemneustart-Manager-Meldungen](#adhere-to-system-restart-manager-messages)
-   [Tresor Modustest](#safe-mode-test)
-   [Multiuser-Sitzungstest](#multiuser-session-test)
-   [Abstürze und Hängen – Test](#crashes-and-hangs-test)
-   [Kompatibilitäts- und Resilienztest](#compatibility-and-resiliency-test)
-   [Windows-Sicherheit bewährten Methoden – Test](#windows-security-best-practices-test)
-   [Test der Windows-Sicherheitsfeatures](#windows-security-features-test)
-   [Hoher DPI-Test](#high-dpi-test)

## <a name="clean-reversible-install"></a>Bereinige umkehrbare Installation

Installiert und deinstalliert die App und sucht nach Restdateien und Registrierungseinträgen.

-   Hintergrund
    -   Mit einer sauberen, umkehrbaren Installation können Benutzer Apps bereitstellen und entfernen. Um diesen Test bestehen zu können, muss die App Folgendes tun:
        -   Die App erzwingen nicht, dass das System sofort nach der Installation oder Deinstallation der App neu gestartet wird. *Der Installations- oder Deinstallationsprozess einer App sollte niemals einen Systemneustart direkt nach Abschluss erfordern. Wenn dies erfordert, dass das System neu gestartet wird, sollten Benutzer in der Lage sein, das System nach Bedarf neu zu starten.*
        -   Die App ist nicht von 8.3 Kurzdateinamen (Short File Names, SFN) abhängig. *Die Installations- und Deinstallationsprozesse der App müssen lange Dateinamen und Ordnerpfade verwenden können.*
        -   Die Automatische Installation/Deinstallation wird von der App nicht blockiert.
        -   Die App erstellt die erforderlichen Einträge in der Systemregistrierung. *Windows Inventurtools und Telemetrietools erfordern vollständige Informationen zu installierten Apps. App-Installationsprogramme müssen die richtigen Registrierungseinträge erstellen, um eine erfolgreiche Erkennung und Deinstallation zu ermöglichen.*
    -   Wenn Sie ein MSI-basiertes Installationsprogramm verwenden, erstellt MSI automatisch die folgenden Registrierungseinträge. Wenn Sie kein MSI-Installationsprogramm verwenden, muss das Installationsmodul während der Installation die folgenden Registrierungseinträge erstellen:
        -   DisplayName
        -   InstallLocation
        -   Herausgeber
        -   UninstallString
        -   VersionMajor oder MajorVersion
        -   VersionMinor oder MinorVersion
    -   Die App muss alle Einträge in "Programme hinzufügen/entfernen" entfernen.
-   Testdetails
    -   Dieser Test überprüft die Installations- und Deinstallationsprozesse der App auf das erforderliche Verhalten.
-   Korrekturmaßnahme
    -   Überprüfen Sie den Entwurf und das Verhalten der App mit den oben beschriebenen Anforderungen.

## <a name="install-to-the-correct-folders-test"></a>Installieren im richtigen Ordnertest

Überprüft, ob die App ihre Programm- und Datendateien in die richtigen Ordner schreibt.

-   Hintergrund
    -   Apps müssen system- und benutzerspezifische Ordner ordnungsgemäß verwenden, damit sie auf die benötigten Daten und Einstellungen zugreifen und gleichzeitig die Daten und Einstellungen des Benutzers vor nicht autorisiertem Zugriff schützen können.
-   Ordner "Programme"
    -   Die App muss standardmäßig im Ordner Programme installiert sein (%ProgramFiles% für native 32-Bit- und 64-Bit-Apps und %ProgramFiles(x86)% für 32-Bit-Apps, die unter x64 ausgeführt werden).
    -   **Hinweis:** Die App darf aufgrund der für diesen Ordner konfigurierten Sicherheitsberechtigungen keine Benutzer- oder App-Daten in einem Ordner "Programme" speichern.
    -   Die ACLs auf Windows-Systemordnern ermöglichen nur Administratorkonten das Lesen und Schreiben in diese. Daher haben Standardbenutzerkonten keinen Zugriff auf diese Ordner. Mit der Dateivirtualisierung können Apps jedoch eine Datei, z. B. eine Konfigurationsdatei, an einem Systemspeicherort speichern, der in der Regel nur von Administratoren geschrieben werden kann. Das Ausführen von Programmen als Standardbenutzer in dieser Situation kann zu Fehlern führen, wenn er nicht auf eine erforderliche Datei zugreifen kann.
    -   Apps sollten bekannte [Ordner verwenden,](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)) um sicherzustellen, dass sie auf ihre Daten zugreifen können.
    -   **Hinweis: Windows** bietet Dateivirtualisierung, um die App-Kompatibilität zu verbessern und Probleme zu vermeiden, wenn Apps als Standardbenutzer auf einem Windows. Ihre App sollte sich nicht darauf verlassen, dass die Virtualisierung in zukünftigen Versionen von Windows.
-   Benutzerspezifische App-Datenordner
    -   Bei Installationen pro Computer darf die App während der Installation keine benutzerspezifischen Daten schreiben. Benutzerspezifische Installationsdaten sollten nur geschrieben werden, wenn ein Benutzer die App zum ersten Mal startet. Dies liegt daran, dass es keinen richtigen Benutzerspeicherort gibt, an dem Daten zum Zeitpunkt der Installation gespeichert werden. Versuche einer App, das Standardverhalten von Zuordnungen auf Computerebene nach der Installation zu ändern, sind nicht erfolgreich. Stattdessen müssen Standardwerte auf Benutzerebene beansprucht werden, wodurch verhindert wird, dass mehrere Benutzer die Standardwerte der anderen Benutzer überschreiben.
    -   Alle App-Daten, die ausschließlich für einen bestimmten Benutzer gelten und nicht für andere Benutzer des Computers freigegeben werden sollen, müssen in \\ <username> \\ Benutzer-AppData gespeichert werden.
    -   Alle App-Daten, die von Benutzern auf dem Computer gemeinsam genutzt werden müssen, sollten in ProgramData gespeichert werden.
-   Andere Systemordner und Registrierungsschlüssel
    -   Die App sollte niemals direkt in das Windows verzeichnis und oder unterdirectories schreiben. Verwenden Sie die richtigen Methoden zum Installieren von Dateien, z. B. Schriftarten oder Treibern, in diesen Verzeichnissen.
    -   Apps sollten nicht automatisch beim Start gestartet werden, z. B. durch Hinzufügen eines Eintrags zu einem oder mehreren dieser Speicherorte:
        -   Registrierungsschlüssel HKLM und oder HKCU unter Software \\ Microsoft \\ Windows \\ CurrentVersion
        -   Registrierungsschlüssel HKLM und oder HKCU unter Software \\ Wow6432Node \\ Microsoft \\ Windows \\ CurrentVersion
        -   Startmenü AllPrograms > STARTUP
-   Testdetails
    -   Dieser Test überprüft, ob die App die spezifischen Speicherorte im Dateisystem verwendet, die Windows zum Speichern von Programmen und Softwarekomponenten, freigegebenen App-Daten und App-Daten für einen Benutzer bietet.
-   Maßnahmen
    -   Überprüfen Sie, wie die App die Ordner des Systems verwendet, und stellen Sie sicher, dass sie sie ordnungsgemäß verwendet.
-   Ausnahmen und Ausnahmen
    -   Für Desktop-Apps, die in den globalen Assemblycache (GAC) schreiben, ist eine Zurückstellung erforderlich (.NET-Apps sollten Assemblyabhängigkeiten privat halten und im Verzeichnis der App speichern, es sei denn, die Freigabe einer Assembly ist explizit erforderlich).
    -   Die Installation im Ordner Programme ist keine Voraussetzung für Desktop-SW-Pakete, um ein SW-Logo zu erhalten, sondern nur in der Kategorie SW-Grundlagen.

## <a name="digitally-signed-file-test"></a>Digital signierter Dateitest

Testet ausführbare Dateien und Gerätetreiber, um sicherzustellen, dass sie über eine gültige digitale Signatur verfügen.

-   Hintergrund
    -   Digital signierte Dateien ermöglichen es, zu überprüfen, ob die Datei original ist, und zu erkennen, ob die Datei manipuliert wurde.
    -   Die Erzwingung von Codesignaturen Windows Kernelmodus ist ein Feature, das auch als Codeintegrität (Code Integrity, CI) bekannt ist. CI verbessert die Sicherheit von Windows, indem die Integrität einer Datei jedes Mal überprüft wird, wenn sie in den Arbeitsspeicher geladen wird. CI erkennt, ob schädlicher Code eine Binärdatei des Systems geändert hat, und generiert ein Diagnose- und Systemüberwachungsprotokollereignis, wenn die Signatur eines Kernelmoduls nicht ordnungsgemäß überprüft werden kann.
    -   Wenn die App erhöhte Berechtigungen erfordert, zeigt die Eingabeaufforderung für erhöhte Rechte Kontextinformationen zur ausführbaren Datei an, die erhöhte Zugriffsrechte anfordert. Je nachdem, ob die App authenticode signiert ist, wird dem Benutzer möglicherweise die Zustimmungsaufforderung oder die Eingabeaufforderung für Anmeldeinformationen angezeigt.
    -   Starke Namen verhindern, dass Dritte Ihren Code spoofen, solange Sie den privaten Schlüssel schützen. Die .NET Framework überprüft die digitale Signatur, wenn sie die Assembly lädt oder im GAC installiert. Ohne Zugriff auf den privaten Schlüssel kann ein böswilliger Benutzer Ihren Code nicht ändern und erneut signieren.
-   Testdetails
    -   Alle ausführbaren Dateien, z. B. dateien mit den Dateierweiterungen .exe, .dll, .ocx, .sys, .cpl, .drv und .scr, müssen mit einem Authenticode-Zertifikat signiert werden.
    -   Alle von der App installierten Kernelmodustreiber müssen über eine Microsoft-Signatur verfügen, die über das WHQL- oder DRS-Programm erhalten wird. Alle Dateisystemfiltertreiber müssen WHQL-signiert sein.
-   Korrekturmaßnahme
    -   Signieren Sie die ausführbaren Dateien der App.
    -   Verwenden makecert.exe, um ein Zertifikat zu generieren oder einen Signaturschlüssel von einer der kommerziellen Zertifizierungsstellen (ZS) wie VeriSign, Thawte oder einer Microsoft-Zertifizierungsstelle zu erhalten.
-   Ausnahmen und Ausnahmen
    -   Nicht signierte Verteilbare Drittanbieter werden nur in Betracht gezogen. Ein Kommunikationsnachweis, der eine signierte Version der Verteilbaren an fordert, ist erforderlich, damit dieser Antrag gewährt wird.
    -   Softwarepakete mit Gerätewert sind von der Kernelmodus-Treiberzertifizierung ausgenommen, da Treiber durch die Windows zertifiziert werden müssen.

## <a name="support-x64-windows-test"></a>Support x64 Windows test

Testen Sie die App, um sicherzustellen, .exe die Plattformarchitektur erstellt wurde, auf der sie installiert wird.

-   Hintergrund
    -   Die ausführbare Datei muss für die Prozessorarchitektur erstellt werden, auf der sie installiert ist. Einige ausführbare Dateien können auf einer anderen Prozessorarchitektur ausgeführt werden, aber dies ist nicht zuverlässig.
    -   Die Architekturkompatibilität ist wichtig, da 32-Bit-Prozesse keine 64-Bit-DLLs laden können und 64-Bit-Prozesse keine 32-Bit-DLLs laden können. Ebenso unterstützen 64-Bit-Versionen von Windows das Ausführen von Windows-basierten 16-Bit-Anwendungen nicht, da Handles 32 signifikante Bits auf 64-Bit-Windows haben, sodass sie nicht an 16-Bit-Anwendungen übergeben werden können. Daher ist der Versuch, eine 16-Bit-Anwendung zu starten, bei 64-Bit-Versionen von Windows.
    -   32-Bit-Gerätetreiber können nicht in 64-Bit-Versionen von Windows ausgeführt werden und müssen daher in die 64-Bit-Architektur portiert werden.
    -   Für Anwendungen im Benutzermodus enthält die 64-Bit-Windows WOW64, wodurch 32-Bit-Windows-Anwendungen auf Systemen ausgeführt werden können, auf denen 64-Bit-Windows ausgeführt wird. Dies ist jedoch mit leistungseinbußen. Für Gerätetreiber ist keine entsprechende Übersetzungsebene vorhanden.
    -   Um die Kompatibilität mit 64-Bit-Versionen von Windows zu gewährleisten, müssen Apps nativ 64-Bit- oder mindestens 32-Bit-Windows-basierte Apps nahtlos auf 64-Bit-Systemen unterstützen:
        -   Apps und ihre Installationsprogramme dürfen keinen 16-Bit-Code enthalten oder 16-Bit-Komponenten verwenden.
        -   Das App-Setup muss die richtigen Treiber und Komponenten in 64-Bit-Versionen von Windows.
        -   Alle Shell-Plug-Ins müssen auf 64-Bit-Versionen von Windows.
        -   Apps, die unter dem WoW64-Emulator ausgeführt werden, sollten nicht versuchen, Wow64-Virtualisierungsmechanismen zu umgehen. Wenn es bestimmte Szenarien gibt, in denen Apps erkennen müssen, ob sie in einem WoW64-Emulator ausgeführt werden, sollten sie dies durch Aufrufen von [**IsWow64Process tun.**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   Testdetails
    -   Die App sollte keine 16-Bit-Binärdateien installieren. Die App sollte keinen 32-Bit-Kernelmodustreiber installieren, wenn er auf einem 64-Bit-Computer ausgeführt werden soll.
-   Korrekturmaßnahmen
    -   Erstellen Sie die ausführbaren Dateien und Treiber für die Prozessorarchitektur, für die Sie sie installieren möchten.

## <a name="os-version-checking-test"></a>Test zur Überprüfung der Betriebssystemversion

Testet, wie die App überprüft, ob die Version Windows, auf der sie ausgeführt wird.

-   Hintergrund
    -   Apps überprüfen die Betriebssystemversion, indem sie eine Version testen, die größer oder gleich der erforderlichen Version ist, um die Kompatibilität mit zukünftigen Versionen von Windows.
-   Testdetails
    -   Simuliert die Ausführung der App in verschiedenen Versionen von Windows, um zu sehen, wie sie reagiert.
-   Maßnahmen
    -   Testen Sie die richtige Version von Windows, indem Sie testen, ob die aktuelle Version größer oder gleich der Version ist, die Ihre App, Ihr Dienst oder Ihr Treiber benötigt.
    -   Treiberinstallations- und Deinstallationsmodule dürfen niemals die Betriebssystemversion überprüfen.
-   Ausnahmen und Ausnahmen
    -   Ausnahmen werden für Apps berücksichtigt, die die folgenden Kriterien erfüllen: (Gilt nur für die *Zertifizierung von Desktop-Apps)*
        -   Apps, die als ein Paket bereitgestellt werden, das unter Windows XP, Windows Vista und Windows 7 ausgeführt wird und die Betriebssystemversion überprüfen müssen, um zu bestimmen, welche Komponenten unter einem bestimmten Betriebssystem installiert werden sollen.
        -   Apps, die nur die Mindestversion des Betriebssystems überprüfen (nur während der Installation, nicht zur Laufzeit), indem sie nur die genehmigten API-Aufrufe verwenden und die Mindestversionsanforderung im App-Manifest nach Bedarf auflisten.
        -   Sicherheits-Apps wie Antiviren- und Firewall-Apps, Systemprogramme wie Defragmentierungs-Hilfsprogramme und Sicherungs-Apps sowie Diagnosetools, die die Betriebssystemversion nur mithilfe der genehmigten API-Aufrufe überprüfen.

## <a name="user-account-control-uac-test"></a>Test der Benutzerkontensteuerung (User Account Control, UAC)

Testet die App, um sicherzustellen, dass für die Ausführung keine unnötig erhöhten Berechtigungen erforderlich sind.

-   Hintergrund
    -   Eine App, die nur ausgeführt oder installiert wird, wenn der Benutzer Administrator ist, zwingt Benutzer, die App mit unnötig erhöhten Berechtigungen ausführen, wodurch Schadsoftware in den Computer des Benutzers gelangen kann.
    -   Wenn Benutzer immer gezwungen sind, Apps mit Erhöhten Zugriffstoken ausführen zu müssen, kann die App als Einstiegspunkt für schädlichen oder schädlichen Code serveren. Diese Schadsoftware kann das Betriebssystem leicht ändern oder sich noch schlechter auf andere Benutzer auswirken. Es ist fast unmöglich, einen Benutzer zu steuern, der vollzugriff auf den Administrator hat, da Administratoren Apps installieren und alle Apps oder Skripts auf dem Computer ausführen können. IT-Manager suchen immer nach Möglichkeiten, "Standarddesktops" zu erstellen, bei denen sich Benutzer als Standardbenutzer anmelden. Standarddesktops senken die Helpdeskkosten deutlich und reduzieren den IT-Aufwand.
    -   Die meisten Anwendungen erfordern zur Laufzeit keine Administratorrechte. Ein Standardbenutzerkonto sollte in der Lage sein, sie ausführen zu können. Windows-Apps müssen über ein Manifest (eingebettet oder extern) verfügen, um die Ausführungsebene zu definieren, mit der das Betriebssystem über die Berechtigungen informiert wird, die zum Ausführen der App erforderlich sind. Das App-Manifest gilt nur für .exe Dateien, nicht für .dll Dateien. Die Benutzerkontensteuerung (User Account Control, UAC) überprüft dlLs während der Erstellung des Prozesses nicht. UAC-Regeln gelten nicht für Microsoft-Dienste. Das App-Manifest kann eingebettet oder extern sein.
    -   Um ein Manifest zu erstellen, erstellen Sie eine Datei mit dem Namen <App-Namen>.exe.manifest, und speichern Sie sie im gleichen Verzeichnis \_ wie die EXE. Beachten Sie, dass jedes externe Manifest ignoriert wird, wenn die App über ein internes Manifest verfügt.
        -   Beispiel: <requestedExecutionLevel level=""asInvoker \| highestAvailable \| requireAdministrator"" uiAccess=""true \| false""/>
        -   Der Hauptprozess der App muss als Standardbenutzer **(asInvoker) ausgeführt werden.** Alle administrativen Funktionen müssen in einen separaten Prozess verschoben werden, der mit Administratorrechten ausgeführt wird.
        -   Für Benutzer bestimmte Apps, die erhöhte Berechtigungen erfordern, müssen mit Authenticode signiert sein.
-   Testdetails
    -   Alle exe-Dateien für Benutzer sollten mit dem Attribut asInvoker gekennzeichnet werden. Wenn sie als highestAvailable oder requireAdministrator gekennzeichnet sind, sollten sie ordnungsgemäß authenticode signed sein. Für jede App-EXE-Datei sollte das uiAccess-Attribut nicht auf TRUE festgelegt sein. Alle EXE-Dateien, die als Dienst ausgeführt werden, werden von dieser speziellen Überprüfung ausgeschlossen.
-   Maßnahmen
    -   Überprüfen Sie die Manifestdatei der App auf die richtigen Einträge und Berechtigungsstufen.
-   Ausnahmen und Ausnahmen
    -   Eine Ausnahme ist für Apps erforderlich, die ihren Hauptprozess mit erhöhten Rechten ausführen **(requireAdministrator** oder **highestAvailable**). Der Hauptprozess ist der Prozess, der den Einstiegspunkt des Benutzers für die App bietet.
    -   Ausnahmen werden für die folgenden Szenarien berücksichtigt:
        -   Verwaltungs- oder Systemtools, bei denen die Ausführungsebene **auf highestAvailable**, **requireAdministrator** oder beides festgelegt ist.
        -   Nur die Framework-App für Barrierefreiheit oder Benutzeroberflächenautomatisierung legt das uiAccess-Flag auf TRUE fest, um die Benutzeroberflächen-Berechtigungsisolation (UIPI) zu umgehen. Um die App-Auslastung ordnungsgemäß zu starten, muss dieses Flag authenticode signiert sein und sich an einem geschützten Speicherort im Dateisystem befinden, z. B. Programme.

## <a name="adhere-to-system-restart-manager-messages"></a>Befolgen von Systemneustart-Manager-Meldungen

Testet, wie die App auf Meldungen zum Herunterfahren und Neustarten des Systems reagiert.

-   Hintergrund
    -   Apps müssen so schnell wie möglich beendet werden, wenn sie benachrichtigt werden, dass das System heruntergefahren wird, um dem Benutzer ein reaktionsfähiges Herunterfahren oder Ausschalten zu ermöglichen.
    -   Bei einem kritischen Herunterfahren werden Apps, die FALSE an [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) zurückgeben, an **WM \_ ENDSESSION** gesendet und geschlossen, während diejenigen, für die als Reaktion auf WM QUERYENDSESSION ein Time out erfolgt, gesperrt \_ werden.
-   Testdetails
    -   Untersucht, wie die App auf das Herunterfahren und Beenden von Nachrichten reagiert.
-   Maßnahmen
    -   Wenn Ihre App diesen Test nicht bestanden hat, überprüfen Sie, wie sie diese Windows behandelt:
        -   [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) mit *LPARAM*  =  **ENDSESSION \_ CLOSEAPP**(0x1): Desktop-Apps müssen sofort reagieren (TRUE) als Vorbereitung auf einen Neustart. Konsolen-Apps können [**SetConsoleCtrlHandler aufrufen,**](/windows/console/setconsolectrlhandler) um Benachrichtigungen zum Herunterfahren zu erhalten. Dienste können [**RegisterServiceCtrlHandlerEx aufrufen,**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) um Benachrichtigungen zum Herunterfahren in einer Handlerroutine zu empfangen.
        -   [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) mit *LPARAM*  =  **ENDSESSION \_ CLOSEAPP**(0x1): Apps müssen innerhalb von 30 Sekunden einen Wert von 0 zurückgeben und herunterfahren. Apps sollten sich mindestens vorbereiten, indem sie alle Benutzerdaten speichern und die Informationen, die nach einem Neustart benötigt werden, zustandsbereit machen.
    -   Konsolen-Apps, die die **\_ STRG-C-EREIGNISbenachrichtigung \_** erhalten, sollten sofort heruntergefahren werden. Treiber dürfen kein Systemabschaltungsereignis verursachen.
    -   **Hinweis:** Apps, die das Herunterfahren aufgrund eines Vorgangs blockieren müssen, der nicht unterbrochen werden kann, sollten [**ShutdownBlockReasonCreate**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasoncreate) verwenden, um eine Zeichenfolge zu registrieren, die den Grund für den Benutzer erklärt. Wenn der Vorgang abgeschlossen ist, sollte die App [**ShutdownBlockReasonDestroy**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasondestroy) aufrufen, um anzugeben, dass das System heruntergefahren werden kann.

## <a name="safe-mode-test"></a>Tresor Modustest

Testet, ob der Treiber oder Dienst für den Start im abgesicherten Modus konfiguriert ist.

-   Hintergrund
    -   Tresor-Modus ermöglicht Benutzern das Diagnostizieren und Behandeln von Problemen mit Windows. Nur Treiber und Dienste, die für den grundlegenden Betrieb des Betriebssystems erforderlich sind oder Diagnose- und Wiederherstellungsdienste bereitstellen, sollten im abgesicherten Modus geladen werden. Das Laden anderer Dateien im abgesicherten Modus erschwert die Behandlung von Problemen mit dem Betriebssystem.
    -   Standardmäßig werden nur die Treiber und Dienste, die mit vorinstalliert sind, Windows im abgesicherten Modus gestartet. Alle anderen Treiber und Dienste sollten deaktiviert werden, es sei denn, das System erfordert sie für grundlegende Vorgänge oder für Diagnose- und Wiederherstellungszwecke.
-   Testdetails
    -   Von der App installierte Treiber sollten nicht für das Laden im abgesicherten Modus gekennzeichnet werden.
-   Maßnahmen
    -   Wenn der Treiber oder Dienst nicht im abgesicherten Modus gestartet werden soll, entfernen Sie die Einträge der App aus den Registrierungsschlüsseln.
-   Ausnahmen und Ausnahmen
    -   Treiber und Dienste, die im abgesicherten Modus gestartet werden müssen, erfordern eine Zertifizierung. Die Anforderung für den Antrag auf Unterstützung muss jeden Treiber und Dienst enthalten, der den SafeBoot-Registrierungsschlüsseln hinzugefügt werden soll, und die technischen Gründe dafür beschreiben, warum der Treiber oder Dienst im abgesicherten Modus ausgeführt werden muss. Das App-Installationsprogramm muss alle diese Treiber und Dienste in diesen Registrierungsschlüsseln registrieren:
        -   HKLM/System/CurrentControlSet/Control/SafeBoot/Minimal
        -   HKLM/System/CurrentControlSet/Control/SafeBoot/Network
-   **Hinweis:** Sie müssen die Treiber und Dienste testen, die sie im abgesicherten Modus starten möchten, um sicherzustellen, dass sie fehlerfrei im abgesicherten Modus funktionieren.

## <a name="multiuser-session-test"></a>Multiuser-Sitzungstest

Testen Sie, wie sich die App verhält, wenn sie gleichzeitig in mehreren Sitzungen ausgeführt wird.

-   Hintergrund
    -   Windows Benutzer müssen gleichzeitige Sitzungen ausführen können. Apps müssen sicherstellen, dass die normale Funktionalität der App nicht beeinträchtigt wird, wenn sie lokal oder remote in mehreren Sitzungen ausgeführt werden. App-Einstellungen und Datendateien müssen benutzerspezifisch sein, und der Datenschutz und die Einstellungen des Benutzers müssen auf die Sitzung des Benutzers beschränkt sein.
-   Testdetails
    -   Führt mehrere gleichzeitige Instanzen der App aus, um Folgendes zu testen:
        -   Mehrere Instanzen einer App, die gleichzeitig ausgeführt werden, sind voneinander isoliert.
    -   Dies bedeutet, dass Benutzerdaten aus einer Instanz für eine andere Instanz nicht sichtbar sind. Sound in einer inaktiven Benutzersitzung sollte in einer aktiven Benutzersitzung nicht gehört werden. In Fällen, in denen mehrere App-Instanzen freigegebene Ressourcen verwenden, muss die App sicherstellen, dass es keinen Konflikt gibt.
        -   Wenn die App für mehrere Benutzer installiert wurde, speichert sie Daten in den richtigen Ordnern und Registrierungsspeicherorten.
        -   Die App kann in mehreren Benutzersitzungen (schneller Benutzerwechsel) sowohl für den lokalen als auch für den Remotezugriff ausgeführt werden.
    -   Um dies sicherzustellen, muss die App andere Terminaldienstsitzungen auf vorhandene Instanzen der App überprüfen. Wenn die App nicht mehrere Benutzersitzungen oder den Remotezugriff unterstützt, muss sie dies dem Benutzer klar sagen, wenn sie über eine solche Sitzung gestartet wird.
-   Korrekturmaßnahme
    -   Stellen Sie sicher, dass die App keine systemweiten Datendateien oder -einstellungen in benutzerspezifischen Datenspeichern wie Benutzerprofil oder HKCU speichert. Wenn dies der Derkung ist, sind diese Informationen für andere Benutzer nicht verfügbar.
    -   Ihre App muss während der Installation systemweite Konfigurations- und Datendateien installieren und die benutzerspezifischen Dateien und Einstellungen nach der Installation erstellen, wenn ein Benutzer sie ausgeführt.
    -   Stellen Sie sicher, dass die App nicht mehrere gleichzeitige Sitzungen blockiert, weder lokal noch remote. Die App darf nicht von globalen Mutexen oder anderen benannten Objekten abhängig sein, um mehrere gleichzeitige Sitzungen zu überprüfen oder zu blockieren.
    -   Wenn die App nicht mehrere gleichzeitige Sitzungen pro Benutzer zulassen kann, verwenden Sie Namespaces pro Benutzer oder pro Sitzung für Mutexe und andere benannte Objekte.

## <a name="crashes-and-hangs-test"></a>Abstürze und Hängen – Test

Überwachen die App während des Zertifizierungstests, um aufzuzeichnen, wann sie abstürzt oder sich aufhängt.

-   Hintergrund
    -   App-Ausfälle wie Abstürze und Hängen stellen eine erhebliche Störung für Benutzer und sorgen für Frust. Die Beseitigung solcher Fehler verbessert die Stabilität und Zuverlässigkeit der App und bietet Benutzern insgesamt eine bessere App-Erfahrung. Apps, die nicht mehr reagieren oder abstürzen, können zu einem Datenverlust und zu einer Beeinträchtigung des Benutzererlebnisses führen.
-   Testdetails
    -   Die App wird beim Zertifizierungstest durchgehend auf Flexibilität und Stabilität geprüft.
    -   Das Windows App Certification Kit ruft [**IApplicationActivationManager::ActivateApplication**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication) auf, um Windows Store zu starten. Damit eine App mit **ActivateApplication** gestartet werden kann, muss die Benutzerkontensteuerung (UAC) aktiviert sein und die Bildschirmauflösung mindestens 1024 x 768 oder 768 x 1024 betragen. Ist eine dieser Bedingungen nicht erfüllt, fällt die App bei diesem Test durch.
-   Korrekturmaßnahmen
    -   Stellen Sie sicher, dass die Benutzerkontensteuerung (UAC) auf dem Test-PC aktiviert ist.
    -   Führen Sie den Test auf einem PC mit ausreichend großem Bildschirm aus.
    -   Falls die App nicht gestartet werden kann, obwohl die Testplattform die Voraussetzungen für [**ActivateApplication**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication) erfüllt, können Sie das Problem mithilfe des Aktivierungsereignisprotokolls beheben. So finden Sie die Einträge im Ereignisprotokoll:
        1.  Öffnen eventvwr.exe, und navigieren Sie zum Knoten \\ Windows \\ Protokollanwendung.
        2.  Filtern Sie die Ansicht entsprechend, um folgende Ereigniskennungen anzuzeigen: 5900-6000.
        3.  Prüfen Sie die Protokolleinträge, um zu ermitteln, weshalb die App nicht gestartet wurde.
    -   Führen Sie für die Datei mit dem Problem eine Problembehandlung durch, um das Problem zu identifizieren und zu beheben. Erstellen Sie die App neu, und wiederholen Sie den Test.
-   Zusätzliche Ressourcen
    -   [Verwenden Application Verifier in Ihrem Softwareentwicklungslebenszyklus](https://blogs.msdn.com/b/ntdebugging/archive/2014/01/13/debugging-a-windows-8-1-store-app-crash-dump.aspx)
    -   [Application Verifier]( https://go.microsoft.com/fwlink/p/?LinkId=708300)
    -   [Verwenden Application Verifier](https://www.microsoft.com/?ref=go)
    -   [AppInit-DLLs](https://www.microsoft.com/?ref=go)
    -   [Minimieren der Startzeit (Windows Store-Apps mit C#/VB/C++ und XAML)](/previous-versions/windows/apps/hh994639(v=win.10))

## <a name="compatibility-and-resiliency-test"></a>Kompatibilitäts- und Resilienztest

-   Hintergrund
    -   Bei dieser Überprüfung werden zwei Aspekte einer App überprüft: Die ausführbaren Hauptdateidateien der App, z. B. der Einstiegspunkt für die Benutzer-App, müssen aus Kompatibilitäts- und Deklarationsaspekten der richtigen GUID manifestiert werden. Zur Unterstützung dieses neuen Tests enthält der Bericht einen Unterknoten unter "Kompatibilität & Resilienz". Die App kann nicht verwendet werden, wenn eine oder beide dieser Bedingungen fehlen.
-   Testdetails
    -   **Kompatibilität:** Apps müssen voll funktionsfähig sein, ohne Windows Kompatibilitätsmodi, AppHelp-Meldungen oder andere Kompatibilitätskorrekturen zu verwenden. Ein Kompatibilitätsmanifest ermöglicht Windows, Ihrer App das richtige Kompatibilitätsverhalten unter den verschiedenen Versionen des Betriebssystems zur Verfügung zu stellen.
    -   **AppInit:** Apps dürfen keine DLLs auflisten, die in der HKEY LOCAL MACHINE Software Microsoft Windows NT CurrentVersion Windows \_ \_ \\ \\ \\ \\ \\ \\ AppInit \_ DLLs-Registrierungsschlüssel geladen werden sollen.
    -   **Switchback:** Die Anwendung muss das Switchbackmanifest bereitstellen. Wenn das Manifest fehlt, wird Windows App Certification Kit eine Warnmeldung angezeigt. Windows Das App Certification Kit überprüft außerdem, ob das Manifest eine gültige Betriebssystem-GUID enthält.
-   Maßnahmen
    -   Korrigieren Sie die Komponente der App, die den Kompatibilitätsfix verwendet.
    -   Stellen Sie sicher, dass die App nicht auf Kompatibilitätskorrekturen für ihre Funktionalität angewiesen ist.
    -   Stellen Sie sicher, dass Ihre App manifestiert ist und der Kompatibilitätsabschnitt die entsprechenden Werte enthält.
-   Zusätzliche Informationen
    -   Weitere Informationen finden Sie unter [AppInit-DLLs.](/previous-versions/windows/apps/hh994639(v=win.10))

## <a name="windows-security-best-practices-test"></a>Windows-Sicherheit bewährten Methoden – Test

-   Hintergrund
    -   Eine App sollte die Standardsicherheitseinstellungen nicht Windows ändern.
-   Testdetails
    -   Testet die Sicherheit der App, indem das Attack Surface Analyzer ausgeführt wird. Der Ansatz ist das Hinzufügen von Fehlerkategorien pro Test. Einige Kategorien für Sicherheitstests können beispielsweise Folgendes umfassen:
        -   Initialisierungsfehler
        -   Fehler bei der Sicherheitsarchitektur
        -   Möglicher Pufferüberlauffehler
        -   Absturzfehler
    -   Weitere Informationen finden Sie [hier.](/previous-versions/windows/hh920280(v=win.10))
-   Maßnahmen
    -   Beheben Sie das von den Tests identifizierte Problem, und beheben Sie es. Erstellen Sie die App neu, und wiederholen Sie den Test.

## <a name="windows-security-features-test"></a>Windows von Sicherheitsfeatures

-   Hintergrund
    -   Anwendungen müssen sich für Windows Sicherheitsfeatures entscheiden. Durch Ändern der standardmäßigen Windows-Sicherheitsvorkehrungen können Kunden einem erhöhten Risiko ausgesetzt werden.
-   Testdetails
    -   Testet die Sicherheit der App durch Ausführen des BinScope Binary Analyzers. Weitere Informationen finden Sie [hier.](/previous-versions/windows/hh920280(v=win.10))
-   Maßnahmen
    -   Behandeln und Beheben des von den Tests identifizierten Problems. Erstellen Sie die App neu, und wiederholen Sie den Test.

## <a name="high-dpi-test"></a>Hoher DPI-Test

Es wird dringend empfohlen, dass die Win32-Apps DPI-bewusst sind. Dies ist der Schlüssel, damit die Benutzeroberfläche der App in einer Vielzahl von Anzeigeeinstellungen mit hohem DPI-Wert konsistent gut aussieht. Bei einer Nicht-DPI-fähigen App, die auf einer Anzeigeeinstellung mit hohem DPI-Wert ausgeführt wird, können Probleme auftreten, z. B. eine falsche Skalierung von Benutzeroberflächenelementen, abgeschnittener Text und unscharfe Bilder. Es gibt zwei Möglichkeiten, eine App als DPI-fähige App zu deklarieren. Eine davon ist das Deklarieren von DPI.

-   Hintergrund
    -   Bei dieser Überprüfung werden zwei Aspekte einer App überprüft: Die wichtigsten ausführbaren Dateien, z. B. Benutzerseitige App-Einstiegspunkte, müssen für HIGH-DPI-Bekanntheit manifestiert werden und dass die richtigen APIs aufgerufen werden, um HIGH-DPI zu unterstützen. Die App schlägt fehl, wenn eine oder beide dieser Bedingungen fehlen. Diese Überprüfung führt einen neuen Abschnitt im Desktopbericht ein, siehe Beispiel unten.
-   Testdetails
    -   Der Test generiert eine Warnung, wenn eine der folgenden Erkannt wird:
        -   Die Haupt-EXE deklariert keine DPI-Wahrnehmung in ihrem Manifest und ruft keine SetProcessDPIAware-API auf. (Warnen Sie den Entwickler, wenn er vergessen hat, ein DPI-Bekanntheitsmanifest hinzuzufügen.)
        -   Die Haupt-EXE deklariert keine DPI-Bekanntheit in ihrem Manifest, aber sie ruft die SetProcessDPIAware-API auf (Warnen Sie den Entwickler, dass er das Manifest verwenden soll, um die DPI-Bekanntheit zu deklarieren, anstatt die API aufzurufen).
        -   MainEXE deklariert die DPI-Bekanntheit in seinem Manifest, ruft aber auch die SetProcessDPIAware-API auf (Warnen Sie den Entwickler, dass der Aufruf dieser API nicht erforderlich ist).
        -   Geben Sie für die Binärdateien, bei denen es sich nicht um Haupt-EXEs handelt, eine Warnung aus (Das Aufrufen der API wird nicht empfohlen), wenn sie die API aufrufen.
-   Maßnahmen
    -   Von der Verwendung der SetProcessDPIAware()-Funktion wird abgeraten. Wenn eine DLL während der Initialisierung DPI-Einstellungen zwischenspeichert, generiert das Aufrufen von SetProcessDPIAware() in der App möglicherweise eine Racebedingung. Das Aufrufen der SetProcessDPIAware()-Funktion in einer DLL ist auch keine bewährte Methode.
-   Zusätzliche Informationen
    -   [Schreiben von Apps mit hohem DPI-Anteil](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))

 

 