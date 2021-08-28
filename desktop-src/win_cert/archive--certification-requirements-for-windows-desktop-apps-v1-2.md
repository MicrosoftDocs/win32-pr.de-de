---
title: Archivzertifizierungsanforderungen für Windows Desktop-Apps v1.2
description: Dokumentversion 1.2Dokumentdatum 31. Mai 2012 Dieses Dokument enthält die technischen Anforderungen und Qualifikationsvoraussetzungen, die eine Desktop-App erfüllen muss, um am Zertifizierungsprogramm für Windows 8 Desktop-App teilzunehmen.
ms.assetid: A65D7FE9-554B-4D59-91B7-E1582F7C6C87
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a2a6aecc46c091e44463b74870807873f73053f7
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882667"
---
# <a name="archive-certification-requirements-for-windows-desktop-apps-v12"></a>Archiv: Zertifizierungsanforderungen für Windows Desktop-Apps v1.2

**Dokumentversion:** 1.2

**Dokumentdatum:** 31. Mai 2012

Dieses Dokument enthält die technischen Anforderungen und Qualifikationsqualifikationen, die eine Desktop-App erfüllen muss, um am Windows 8 Desktop-App-Zertifizierungsprogramm teilnehmen zu können. Für Windows 7 wurde dieses Programm als Windows Softwarelogo-Programm bezeichnet.

## <a name="welcome"></a>Willkommen!

Die Windows-Plattform unterstützt ein breites Ökosystem von Produkten und Partnern. Das Anzeigen des Windows-Logos in Ihrem Produkt stellt eine Beziehung und eine gemeinsame Verpflichtung zur Qualität zwischen Microsoft und Ihrem Unternehmen dar. Kunden vertrauen der Windows Marke auf Ihr Produkt, da sie sicherstellt, dass sie Kompatibilitätsstandards erfüllt und auf der Windows-Plattform gut funktioniert. Wenn Sie Windows App-Zertifizierung erfolgreich bestanden haben, kann Ihre App im Windows Compatibility Center vorgestellt werden, und es ist auch ein notwendiger Schritt zum Auflisten eines Desktop-App-Verweises im Windows Store.

Das Windows App Certification Program setzt sich aus Programm- und technischen Anforderungen zusammen, um sicherzustellen, dass Drittanbieter-Apps, die die marke Windows tragen, auf PCs, auf denen Windows ausgeführt wird, einfach zu installieren und zuverlässig sind. Kunden legen Wert auf Stabilität, Kompatibilität, Zuverlässigkeit, Leistung und Qualität in den systemen, die sie erwerben. Microsoft konzentriert sich auf seine Investitionen, um diese Anforderungen für Software-Apps zu erfüllen, die auf der Windows-Plattform für PCs ausgeführt werden sollen. Diese Bemühungen umfassen Kompatibilitätstests auf Konsistenz der Benutzererfahrung, verbesserte Leistung und erhöhte Sicherheit auf PCs, auf denen Windows Software ausgeführt wird. Microsoft-Kompatibilitätstests wurden in Zusammenarbeit mit Branchenpartnern entwickelt und als Reaktion auf Branchenentwicklungen und Verbrauchernachfrage kontinuierlich verbessert.

Das Windows App Certification Kit wird verwendet, um die Konformität mit diesen Anforderungen zu überprüfen, und ersetzt den WSLK, der für die Validierung im softwarelogo-Programm Windows 7 verwendet wird. Das Windows App Certification Kit ist eine der Komponenten, die im Windows Software Development Kit (SDK) enthalten sind.

## <a name="app-eligibility"></a>App-Berechtigung

Damit eine App für Windows 8 Desktop-App-Zertifizierung qualifiziert werden kann, muss sie die folgenden Kriterien und alle technischen Anforderungen erfüllen, die in diesem Dokument aufgeführt sind.

-   Es muss sich um eine eigenständige App
-   Er muss auf einem lokalen Windows 8.1 Computer ausgeführt werden.
-   Dies kann eine Clientkomponente einer zertifizierten Windows Server-App sein.
-   Es muss Code und Feature vollständig sein.

## <a name="1-apps-are-compatible-and-resilient"></a>1. Apps sind kompatibel und resilient

Die Zeiten, in denen eine App abstürzt oder nicht mehr reagiert, führen zu einer großen Benutzerverärkung. Es wird erwartet, dass Apps resilient und stabil sind, und die Beseitigung solcher Fehler trägt dazu bei, sicherzustellen, dass Software besser vorhersagbar, wartbar, leistungsfähig und vertrauenswürdig ist.<dl> 1.1 Ihre App darf keine Abhängigkeit von Windows Kompatibilitätsmodi, AppHelp-Nachricht und oder anderen Kompatibilitätskorrekturen annehmen.  
1.2 Ihre App darf keine Abhängigkeit von der VB6-Runtime annehmen.  
1.3 Ihre App darf keine beliebigen DLLs laden, um Win32-API-Aufrufe mit hklm \\ software Microsoft Windows NT \\ \\ \\ CurrentVersion Windows \\ AppInit-DLLs \_ abzufangen.  
</dl>

## <a name="2-apps-must-adhere-to-windows-security-best-practices"></a>2. Apps müssen Windows bewährten Sicherheitsmethoden entsprechen.

Die Verwendung Windows bewährten Sicherheitsmethoden trägt dazu bei, die Gefährdung durch Windows Angriffsflächen zu vermeiden. Angriffsflächen sind die Einstiegspunkte, die ein böswilliger Angreifer verwenden kann, um das Betriebssystem auszunutzen, indem er Sicherheitsrisiken in der Zielsoftware nutzt. Eines der schlechtesten Sicherheitsrisiken ist die Rechteerweiterung.

<dl> 2.1 Ihre App muss starke und geeignete <a href="/windows/desktop/SecAuthZ/access-control-lists">ACLs</a> verwenden, um ausführbare Dateien zu schützen.  
2.2 Ihre App muss starke und geeignete <a href="/windows/desktop/SecAuthZ/access-control-lists">ACLs</a> verwenden, um Verzeichnisse zu schützen.  
2.3 Ihre App muss starke und geeignete <a href="/windows/desktop/SecAuthZ/access-control-lists">ACLs</a> verwenden, um Registrierungsschlüssel zu schützen.  
2.4 Ihre App muss starke und geeignete <a href="/windows/desktop/SecAuthZ/access-control-lists">ACLs</a> verwenden, um Verzeichnisse zu schützen, die Objekte enthalten.  
2.5 Ihre App muss den Nichtadministratorzugriff auf Dienste reduzieren, die anfällig für Manipulationen sind.  
2.6 Ihre App muss verhindern, dass Dienste mit schnellen Neustarts mehr als zweimal alle 24 Stunden neu gestartet werden.
</dl>**Hinweis: Zugriff sollte nur den Entitäten gewährt werden, die ihn benötigen.**

Das Windows App-Zertifizierungsprogramm überprüft, ob Windows Angriffsoberflächen nicht verfügbar gemacht werden, indem überprüft wird, ob ACLs und Dienste auf eine Weise implementiert werden, die das Windows System nicht gefährdet.

## <a name="3-apps-support-windows-security-features"></a>3. Apps unterstützen Windows Sicherheitsfeatures

Das Windows Betriebssystem verfügt über viele Features, die die Systemsicherheit und den Datenschutz unterstützen. Apps müssen diese Features unterstützen, um die Integrität des Betriebssystems aufrechtzuerhalten. Falsch kompilierte Apps können Pufferüberläufe verursachen, die wiederum Denial-of-Service-Angriffe verursachen oder die Ausführung von schädlichem Code zulassen. <dl> 3.1 Ihre App darf allowPartiallyTrustedCallersAttribute (APTCA) nicht verwenden, um den sicheren Zugriff auf Assemblys mit starkem Namen sicherzustellen.  
3.2 Ihre App muss mit dem /SafeSEH-Flag kompiliert werden, um die Behandlung sicherer Ausnahmen sicherzustellen.  
3.3 Ihre App muss mit dem /NXCOMPAT-Flag kompiliert werden, um die Datenausführung zu verhindern.  
3.4 Ihre App muss mit dem /DYNAMICBASE-Flag für die Zufälligisierung des Adressraumlayouts (Address Space Layout Randomization, ASLR) kompiliert werden.  
3.5 Ihre App darf die freigegebenen PE-Abschnitte nicht lesen/schreiben  
</dl>

## <a name="4-apps-must-adhere-to-system-restart-manager-messages"></a>4. Apps müssen Den Meldungen des Systemneustart-Managers entsprechen.

Wenn Benutzer das Herunterfahren initiieren, möchten sie in der Regel, dass das Herunterfahren erfolgreich ist. sie sind möglicherweise in der Lage, das Büro zu verlassen, und möchten nur, dass ihre Computer ausgeschaltet werden. Apps müssen diesen Wunsch berücksichtigen, indem sie das Herunterfahren nicht blockieren. In den meisten Fällen ist das Herunterfahren möglicherweise nicht kritisch, Apps müssen jedoch auf die Möglichkeit eines kritischen Herunterfahrens vorbereitet werden.<dl> 4.1 Ihre App muss kritisches Herunterfahren entsprechend behandeln. <dl> Bei einem kritischen Herunterfahren werden Apps, die FALSE an WM \_ QUERYENDSESSION zurückgeben, WM ENDSESSION gesendet \_ und geschlossen, während apps, bei denen ein Time out als Reaktion auf WM \_ QUERYENDSESSION erfolgt, beendet werden.  
</dl> </dd> 4.2 A GUI app must return TRUE immediately in preparation for a restart <dl> WM \_ QUERYENDSESSION mit LPARAM = ENDSESSION \_ CLOSEAPP(0x1).  
Konsolen-Apps können SetConsoleCtrlHandler aufrufen, um die Funktion anzugeben, die Benachrichtigungen zum Herunterfahren verarbeitet. Dienst-Apps können RegisterServiceCtrlHandlerEx aufrufen, um die Funktion anzugeben, die Benachrichtigungen zum Herunterfahren empfängt.  
</dl> </dd> 4.3 Your app must return 0 within 30 seconds and shut down <dl> WM \_ ENDSESSION with LPARAM = ENDSESSION \_ CLOSEAPP(0x1).  
Die App sollte sich mindestens darauf vorbereiten, indem sie alle Benutzerdaten speichert und die Informationen angibt, die nach einem Neustart benötigt werden.  
</dl> </dd> 4.4 Console apps that receive the CTRL\_C\_EVENT notification should shut down immediately  
4.5 Drivers must not veto a system shutdown event  
</dl>**Note: Apps that must block shutdown because of an operation that cannot be interrupted should explain the reason to the user.** Use ShutdownBlockReasonCreate to register a string that explains the reason to the user. When the operation has completed, the app should call ShutdownBlockReasonDestroy to indicate that the system can be shut down.

## <a name="5-apps-must-support-a-clean-reversible-installation"></a>5. Apps müssen eine bereinigte, umkehrbare Installation unterstützen.

Mit einer sauberen, umkehrbaren Installation können Benutzer Apps auf ihren Systemen erfolgreich verwalten (bereitstellen und entfernen).<dl> 5.1 Ihre App muss eine saubere, umkehrbare Installation ordnungsgemäß implementieren. <dl> Wenn bei der Installation ein Fehler auftritt, sollte die App in der Lage sein, ein Rollback für den Computer und dessen vorherigen Zustand wiederherzustellen.  
</dl> </dd> 5.2 Your app must never force the user to restart the computer immediately <dl> Das Neustarten des Computers sollte nie die einzige Option am Ende einer Installation oder eines Updates sein. Benutzer sollten die Möglichkeit haben, später neu zu starten.  
</dl> </dd> 5.3 Your app must never be dependent on 8.3 short file names (SFN)  
5.4 Your app must never block silent install/uninstall  
5.5 Your app installer must create the correct registry entries to allow successful detection and uninstalls <dl> Windows Inventurtools und Telemetrietools benötigen vollständige Informationen zu installierten Apps. Wenn Sie ein MSI-basiertes Installationsprogramm verwenden, erstellt MSI automatisch die unten angegebenen Registrierungseinträge. Wenn Sie kein MSI-Installationsprogramm verwenden, muss das Installationsmodul während der Installation die folgenden Registrierungseinträge erstellen:  
</dl>

-   DisplayName
-   InstallLocation
-   Publisher
-   UninstallString
-   VersionMajor oder MajorVersion
-   VersionMinor oder MinorVersion

</dd> </dl>

## <a name="6-apps-must-digitally-sign-files-and-drivers"></a>6. Apps müssen Dateien und Treiber digital signieren.

Mit einer digitalen Authenticode-Signatur können Benutzer sicherstellen, dass die Software echt ist. Außerdem kann erkannt werden, ob eine Datei manipuliert wurde, z. B. ob sie von einem Virus infiziert wurde. Die Erzwingung der Kernelmodus-Codesignatur ist ein Windows Feature, das als Codeintegrität (Code Integrity, CI) bezeichnet wird und die Sicherheit des Betriebssystems verbessert, indem jedes Mal, wenn das Image der Datei in den Arbeitsspeicher geladen wird, die Integrität einer Datei überprüft wird. CI erkennt, ob schädlicher Code eine Systembinärdatei geändert hat. Generiert auch ein Diagnose- und Systemüberwachungsprotokollereignis, wenn die Signatur eines Kernelmoduls nicht ordnungsgemäß überprüft werden kann. <dl> 6.1 Alle ausführbaren Dateien (.exe, .dll, OCX, .sys, .cpl, DRV, SCR) müssen mit einem Authenticode-Zertifikat signiert werden.  
6.2 Alle von der App installierten Kernelmodustreiber müssen über eine Microsoft-Signatur verfügen, die über das Windows Hardwarezertifizierungsprogramm abgerufen wurde. Alle Dateisystemfiltertreiber müssen von Microsoft signiert werden.  
6.3 Ausnahmen und Ausnahmen <dl> Ausnahmen werden nur für verteilbare Drittanbieter ohne Vorzeichen berücksichtigt, ausgenommen Treiber. Ein Kommunikationsnachweis, der eine signierte Version der verteilbaren (verteilbaren) Verteilbaren Anforderer anfordert, ist erforderlich, damit dieser Verzicht gewährt wird.  
</dl> </dd> </dl>

## <a name="7-apps-don-t-block-installation-or-app-launch-based-on-an-operating-system-version-check"></a>7. Apps blockieren die Installation oder den App-Start nicht basierend auf einer Versionsprüfung des Betriebssystems.

Es ist wichtig, dass Kunden nicht daran gehindert werden, ihre App zu installieren oder auszuführen, wenn es keine technischen Einschränkungen gibt. Wenn Apps für Windows Vista oder höhere Versionen von Windows geschrieben wurden, sollten sie im Allgemeinen nicht die Betriebssystemversion überprüfen müssen.<dl> 7.1 Ihre App darf keine Versionsüberprüfungen auf Gleichheit durchführen. <dl> Wenn Sie ein bestimmtes Feature benötigen, überprüfen Sie, ob das Feature selbst verfügbar ist. Wenn Sie Windows XP benötigen, suchen Sie nach Windows XP oder höher (>= 5.1). Auf diese Weise funktioniert Ihr Erkennungscode weiterhin an zukünftigen Versionen von Windows. Treiberinstallationsprogramme und Deinstallationsmodule sollten nie die Betriebssystemversion überprüfen.  
</dl> </dd> 7.2 Exceptions and Waivers will be considered for apps meeting the criteria below:

-   Apps, die als ein Paket bereitgestellt werden, das auch unter Windows XP, Windows Vista und Windows 7 ausgeführt wird, und die die Betriebssystemversion überprüfen müssen, um zu bestimmen, welche Komponenten auf einem bestimmten Betriebssystem installiert werden sollen.
-   Apps, die nur die Mindestversion des Betriebssystems überprüfen (nur während der Installation, nicht zur Laufzeit), indem sie nur die genehmigten API-Aufrufe verwenden und die Mindestversionsanforderungen im App-Manifest ordnungsgemäß auflisten.
-   Sicherheits-Apps (Antivirensoftware, Firewall usw.), Systemprogramme (z. B. Defragmentierung, Sicherungen und Diagnosetools), die die Betriebssystemversion nur mithilfe der genehmigten API-Aufrufe überprüfen.

  
</dl>

## <a name="8-apps-don-t-load-services-or-drivers-in-safe-mode"></a>8. Apps laden keine Dienste oder Treiber im abgesicherten Modus.

Tresor-Modus ermöglicht Benutzern die Diagnose und Problembehandlung Windows. Treiber und Dienste dürfen nicht so festgelegt werden, dass sie im abgesicherten Modus geladen werden, es sei denn, sie sind für grundlegende Systemvorgänge von wie Speichergerätetreiber oder für Diagnose- und Wiederherstellungszwecke wie Virenscanner erforderlich. Wenn sich Windows im abgesicherten Modus befindet, werden standardmäßig nur die Treiber und Dienste gestartet, die mit vorinstalliert Windows.

-   8.1 Ausnahmen und Ausnahmen <dl> Treiber und Dienste, die im abgesicherten Modus gestartet werden müssen, erfordern eine Ausnahme. Die Anforderung zur Aufhebung der Anforderung muss jeden anwendbaren Treiber oder Dienst enthalten, der in die SafeBoot-Registrierungsschlüssel schreibt, und die technischen Gründe beschreiben, warum die App oder der Dienst im abgesicherten Modus ausgeführt werden muss. Das App-Installationsprogramm muss alle diese Treiber und Dienste mithilfe dieser Registrierungsschlüssel registrieren:  
    </dl>
    -   HKLM/System/CurrentControlSet/Control/SafeBoot/Minimal
    -   HKLM/System/CurrentControlSet/Control/SafeBoot/Network

**Hinweis:** Sie müssen diese Treiber und Dienste testen, um sicherzustellen, dass sie fehlerfrei im abgesicherten Modus funktionieren.

## <a name="9-apps-must-follow-user-account-control-guidelines"></a>9. Apps müssen den Richtlinien für die Benutzerkontensteuerung entsprechen.

Einige Windows-Apps werden im Sicherheitskontext eines Administratorkontos ausgeführt, und Apps fordern häufig übermäßige Benutzerrechte und Windows Berechtigungen an. Durch die Steuerung des Zugriffs auf Ressourcen können Benutzer die Kontrolle über ihre Systeme haben und sie vor unerwünschten Änderungen schützen. Eine unerwünschte Änderung kann böswillig sein, z. B. ein Rootkit, das die Kontrolle über den Computer übernimmt, oder das Ergebnis einer Aktion von Personen mit eingeschränkten Berechtigungen sein. Die wichtigste Regel für die Steuerung des Zugriffs auf Ressourcen besteht in der Bereitstellung der geringsten Zugriffsmenge an Standardbenutzerkontext, die ein Benutzer zum Ausführen seiner erforderlichen Aufgaben benötigt. Die folgenden Richtlinien zur Benutzerkontensteuerung (User Account Control, UAC) bieten der App die erforderlichen Berechtigungen, wenn sie von der App benötigt werden, ohne dass das System ständig Sicherheitsrisiken ausgesetzt bleibt. Die meisten Apps erfordern zur Laufzeit keine Administratorrechte und sollten als Standardbenutzer in Ordnung sein.<dl> 9.1 Ihre App muss über ein Manifest verfügen, das Ausführungsebenen definiert und dem Betriebssystem anfordert, welche Berechtigungen die App für die Ausführung benötigt. <dl> Die App-Manifestmarkierung gilt nur für EXEs, nicht für DLLs. Dies liegt daran, dass die UAC dlLs während der Prozesserstellung nicht überprüft. Beachten Sie auch, dass UAC-Regeln nicht für Windows gelten. Das Manifest kann eingebettet oder extern sein.  
Erstellen Sie zum Erstellen eines Manifests eine Datei mit dem Namen <App-Namen>.exe.manifest, und speichern Sie sie im gleichen Verzeichnis wie \_ die EXE-Datei. Beachten Sie, dass jedes externe Manifest ignoriert wird, wenn die App über ein internes Manifest verfügt. Beispiel:  
<requestedExecutionLevel level=""asInvoker \| highestAvailable \| requireAdministrator"" uiAccess=""true \| false""/>  
</dl> </dd> 9.2 Your app s main process must be run as a standard user (asInvoker). <dl> Alle administrativen Funktionen müssen in einen separaten Prozess verschoben werden, der mit Administratorrechten ausgeführt wird. Für Benutzer zugängliche Apps, z. B. apps, auf die über die Programmgruppe im Startmenü zugegriffen werden kann und für die eine Erhöhung erforderlich ist, muss Authenticode signiert sein.  
</dl> </dd> 9.3 Exceptions and Waivers <dl> Eine Ausnahme ist für Apps erforderlich, die ihren Hauptprozess mit erhöhten Rechten ausführen (requireAdministrator oder highestAvailable). Der Hauptprozess wird als Einstiegspunkt des Benutzers für die App identifiziert. Ausnahmen werden für die folgenden Szenarien berücksichtigt:

-   Verwaltungs- oder Systemtools mit der Ausführungsebene highestAvailable und/oder requireAdministrator
-   Nur die Framework-App für Barrierefreiheit oder Benutzeroberflächenautomatisierung legt das uiAccess-Flag auf TRUE fest, um die Benutzeroberflächen-Berechtigungsisolation (UIPI) zu umgehen. Um die App-Auslastung ordnungsgemäß zu starten, muss dieses Flag authenticode signiert sein und sich an einem geschützten Speicherort im Dateisystem befinden, nämlich Programme.

  
</dl> </dd> </dl>

## <a name="10-apps-must-install-to-the-correct-folders-by-default"></a>10. Apps müssen standardmäßig in den richtigen Ordnern installiert werden.

Benutzer sollten über eine konsistente und sichere Umgebung mit dem Standardinstallationsspeicherort von Dateien verfügen und gleichzeitig die Option beibehalten, eine App am Speicherort ihrer Wahl zu installieren. Es ist auch erforderlich, App-Daten am richtigen Speicherort zu speichern, damit mehrere Personen denselben Computer verwenden können, ohne die Daten und Einstellungen des jeweils anderen zu beschädigt oder zu überschreiben. Windows stellt bestimmte Speicherorte im Dateisystem zum Speichern von Programmen und Softwarekomponenten, freigegebenen App-Daten und App-Daten für einen Benutzer zur Verfügung.<dl> 10.1 Ihre App muss standardmäßig im Ordner "Programme" installiert sein. <dl> Für native 32-Bit- und 64-Bit-Apps in %ProgramFiles%, und %ProgramFiles(x86)% für 32-Bit-Apps, die auf x64 ausgeführt werden. Benutzer- oder App-Daten dürfen aufgrund der für diesen Ordner konfigurierten Sicherheitsberechtigungen nie an diesem Speicherort gespeichert werden.  
</dl> </dd> 10.2 Your app must avoid starting automatically on startup <dl> Ihre App sollte z. B. keine der folgenden Bedingungen festlegen:  
</dl>

-   Registrierungsschlüssel HKLM und oder HKCU unter Software \\ Microsoft \\ Windows \\ CurrentVersion
-   Registrierungsschlüssel HKLM und oder HKCU unter Software \\ Wow6432Node \\ Microsoft \\ Windows \\ CurrentVersion
-   Startmenü AllPrograms > STARTUP

</dd> 10.3 Your app data, which must be shared among users on the computer, should be stored within ProgramData  
10.4 Your app s data that is exclusive to a specific user and that is not to be shared with other users of the computer, must be stored in Users\\&lt;username&gt;\\AppData  
10.5 Your app must never write directly to the "Windows" directory and or subdirectories <dl> Verwenden Sie die richtigen Methoden zum Installieren von Dateien, z. B. Schriftarten oder Treiber.  
</dl> </dd> 10.6 Your app must write user data at first run and not during the installation in  per-machine  installations <dl> Wenn die App installiert ist, gibt es keinen richtigen Benutzerspeicherort zum Speichern von Daten. Versuche einer App, das Standardverhalten von Zuordnungen auf Computerebene nach der Installation zu ändern, sind nicht erfolgreich. Stattdessen müssen Standardwerte auf Benutzerebene beansprucht werden, wodurch verhindert wird, dass mehrere Benutzer die Standardwerte der anderen Benutzer überschreiben.  
</dl> </dd> 10.7 Exceptions and Waivers <dl> Apps, die in den globalen Assemblycache (GAC) von .NET-Apps schreiben, sollten Assemblyabhängigkeiten privat halten und im App-Verzeichnis speichern, es sei denn, die Freigabe einer Assembly ist explizit erforderlich.  
</dl> </dd> </dl>

## <a name="11-apps-must-support-multi-user-sessions"></a>11. Apps müssen Sitzungen mit mehreren Benutzer unterstützen.

Windows Benutzer sollten gleichzeitige Sitzungen ohne Konflikte oder Unterbrechungen ausführen können.<dl> 11.1 Ihre App muss sicherstellen, dass die normale Funktionalität der App nicht beeinträchtigt wird, wenn sie in mehreren Sitzungen lokal oder remote ausgeführt wird.  
11.2 Die Einstellungen und Datendateien Ihrer App dürfen nicht benutzerübergreifend beibehalten werden.  
11.3 Der Datenschutz und die Einstellungen eines Benutzers müssen auf die Sitzung des Benutzers isoliert werden.  
11.4 Die Instanzen Ihrer App müssen voneinander isoliert sein. <dl> Dies bedeutet, dass Benutzerdaten aus einer Instanz für eine andere Instanz der App nicht sichtbar sind. Sound in einer inaktiven Benutzersitzung sollte in einer aktiven Benutzersitzung nicht gehört werden. In Fällen, in denen mehrere App-Instanzen freigegebene Ressourcen verwenden, muss die App sicherstellen, dass es keinen Konflikt gibt.  
</dl> </dd> 11.5 Apps that are installed for multiple users must store data in the correct folder(s) and registry locations <dl> Weitere Informationen finden Sie in den UAC-Anforderungen.  
</dl> </dd> 11.6 User apps must be able to run in multiple user sessions (Fast User Switching) for both local and remote access  
11.7 Your app must check other terminal service (TS) sessions for existing instances of the app  
</dl>**Note:** If an app does not support multiple user sessions or remote access, it must clearly state this when launched from this kind of session.

## <a name="12-apps-must-support-x64-versions-of-windows"></a>12. Apps müssen x64-Versionen von Windows

Mit zunehmender 64-Bit-Hardware erwarten Benutzer, dass App-Entwickler die Vorteile der 64-Bit-Architektur nutzen, indem sie ihre Apps zu 64-Bit migrieren oder dass 32-Bit-Versionen der App gut unter 64-Bit-Versionen von Windows.<dl> 12.1 Ihre App muss nativ 64-Bit unterstützen, oder mindestens 32-Bit-Windows-basierte Apps müssen nahtlos auf 64-Bit-Systemen ausgeführt werden, um die Kompatibilität mit 64-Bit-Versionen von Windows  
12.2 Ihre App und ihre Installationsprogramme dürfen keinen 16-Bit-Code enthalten oder sich auf eine 16-Bit-Komponente verlassen.  
12.3 Das Setup Ihrer App muss die richtigen Treiber und Komponenten für die 64-Bit-Architektur erkennen und installieren.  
12.4 Alle Shell-Plug-Ins müssen auf 64-Bit-Versionen von Windows  
12.5 App, die unter dem WoW64-Emulator ausgeführt wird, sollte nicht versuchen, Wow64-Virtualisierungsmechanismen zu unter- oder zu umgehen. <dl> Wenn es bestimmte Szenarien gibt, in denen Apps erkennen müssen, ob sie unter dem WoW64-Emulator ausgeführt werden, sollten sie dies durch Aufrufen von IsWow64Process tun.  
</dl> </dd> </dl>

## <a name="summary-of-the-tests-performed-on-desktop-apps"></a>Zusammenfassung der Tests, die für Desktop-Apps ausgeführt wurden



|   Testname                                                             |   Mögliche Testergebnisse   |
|-------------------------------------------------------------------------|---------------------------|
| Befolgen von Systemneustart-Manager-Meldungen                               | Pass/Fail               |
| Bereinige umkehrbare Installation                                                | Pass/Fail/Warning     |
| Kompatibilität & Resilienztest                                         | Pass/Fail/Warning     |
| Digital signierter Dateitest                                              | Pass/Fail/Warning     |
| Installieren im richtigen Ordnertest                                     | Warnung                   |
| Multiuser-Sitzungstest                                                  | Warnung                   |
| Test zur Überprüfung der Betriebssystemversion                                                | Pass/Fail               |
| Tresor Modustest                                                          | Pass/Fail               |
| Support x64 Windows test                                                | Pass/Fail               |
| Testen auf Änderungen an Windows Sicherheitsfeatures (Attack Surface Analyzer) | Pass/Fail/Warning     |
| Testen auf Änderungen an Windows-Sicherheitsfeatures (BinScope Binary Analyzer) | Warnung                   |
| Test der Benutzerkontensteuerung (User Account Control, UAC)                                         | Pass/Fail/Warning     |



 

## <a name="conclusion"></a>Zusammenfassung

Wenn sich diese Anforderungen weiterentwickeln, werden wir die Änderungen im Revisionsverlauf unten notieren. Stabile Anforderungen sind wichtig, um Ihre beste Arbeit zu erreichen, daher möchten wir sicherstellen, dass die vorgenommenen Änderungen dauerhaft sind und Ihre Apps weiterhin schützen und verbessern.

Vielen Dank, dass Sie sich erneut für unsere Verpflichtung zur Bereitstellung hervorragender Kundenerfahrungen verpflichtet haben.

## <a name="revision-history"></a>Revisionsverlauf



| Date         | Version | Revisionsbeschreibung                                            | Link zum Dokument                                                             |
|--------------|---------|-----------------------------------------------------------------|------------------------------------------------------------------------------|
| 20. Dezember 2011 | 1.0     | Erster Entwurf des Dokuments für die Vorschau.                          |                                                                              |
| 26. Januar 2012 | 1.1     | Aktualisieren Sie auf Abschnitt \# 2.                                          | [1.1](archive--certification-requirements-for-windows-desktop-apps-v1-1.md) |
| 31. Mai 2012 | 1.2     | Zusammenfassungstestergebnisse hinzugefügt<br/> Endgültiges Dokument<br/> | 1.2                                                                          |



 

## <a name="learn-more-about-desktop-app-certification"></a>Weitere Informationen zur Zertifizierung von Desktop-Apps



| Anforderung                                                                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Weitere Informationen                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kompatibilität und Resilienz                                                    | Abstürze & Hängen stellen eine erhebliche Unterbrechung für Benutzer dar und verursachen Frust. Es wird erwartet, dass Apps resilient und stabil sind. Die Beseitigung solcher Fehler trägt dazu bei, sicherzustellen, dass Software besser vorhersagbar, wartbar, leistungsfähig und vertrauenswürdiger ist.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [Windows Betriebssysteme Vista, Windows 7 und Windows 8](/previous-versions/windows/it-pro/windows-7/cc722305(v=ws.10))<br/> [Application Verifier](/previous-versions/aa480483(v=msdn.10))<br/> [AppInit-DLLs](https://support.microsoft.com/kb/197571)<br/> |
| Befolgen sie Windows-Sicherheit bewährten Methoden.                                       | Die Verwendung Windows bewährten Sicherheitsmethoden trägt dazu bei, die Gefährdung durch Windows Angriffsflächen zu vermeiden. Angriffsflächen sind die Einstiegspunkte, die ein böswilliger Angreifer verwenden kann, um das Betriebssystem auszunutzen, indem er Sicherheitsrisiken in der Zielsoftware nutzt. Eines der schlechtesten Sicherheitsrisiken ist die Rechteerweiterung.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | [Attack Surface Analyzer](https://technet.microsoft.com/security/gg749821)<br/> [Access Control Listen](/windows/desktop/SecAuthZ/access-control-lists)<br/>                                                                                                                                |
| Unterstützung Windows-Sicherheit Features                                               | Das Windows Betriebssystem hat viele Maßnahmen zur Unterstützung der Systemsicherheit und des Datenschutzes implementiert. Anwendungen müssen diese Maßnahmen unterstützen, um die Integrität des Betriebssystems aufrechtzuerhalten. Falsch kompilierte Anwendungen können Pufferüberläufe verursachen, die wiederum Denial-of-Service-Angriffe verursachen oder böswilligen Code ausführen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [BinScope-Toolreferenz](https://blogs.microsoft.com/cybertrust/2012/08/15/microsofts-free-security-tools-binscope-binary-analyzer/)<br/>                                                                                                                                             |
| Befolgen von Meldungen des Systemneustart-Managers                                       | Wenn Benutzer das Herunterfahren initiieren, haben sie in den meisten Fällen den starken Wunsch, dass das Herunterfahren erfolgreich ist. sie sind möglicherweise in der Lage, das Büro zu verlassen, und "nur" möchten, dass ihre Computer ausgeschaltet werden. Apps müssen diesen Wunsch berücksichtigen, indem sie das Herunterfahren nicht blockieren. In den meisten Fällen ist das Herunterfahren möglicherweise nicht kritisch, Apps müssen jedoch auf die Möglichkeit eines kritischen Herunterfahrens vorbereitet werden.                                                                                                                                                                                                                                                                                                                                                                                                                                       | [Änderungen beim Herunterfahren von Anwendungen in Windows Vista](/previous-versions/windows/desktop/ms700677(v=vs.85))<br/> [Neustart-Manager-Entwicklung](/previous-versions/bb756958(v=msdn.10))<br/>                                                                              |
| Clean Reversible Installation                                                   | Mit einer sauberen, umkehrbaren Installation können Benutzer Apps auf ihren Systemen erfolgreich verwalten (bereitstellen und entfernen).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | [Gewusst wie: Installieren von erforderlichen Komponenten mit einer ClickOnce-Anwendung](/visualstudio/deployment/how-to-install-prerequisites-with-a-clickonce-application?view=vs-2015)<br/> [Anwendungsinstallation auf 64-Bit-Systemen](/windows/desktop/WinProg64/application-installation)<br/>                                                |
| Digitales Signieren von Dateien und Treibern                                                | Mit einer digitalen Authenticode-Signatur können Benutzer sicherstellen, dass die Software echt ist. Außerdem kann erkannt werden, ob eine Datei manipuliert wurde, z. B. wenn sie von einem Virus infiziert wurde. Die Erzwingung der Kernelmodus-Codesignatur ist ein Windows Feature, das als Codeintegrität (Code Integrity, CI) bezeichnet wird und die Sicherheit des Betriebssystems verbessert, indem jedes Mal, wenn das Image der Datei in den Arbeitsspeicher geladen wird, die Integrität einer Datei überprüft wird. CI erkennt, ob schädlicher Code eine Systembinärdatei geändert hat. Generiert auch ein Diagnose- und Systemüberwachungsprotokollereignis, wenn die Signatur eines Kernelmoduls nicht ordnungsgemäß überprüft werden kann.                                                                                                                                                                            | [Digitale Signaturen für Kernelmodule auf Windows](/previous-versions/windows/hardware/design/dn653559(v=vs.85))<br/>                                                                                                                                             |
| Installation oder App-Start nicht basierend auf der Versionsprüfung des Betriebssystems blockieren | Es ist wichtig, dass Kunden nicht daran gehindert werden, ihre App zu installieren oder auszuführen, wenn es keine technischen Einschränkungen gibt. Wenn Apps für Windows Vista oder höhere Versionen geschrieben wurden, sollten sie im Allgemeinen keinen Grund haben, die Betriebssystemversion zu überprüfen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | [Betriebssystemversionsierung](../win7appqual/operating-system-versioning.md)<br/>                                                                                                                                                                                           |
| Nicht laden von Diensten und Treibern im Tresor Modus                                   | Tresor Modus ermöglicht Benutzern die Diagnose und Problembehandlung Windows. Sofern dies nicht für grundlegende Vorgänge des Systems (z. B. Speichergerätetreiber) oder für Diagnose- und Wiederherstellungszwecke (z. B. Virenscanner) erforderlich ist, dürfen Treiber und Dienste nicht auf das Laden im abgesicherten Modus festgelegt werden. Standardmäßig startet der abgesicherte Modus nicht die meisten Treiber und Dienste, die nicht mit Windows vorinstalliert wurden. Sie sollten deaktiviert bleiben, es sei denn, das System erfordert sie für grundlegende Vorgänge oder zu Diagnose- und Wiederherstellungszwecken.                                                                                                                                                                                                                                                                                         | [Bestimmen, ob das Betriebssystem im Tresor Modus ausgeführt wird](/windows-hardware/drivers/kernel/determining-whether-the-operating-system-is-running-in-safe-mode)<br/> [Bestimmen, ob das System im Tresor Modus von einem Gerätetreiber aus ausgeführt wird](https://support.microsoft.com/kb/837643)<br/>       |
| Befolgen der Richtlinien für die Benutzerkontensteuerung (User Account Control, UAC)                                    | Einige Windows App werden im Sicherheitskontext eines Administratorkontos ausgeführt, und viele erfordern übermäßige Benutzerrechte und Windows Berechtigungen. Durch die Steuerung des Zugriffs auf Ressourcen können Benutzer ihre Systeme gegen unerwünschte Änderungen steuern (eine unerwünschte Änderung kann schädlich sein, z. B. ein Rootkit, das den Computer unbeaufsichtigt übernimmt, oder eine Aktion von Personen, die eingeschränkte Berechtigungen haben, z. B. ein Mitarbeiter, der unzulässige Software auf einem Arbeitscomputer installiert). Die wichtigste Regel für die Steuerung des Zugriffs auf Ressourcen besteht darin, den minimalen Standardbenutzerkontext für den Zugriff bereitzustellen, der erforderlich ist, damit ein Benutzer seine erforderlichen Aufgaben ausführen kann. Die Einhaltung der UAC-Richtlinien bietet der App bei Bedarf die erforderlichen Berechtigungen, ohne das System ständig sicherheitsrisiken ausgesetzt zu lassen. | [Benutzerkontensteuerung](/windows/desktop/uxguide/winenv-uac)<br/> [UAC: Richtlinien für Anwendungsupdates](/previous-versions/aa480152(v=msdn.10))<br/>                                                                       |
| Standardmäßig in den richtigen Ordnern installieren                                       | Benutzer sollten über eine konsistente und sichere Umgebung mit dem Standardinstallationsspeicherort von Dateien verfügen und gleichzeitig die Option beibehalten, eine App an dem von ihnen gewählten Speicherort zu installieren. Es ist auch erforderlich, App-Daten am richtigen Speicherort zu speichern, damit mehrere Personen denselben Computer verwenden können, ohne die Daten und Einstellungen gegenseitig zu beschädigen oder zu überschreiben.                                                                                                                                                                                                                                                                                                                                                                                                                                                          | [Zusammenfassung der Installations-/Deinstallationsanforderungen](/previous-versions/ms954376(v=msdn.10))<br/>                                                                                                                                                                                    |
| Unterstützen von Sitzungen mit mehreren Benutzern                                                     | Windows Benutzer sollten in der Lage sein, gleichzeitige Sitzungen ohne Konflikte oder Unterbrechungen auszuführen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | [Remotedesktopdienste Programmierrichtlinien](/windows/desktop/TermServ/terminal-services-programming-guidelines)<br/>                                                                                                                                                                      |
| Unterstützung von x64-Versionen von Windows                                                 | Da 64-Bit-Hardware immer häufiger auftritt, erwarten Benutzer, dass App-Entwickler die Vorteile der 64-Bit-Architektur nutzen, indem sie ihre Apps zu 64-Bit migrieren oder dass 32-Bit-Versionen der App gut unter 64-Bit-Versionen von Windows ausgeführt werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | [Anwendungskompatibilität: Windows Vista 64-Bit](/previous-versions/bb756962(v=msdn.10))<br/>                                                                                                                                                                              |



 

## <a name="see-also"></a>Weitere Informationen

-   [Windows Hardwarezertifizierungsprogramm](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))
-   [Zertifizierungsanforderungen für Windows Store Apps](/legal/windows/agreements/store-policies)

 

