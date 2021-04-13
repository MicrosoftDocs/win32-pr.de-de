---
title: Desktopzertifizierungsanforderungen
description: Dokument Version 10document Date 29. Juli... in diesem Dokument sind die technischen Anforderungen und Berechtigungs Qualifikationen enthalten, die eine Desktop-App erfüllen muss, damit Sie am Zertifizierungsprogramm für Windows 10-Desktop-Apps teilnehmen kann.
ms.assetid: 0F19774E-5258-4152-BBD7-9C37A05C7F69
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4789c4069221b0ea6f65a8636ee35501171089e6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104391107"
---
# <a name="certification-requirements-for-windows-desktop-apps"></a>Zertifizierungsanforderungen für Windows-Desktop-Apps

**Dokument Version:** 10

**Dokument Datum:** 29. Juli 2015

Dieses Dokument enthält die technischen Anforderungen und Berechtigungs Qualifizierungen, die eine Desktop-App erfüllen muss, damit Sie am Zertifizierungsprogramm für Windows 10-Desktop-Apps teilnehmen können.

## <a name="welcome"></a>Willkommen!

Die Windows-Plattform unterstützt ein breites Ökosystem von Produkten und Partnern. Wenn Sie das Windows-Logo auf Ihrem Produktanzeigen, steht eine Beziehung und eine gemeinsame Verpflichtung der Qualität zwischen Microsoft und Ihrem Unternehmen. Kunden Vertrauen der Windows-Marke auf Ihrem Produkt, da sie sicherstellt, dass Sie Kompatibilitäts Standards erfüllt und auf der Windows-Plattform gut funktioniert. Wenn Sie die Windows-App-Zertifizierung erfolgreich übergeben haben, kann Ihre APP im Windows-Kompatibilitäts Center angezeigt werden, und Sie können das Zertifizierungs Logo auf Ihrer Website anzeigen.

Das Windows-App-Zertifizierungsprogramm besteht aus Programm-und technischen Anforderungen, um sicherzustellen, dass Drittanbieter-apps, die die Windows-Marke ausführen, auf PCs mit Windows leicht zu installieren und zuverlässig sind. Kunden Werten Stabilität, Kompatibilität, Zuverlässigkeit, Leistung und Qualität in den von Ihnen erworbenen Systemen. Microsoft konzentriert sich auf seine Investitionen, um diese Anforderungen an Software-apps zu erfüllen, die auf der Windows-Plattform für PCs ausgeführt werden sollen. Diese Bemühungen umfassen Kompatibilitätstests für die Konsistenz der Leistung, eine verbesserte Leistung und eine höhere Sicherheit auf PCs mit Windows-Software. Microsoft-Kompatibilitätstests wurden in Zusammenarbeit mit Branchenpartnern entwickelt und werden als Reaktion auf Branchenentwicklungen und Kundennachfrage kontinuierlich verbessert.

Das zertifizierungskit für Windows-apps wird verwendet, um die Konformität mit diesen Anforderungen zu überprüfen und alle früheren Versionen des Kit zu ersetzen, die zur Validierung unter Windows 7, Windows 8 oder Windows 8.1 verwendet werden. Das Windows-zertifizierungskit für apps ist eine der Komponenten, die im Windows Software Development Kit (SDK) für Windows 10 enthalten sind.

## <a name="app-eligibility"></a>App-Berechtigung

Damit eine APP für die Windows 10-Desktop-App-Zertifizierung qualifiziert wird, muss Sie die folgenden Kriterien und alle technischen Anforderungen erfüllen, die in diesem Dokument aufgeführt sind.

-   Es muss sich um eine eigenständige App handeln.
-   Es muss auf einem lokalen Windows 10-PC ausgeführt werden.
-   Dabei kann es sich um eine Client Komponente einer zertifizierten Windows Server-App handeln.
-   Der Code muss Code und Funktions fertig sein.
-   Es darf nicht mit Windows Store-Apps über lokale Mechanismen kommunizieren, einschließlich über Dateien und Registrierungsschlüssel, außer in den unterstützten Enterprise-Szenarios.
-   Die Sicherheit oder die Funktionalität des Windows-Systems darf nicht beeinträchtigt oder gefährdet werden.
-   Sie muss einen eindeutigen Namen aufweisen und darf nicht von anderen Personen geschützt werden.
-   Alle externen Komponenten müssen separat zertifiziert werden oder mit dem zertifizierungskit für Windows-Apps kompatibel sein.
-   Sie muss über eine Opt-out-Option für alle gebündelten apps verfügen.

Wenn die Desktop-App an die Antiviren-und/oder Antispywareprodukte (d. h. Antischadsoftware) übermittelt wird, muss Sie den Richtlinien für Antischadsoftware-Richtlinien entsprechen. Die Windows 10 Antimalware-API-Lizenz und der Auflistungs Vertrag müssen vor der Übermittlung signiert und wirksam sein. Der Partner muss Mitglied von sein, oder es muss sich um die Mitglieder von Mitgliedern handeln, die in einer der in der Vereinbarung aufgeführten Organisationen vorhanden sind. Die Funktionalität muss von einem der in der Vereinbarung aufgelisteten Organisationen unter Windows 10 zertifiziert werden. Die APP muss mindestens einmal in den letzten 12 Monaten getestet und für die Erkennung und Reinigung zertifiziert sein.

## <a name="1-apps-are-compatible-and-resilient"></a>1. apps sind kompatibel und robust

Die Zeiten, in denen eine APP abstürzt oder reagiert, führen zu einer großen Benutzer Frustration. Apps werden erwartungsgemäß robust und stabil sein. durch das vermeiden solcher Fehler kann sichergestellt werden, dass die Software besser vorhersagbar und verwaltbar und leistungsfähig und vertrauenswürdig ist.<dl> 1,1 Ihre APP darf keine Abhängigkeit von den Windows-Kompatibilitäts Modi, der AppHelp-Nachricht und oder anderen Kompatibilitäts Korrekturen annehmen.  
1,2 Ihre APP muss über ein Kompatibilitäts Manifest verfügen, und Sie müssen die entsprechenden GUIDs für die unterstützten Versionen von Windows verwenden.  
1,3 Ihre APP muss mithilfe des Assemblymanifests der Anwendung und nicht durch Aufrufen von SetProcessDPIAware dpi-fähig sein.  
1,4 Ihre APP darf keine Abhängigkeit von der VB6-Laufzeit annehmen  
1,5 Ihre APP darf keine beliebigen DLLs laden, um Win32-API-Aufrufe mithilfe von HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows AppInit- \_ DLLs abzufangen.  
</dl>

## <a name="2-apps-must-adhere-to-windows-security-best-practices"></a>2. apps müssen den bewährten Methoden für die Windows-Sicherheit entsprechen

Mithilfe der bewährten Methoden für Windows-Sicherheit können Sie das Risiko von Windows-Angriffs Oberflächen vermeiden. Angriffsflächen sind die Einstiegspunkte, mit denen ein böswilliger Angreifer das Betriebssystem ausnutzen könnte, indem er Sicherheitsrisiken in der Ziel Software nutzt. Eine der schlechtesten Sicherheitslücken ist die Erhöhung von Berechtigungen.

Beachten Sie, dass die Tests 2,1 2,6 nur für Desktop-Apps anwendbar sind, die unter Windows 7, Windows 8 oder Windows 8.1 getestet wurden.<dl> 2,1 Ihre APP muss starke und geeignete [ACLs](/windows/desktop/SecAuthZ/access-control-lists) verwenden, um ausführbare Dateien zu sichern.  
2,2 Ihre APP muss starke und geeignete [ACLs](/windows/desktop/SecAuthZ/access-control-lists) zum Sichern von Verzeichnissen verwenden.  
2,3 Ihre APP muss starke und geeignete [ACLs](/windows/desktop/SecAuthZ/access-control-lists) verwenden, um Registrierungsschlüssel zu sichern.  
2,4 Ihre APP muss starke und geeignete [ACLs](/windows/desktop/SecAuthZ/access-control-lists) zum Sichern von Verzeichnissen verwenden, die Objekte enthalten  
2,5 Ihre APP muss den nicht-Administrator Zugriff auf Dienste, die anfällig für Manipulationen sind, verringern.  
2,6 Ihre APP muss verhindern, dass Dienste mit schnellen Neustarts mehr als zweimal alle 24 Stunden neu gestartet werden.  
</dl>

**Hinweis: der Zugriff sollte nur für die Entitäten erteilt werden, für die dies erforderlich ist.**

Das Windows-App-Zertifizierungsprogramm überprüft, ob Windows-Angriffs Oberflächen nicht verfügbar gemacht werden, indem überprüft wird, ob ACLs und Dienste auf eine Weise implementiert werden, in der das Windows-System nicht gefährdet ist.

## <a name="3-apps-support-windows-security-features"></a>3. apps unterstützen Windows-Sicherheitsfeatures

Das Windows-Betriebssystem verfügt über zahlreiche Features zur Unterstützung von Systemsicherheit und Datenschutz. Apps müssen diese Features unterstützen, um die Integrität des Betriebssystems aufrechtzuerhalten. Nicht ordnungsgemäß kompilierte Apps können Pufferüberläufe verursachen, die wiederum zu Denial-of-Service-Angriffen führen oder böswillige Codeausführung zulassen. <dl> 3,1 Ihre APP darf nicht allowpartiallytreuhänder dcallersattribute (APTCA) verwenden, um sicheren Zugriff auf Assemblys mit starkem Namen sicherzustellen.  
3,2 Ihre APP muss mit dem/SAFESEH-Flag kompiliert werden, um die Behandlung sicherer Ausnahmen sicherzustellen  
3,3 Ihre APP muss mit dem/NXCOMPAT-Flag kompiliert werden, um die Datenausführung zu verhindern.  
3,4 Ihre APP muss mit dem/DynamicBase-Flag für Address Space Layout Anordnung (ASLR) kompiliert werden.  
3,5 Ihre APP darf die freigegebenen PE-Abschnitte nicht lesen/schreiben  
</dl>

## <a name="4-apps-must-adhere-to-system-restart-manager-messages"></a>4. apps müssen die Nachrichten des Systemneustart-Managers einhalten.

Wenn Benutzer das Herunterfahren initiieren, haben Sie in der Regel einen starken Wunsch, das Herunterfahren erfolgreich zu sehen. Sie sind möglicherweise eilig, wenn Sie das Büro verlassen möchten und möchten, dass die Computer deaktiviert werden. Apps müssen diesen Wunsch beachten, indem Sie das Herunterfahren nicht blockieren. Obwohl das Herunterfahren in den meisten Fällen nicht entscheidend ist, müssen apps auf die Möglichkeit eines kritischen herunter Fahrens vorbereitet werden.<dl> 4,1 Ihre APP muss wichtige Herunterfahr Vorgänge entsprechend verarbeiten. <dl> Bei einem kritischen Herunterfahren werden apps, die für WM \_ queryendsession den Wert false zurückgeben, mit WM \_ EndSession gesendet und geschlossen, während diejenigen, die als Reaktion auf WM queryendsession als Timeout festgelegt werden, \_ beendet werden.  
</dl> </dd> 4.2 A GUI app must return TRUE immediately in preparation for a restart <dl> WM \_ queryendsession mit lParam = EndSession \_ CloseApp (0x1).  
Konsolen-Apps können SetConsoleCtrlHandler aufrufen, um die Funktion anzugeben, mit der Benachrichtigungen zum Herunterfahren behandelt werden. Dienst-Apps können RegisterServiceCtrlHandlerEx aufrufen, um die Funktion anzugeben, die Shutdown-Benachrichtigungen empfängt.  
</dl> </dd> 4.3 Your app must return 0 within 30 seconds and shut down <dl> WM \_ EndSession mit lParam = EndSession \_ CloseApp (0x1).  
Die APP sollte mindestens eine Vorbereitung durch Speichern von Benutzerdaten und das Angeben der Informationen sein, die nach einem Neustart erforderlich sind.  
</dl> </dd> 4.4 Console apps that receive the CTRL\_C\_EVENT notification should shut down immediately  
4.5 Drivers must not veto a system shutdown event  
</dl>
<strong>Hinweis: apps, die das Herunterfahren aufgrund eines Vorgangs blockieren müssen, der nicht unterbrochen werden kann, sollten den Grund für den Benutzer erläutern.</strong> Verwenden Sie shutdownblockreasoncreate, um eine Zeichenfolge zu registrieren, die den Grund für den Benutzer erläutert. Nachdem der Vorgang abgeschlossen wurde, sollte die APP shutdownblockreasondestroy anrufen, um anzugeben, dass das System heruntergefahren werden kann.

## <a name="5-apps-must-support-a-clean-reversible-installation"></a>5. apps müssen eine saubere, umkehrbare Installation unterstützen.

Eine saubere, umkehrbare Installation ermöglicht es Benutzern, Apps auf Ihren Systemen erfolgreich zu verwalten (bereitzustellen und zu entfernen).<dl> 5,1 Ihre APP muss eine saubere, umkehrbare Installation ordnungsgemäß implementieren <dl> Wenn die Installation fehlschlägt, sollte die app in der Lage sein, ein Rollback auszuführen und den Computer in den vorherigen Zustand zu versetzen.  
</dl> </dd> 5.2 Your app must never force the user to restart the computer immediately <dl> Das Neustarten des Computers sollte am Ende der Installation, Deinstallation oder Aktualisierung nie die einzige Option sein. Benutzer sollten die Möglichkeit haben, später neu zu starten.  
</dl> </dd> 5.3 Your app must never be dependent on 8.3 short file names (SFN)  
5.4 Your app must never block silent install/uninstall  
5.5 Your app installer must create the correct registry entries to allow successful detection and uninstalls <dl> Für Windows-Inventur Tools und telemetrietools sind umfassende Informationen zu installierten apps erforderlich. Wenn Sie ein MSI-basiertes Installationsprogramm verwenden, erstellt MSI die unten aufgeführten Registrierungseinträge automatisch. Wenn Sie keinen MSI-Installer verwenden, muss das Installations Modul während der Installation die folgenden Registrierungseinträge erstellen:  
</dl>

-   DisplayName
-   InstallLocation
-   Publisher
-   UninstallString
-   VersionMajor oder MajorVersion
-   VersionMinor oder MinorVersion

</dd> 5.6 The app must remove all of its entries from Add/ Remove Programs upon uninstall  
</dl>

## <a name="6-apps-must-digitally-sign-files-and-drivers"></a>6. apps müssen Dateien und Treiber digital signieren.

Eine digitale Authenticode-Signatur ermöglicht es Benutzern, sicherzustellen, dass die Software echt ist. Außerdem können Sie erkennen, ob eine Datei manipuliert wurde, z. b. Wenn Sie von einem Virus infiziert wurde. Der Kernelmoduscode-Signatur Erzwingung ist ein Windows-Feature, das als Code Integrität (CI) bezeichnet wird. Dadurch wird die Sicherheit des Betriebssystems verbessert, indem die Integrität einer Datei jedes Mal überprüft wird, wenn das Image der Datei in den Arbeitsspeicher geladen wird. CI erkennt, ob bösartiger Code eine System Binärdatei geändert hat. Generiert auch ein Diagnose-und System Überwachungs Protokoll-Ereignis, wenn die Signatur eines Kernel Moduls nicht korrekt überprüft werden kann. <dl> 6,1 alle ausführbaren Dateien (. exe,. dll,. ocx,. sys,. cpl,. drv,. SCR) müssen mit einem Authenticode-Zertifikat signiert werden.  
6,2 alle von der APP installierten Kernelmodustreiber müssen über eine Microsoft-Signatur verfügen, die über das Windows-Hardware Zertifizierungsprogramm abgerufen wird. Alle Datei System Filter-Treiber müssen von Microsoft signiert werden.  
6,3 Ausnahmen und waivers <dl> Waivers werden nur für nicht signierte Redistributables von Drittanbietern berücksichtigt, ausgenommen Treiber. Ein Kommunikations Nachweis ist erforderlich, um eine signierte Version der verteilbaren verteilbaren Dateien anzufordern.  
</dl> </dd> </dl>

## <a name="7-apps-dont-block-installation-or-app-launch-based-on-an-operating-system-version-check"></a>7. apps blockieren die Installation oder App-Start nicht basierend auf einer Überprüfung der Betriebssystemversion.

Es ist wichtig, dass Kunden die Installation oder Ausführung Ihrer APP nicht künstlich blockieren, wenn keine technischen Einschränkungen vorliegen. Im Allgemeinen sollte die Betriebssystemversion nicht überprüft werden, wenn Apps für Windows Vista oder spätere Versionen von Windows geschrieben wurden.<dl> 7,1 Ihre APP darf keine Versions Überprüfungen auf Gleichheit durchführen <dl> Wenn Sie ein bestimmtes Feature benötigen, überprüfen Sie, ob die Funktion selbst verfügbar ist. Wenn Sie Windows 7 benötigen, suchen Sie nach Windows 7 oder höher (>= 6,2). Auf diese Weise kann der Erkennungs Code weiterhin in zukünftigen Versionen von Windows verwendet werden. Treiber Installationsprogramme und Deinstallations Module sollten nie die Betriebssystemversion überprüfen.  
</dl> </dd> 7.2 Exceptions and Waivers will be considered for apps meeting the criteria below:

-   Apps, die als ein Paket bereitgestellt werden, das auch unter Windows 7, Windows 8 und Windows 8.1 ausgeführt wird, und die Betriebssystemversion überprüfen müssen, um zu bestimmen, welche Komponenten auf einem bestimmten Betriebssystem installiert werden müssen.
-   Apps, die nur die Mindestversion des Betriebssystems überprüfen (nur während der Installation, nicht zur Laufzeit), indem nur die genehmigten API-Aufrufe verwendet werden, und die die Mindestanforderungen an die Version des App-Manifests ordnungsgemäß auflisten.
-   Sicherheits-Apps (Antivirus, Firewall usw.), System Dienstprogramme (z. b. Defrag, Sicherungen und Diagnosetools), die die Betriebssystemversion nur mithilfe der genehmigten API-Aufrufe überprüfen.


</dl>

## <a name="8-apps-dont-load-services-or-drivers-in-safe-mode"></a>8. apps laden keine Dienste oder Treiber im abgesicherten Modus

Der abgesicherte Modus ermöglicht es Benutzern, Windows zu diagnostizieren und Probleme zu beheben. Treiber und Dienste dürfen nicht so festgelegt werden, dass Sie im abgesicherten Modus geladen werden, es sei denn, Sie sind für grundlegende System Vorgänge wie z. b. Treiber von Speichergeräten oder für Diagnose-und Wiederherstellungs Zwecke wie Virenscanner erforderlich. Wenn sich Windows im abgesicherten Modus befindet, werden standardmäßig nur die Treiber und Dienste gestartet, die mit Windows vorinstalliert wurden.

-   8,1 Ausnahmen und waivers <dl> Treiber und Dienste, die im abgesicherten Modus gestartet werden müssen, erfordern einen Verzicht. Die Anforderung zum Anfordern von Anforderungen muss alle anwendbaren Treiber oder Dienste enthalten, die in die SafeBoot-Registrierungsschlüssel schreiben, und die technischen Gründe beschreiben, warum die APP oder der Dienst im abgesicherten Modus ausgeführt werden muss. Der APP-Installer muss alle Treiber und Dienste mit diesen Registrierungs Schlüsseln registrieren:  
    </dl>
    -   HKLM/System/CurrentControlSet/Control/SafeBoot/Minimal
    -   HKLM/System/CurrentControlSet/Control/SafeBoot/Network

**Hinweis:** Sie müssen diese Treiber und Dienste testen, um sicherzustellen, dass Sie ohne Fehler im abgesicherten Modus funktionieren.

## <a name="9-apps-must-follow-user-account-control-guidelines"></a>9. apps müssen Richtlinien für die Benutzerkontensteuerung einhalten.

Einige Windows-apps werden im Sicherheitskontext eines Administrator Kontos ausgeführt, und apps fordern häufig übermäßig viele Benutzerrechte und Windows-Berechtigungen an. Das Steuern des Zugriffs auf Ressourcen ermöglicht es Benutzern, ihre Systeme zu kontrollieren und vor unerwünschten Änderungen zu schützen. Eine unerwünschte Änderung kann bösartig sein, z. b. ein Rootkit, das die Kontrolle über den Computer übernimmt, oder das Ergebnis einer Aktion, die von Personen mit eingeschränkten Berechtigungen ausgeführt wird. Die wichtigste Regel zum Steuern des Zugriffs auf Ressourcen besteht darin, den geringsten Zugriffs Standardbenutzer Kontext bereitzustellen, der für einen Benutzer erforderlich ist, um die erforderlichen Aufgaben auszuführen. Durch die folgenden Richtlinien zur Benutzerkontensteuerung (User Account Control, UAC) wird eine APP mit den erforderlichen Berechtigungen bereitgestellt, wenn Sie von der APP benötigt werden, ohne dass das System ständig Sicherheitsrisiken ausgesetzt ist. Bei den meisten apps sind zur Laufzeit keine Administratorrechte erforderlich, und Sie sollten nur als Standardbenutzer ausgeführt werden.<dl> 9,1 Ihre APP muss über ein Manifest verfügen, das Ausführungs Ebenen definiert und dem Betriebssystem mitteilt, welche Berechtigungen die APP benötigt, um ausgeführt zu werden. <dl> Die Markierung des App-Manifests gilt nur für exe-Objekte, nicht für DLLs. Dies liegt daran, dass die UAC während der Prozesserstellung keine DLLs prüft. Beachten Sie auch, dass UAC-Regeln nicht für Microsoft-Dienste gelten. Das Manifest kann entweder eingebettet oder extern sein.  
Um ein Manifest zu erstellen, erstellen Sie eine Datei mit dem Namen <APP \_ -Name # C1.exe. Manifest, und speichern Sie Sie im selben Verzeichnis wie die exe-Datei. Beachten Sie, dass alle externen Manifeste ignoriert werden, wenn die APP über ein internes Manifest verfügt. Beispiel:  
<requestedExecutionLevel Level = "" asInvoker \| highestAvailable \| requilministrator "" UIAccess = "true \| false" "/>  
</dl> </dd> 9.2 Your app s main process must be run as a standard user (asInvoker). <dl> Alle administrativen Funktionen müssen in einen separaten Prozess verschoben werden, der mit Administratorrechten ausgeführt wird. Benutzer seitige apps, wie z. b. die, auf die über die Programmgruppe im Startmenü zugegriffen werden kann, und die Rechte Erweiterung müssen Authenticode signiert sein.  
</dl> </dd> 9.3 Exceptions and Waivers <dl> Für apps, die ihren Hauptprozess mit erweiterten Berechtigungen ausführen (requilministrator oder highestAvailable), ist ein Verzicht erforderlich. Der Hauptprozess wird als Einstiegspunkt des Benutzers für die APP bezeichnet. Waivers werden für die folgenden Szenarien berücksichtigt:

-   Verwaltungs-oder System Tools mit der Ausführungs Ebene "highestAvailable" und/oder "requilesministrator"
-   Nur die Barrierefreiheit oder die Benutzeroberflächenautomatisierungs-Framework-App legt das UIAccess-Flag auf "true" fest, um die Benutzeroberflächen Berechtigungs Isolation (UIPI Um die APP-Nutzung ordnungsgemäß zu starten, muss dieses Flag mit Authenticode signiert sein, und es muss sich an einem geschützten Speicherort im Dateisystem befinden, nämlich in den Programmdateien.


</dl> </dd> </dl>

## <a name="10-apps-must-install-to-the-correct-folders-by-default"></a>10. apps müssen standardmäßig in den richtigen Ordnern installiert werden

Benutzer sollten über ein konsistentes und sicheres Benutzerkonto mit dem standardmäßigen Installationsort von Dateien verfügen, während gleichzeitig die Option zum Installieren einer APP an dem Speicherort Ihrer Wahl beibehalten wird. Es ist auch erforderlich, App-Daten am richtigen Speicherort zu speichern, damit mehrere Personen denselben Computer verwenden können, ohne die Daten und Einstellungen der anderen zu beschädigen oder zu überschreiben. Windows stellt bestimmte Orte im Dateisystem zum Speichern von Programmen und Softwarekomponenten, freigegebenen App-Daten und App-Daten bereit, die für einen Benutzer spezifisch sind.<dl> 10,1 Ihre APP muss standardmäßig im Ordner "Programme" installiert sein. <dl> Für native 32-Bit-und 64-Bit-apps in% Program Files% und% Program Files (x86)% für 32-Bit-apps, die auf x64 ausgeführt werden. Benutzer-oder App-Daten dürfen nicht an diesem Speicherort gespeichert werden, da die Sicherheits Berechtigungen für diesen Ordner konfiguriert sind.  
</dl> </dd> 10.2 Your app must avoid starting automatically on startup <dl> Ihre APP sollte beispielsweise Folgendes nicht festlegen:  
</dl>

-   Registrierungs Lauf Schlüssel HKLM und oder HKCU unter Software \\ Microsoft \\ Windows \\ CurrentVersion
-   Registrierungs Lauf Schlüssel HKLM und oder HKCU unter Software \\ Wow6432Node \\ Microsoft \\ Windows \\ CurrentVersion
-   Startmenü allprogramme > Start

</dd> 10.3 Your app data, which must be shared among users on the computer, should be stored within ProgramData  
10.4 Your app s data that is exclusive to a specific user and that is not to be shared with other users of the computer, must be stored in Users\\<username>\\APPDATA  
10,5 Ihre APP darf niemals direkt in das Verzeichnis "Windows" und die Unterverzeichnisse schreiben. <dl> Verwenden Sie die richtigen Methoden zum Installieren von Dateien, z. b. Schriftarten oder Treiber.  
</dl> </dd> 10.6 Your app must write user data at first run and not during the installation in  per-machine  installations <dl> Wenn die APP installiert ist, gibt es keinen korrekten Benutzer Speicherort, an dem die Daten gespeichert werden sollen. Versuche einer APP, das Standard Zuordnungs Verhalten auf Computer Ebene nach der Installation zu ändern, sind nicht erfolgreich. Stattdessen müssen die Standardwerte auf der Ebene einzelner Benutzer beansprucht werden, wodurch verhindert wird, dass mehrere Benutzer die Standardwerte der anderen überschreiben.  
</dl> </dd> 10.7 Exceptions and Waivers <dl> Für apps, die in den globalen Assemblycache (GAC) schreiben, ist ein Verzicht erforderlich, um die Assemblyabhängigkeiten privat zu halten und im App-Verzeichnis zu speichern, es sei denn, die Freigabe einer Assembly ist explizit erforderlich.  
</dl> </dd> </dl>

## <a name="11-apps-must-support-multi-user-sessions"></a>11. apps müssen mehr Benutzersitzungen unterstützen.

Windows-Benutzer sollten in der Lage sein, gleichzeitige Sitzungen ohne Konflikte oder Unterbrechungen auszuführen.<dl> 11,1 Ihre APP muss sicherstellen, dass die normale Funktionalität der APP nicht beeinträchtigt wird, wenn Sie in mehreren Sitzungen entweder lokal oder Remote ausgeführt wird.  
11,2 die s-Einstellungen und Datendateien der APP dürfen Nichtbenutzer übergreifend beibehalten werden.  
11,3 der Datenschutz und die Einstellungen eines Benutzers müssen für die Benutzersitzung isoliert sein.  
11,4 Ihre APP-Instanzen müssen voneinander isoliert sein. <dl> Dies bedeutet, dass Benutzerdaten aus einer Instanz nicht für eine andere Instanz der App sichtbar sind. Sound in einer inaktiven Benutzersitzung sollte nicht in einer aktiven Benutzersitzung gehört werden. In Fällen, in denen mehrere App-Instanzen freigegebene Ressourcen verwenden, muss die APP sicherstellen, dass kein Konflikt vorliegt.  
</dl> </dd> 11.5 Apps that are installed for multiple users must store data in the correct folder(s) and registry locations <dl> Weitere Informationen finden Sie unter UAC-Anforderungen.  
</dl> </dd> 11.6 User apps must be able to run in multiple user sessions (Fast User Switching) for both local and remote access  
11.7 Your app must check other terminal service (TS) sessions for existing instances of the app  
</dl>
<strong>Hinweis:</strong> Wenn eine APP nicht mehrere Benutzersitzungen oder den Remote Zugriff unterstützt, muss Sie diese beim Starten aus dieser Art von Sitzung eindeutig angeben.

## <a name="12-apps-must-support-x64-versions-of-windows"></a>12. apps müssen x64-Versionen von Windows unterstützen.

Wenn die 64-Bit-Hardware häufiger ist, erwarten Benutzer, dass App-Entwickler die Vorteile der 64-Bit-Architektur nutzen können, indem Sie Ihre apps auf 64-Bit migrieren oder dass 32-Bit-Versionen der APP unter den 64-Bit-Versionen von Windows gut ausgeführt werden.<dl> 12,1 Ihre APP muss eine systemeigene Unterstützung für 64-Bit-und 32-Bit-Windows-basierte apps auf 64-Bit-Systemen ausführen, um die Kompatibilität mit den 64-Bit-Versionen von Windows aufrechtzuerhalten.  
12,2 Ihre APP und die zugehörigen Installationsprogramme dürfen keinen 16-Bit-Code enthalten oder auf eine 16-Bit-Komponente zurückgreifen.  
12,3 das Setup Ihrer APP muss die richtigen Treiber und Komponenten für die 64-Bit-Architektur erkennen und installieren.  
12,4 alle Shell-Plug-Ins müssen auf 64-Bit-Versionen von Windows ausgeführt werden.  
12,5-APP, die unter dem WOW64-Emulator ausgeführt wird, sollte keine WOW64-virtualisierungstechnmechanismen unterteilen oder umgehen <dl> Wenn apps bestimmte Szenarien erkennen müssen, die erkennen müssen, ob Sie im WOW64-Emulator ausgeführt werden, sollten Sie dies durch Aufrufen von IsWow64Process tun.  
</dl> </dd> </dl>

## <a name="conclusion"></a>Zusammenfassung

Wenn sich diese Anforderungen weiterentwickeln, werden die Änderungen im Revisions Verlauf unten aufgeführt. Stabile Anforderungen sind wichtig für die optimale Arbeit. wir wollen also sicherstellen, dass die von uns vorgenommenen Änderungen nachhaltig sind und weiterhin ihre apps schützen und verbessern.

Nochmals vielen Dank für Ihre Teilnahme an unserer Verpflichtung zur Bereitstellung hervorragend Kundenerfahrung.

## <a name="revision-history"></a>Revisionsverlauf



|               |         |                                        |                                                                                  |
|---------------|---------|----------------------------------------|----------------------------------------------------------------------------------|
| Date          | Version | Revisions Beschreibung                   | Link zum Dokument                                                                 |
| 20. Dezember 2011  | 1.0     | Ursprünglicher Entwurf des Dokuments für die Vorschauversion. |                                                                                  |
| 26. Januar 2012  | 1.1     | Aktualisieren Sie auf Abschnitt \# 2.                 | [1.1](archive--certification-requirements-for-windows-desktop-apps-v1-1.md)     |
| 31. Mai 2012  | 1.2     | Zusammenfassungs Testergebnisse hinzugefügt             | [1.2](archive--certification-requirements-for-windows-desktop-apps-v1-2.md)     |
| 29. Juni 2012  | 3.0     | Letztes Windows 8-Dokument               | [3.0](archive--certification-requirements-for-windows-desktop-apps-v3-0.md)     |
| 18. Juni 2013  | 3.1     | Windows 8.1 Dokument                   | [3.1](archive--certification-requirements-for-windows-desktop-apps-v3-1.md)     |
| 20. Feb., 2014  | 3.2     | Internes Update                        |                                                                                  |
| 18. März 2014  | 3.3     | Windows 8.1 Update 1                   | [3.3](https://www.bing.com/search?q=3.3) |
| 29. Juli 2015 | 10      | Windows 10-Update                      | 10                                                                               |





## <a name="learn-more-about-desktop-app-certification"></a>Weitere Informationen zur Desktop-App-Zertifizierung



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Anforderung</td>
<td>BESCHREIBUNG</td>
</tr>
<tr class="even">
<td>Kompatibilität und Resilienz</td>
<td>Abstürze & hängen von einem großen Unterbrechung der Benutzer und bewirken Frustration. Apps werden erwartungsgemäß robust und stabil sein. Dadurch wird sichergestellt, dass die Software besser vorhersagbar und verwaltbar, leistungsfähig und vertrauenswürdig ist.<br/> Der benutzerorientierte App-Einstiegspunkt muss sich aus Kompatibilitätsgründen manifestieren und die Rechte GUID deklarieren. <br/> Benutzer seitige App-Einstiegspunkte müssen für hochauflösende Informationen angezeigt werden, und es müssen die richtigen APIs aufgerufen werden, um High-dpi zu unterstützen.<br/> Weitere Informationen finden Sie unter:
<ul>
<li><a href="https://support.microsoft.com/kb/197571">AppInit-DLLs</a></li>
<li><a href="/windows/desktop/w8cookbook/application--executable--manifest">App-Manifest (ausführbare Datei)</a></li>
<li><a href="/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows">Schreiben von High-dpi-Win32-Anwendungen</a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>Befolgen Sie die bewährten Methoden für die Windows-Sicherheit</td>
<td>Mithilfe der bewährten Methoden für Windows-Sicherheit können Sie das Risiko von Windows-Angriffs Oberflächen vermeiden. Angriffsflächen sind die Einstiegspunkte, mit denen ein böswilliger Angreifer das Betriebssystem ausnutzen könnte, indem er Sicherheitsrisiken in der Ziel Software nutzt. Eine der schlechtesten Sicherheitslücken ist die Erhöhung von Berechtigungen.<br/> Weitere Informationen finden Sie unter:
<ul>
<li><a href="https://technet.microsoft.com/security/gg749821">Attack Surface Analyzer</a></li>
<li><a href="/windows/desktop/SecAuthZ/access-control-lists">Access Control Listen</a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Unterstützung von Windows-Sicherheits Features</td>
<td>Das Windows-Betriebssystem hat viele Measures implementiert, um die Systemsicherheit und den Datenschutz zu unterstützen. Anwendungen müssen diese Measures unterstützen, um die Integrität des Betriebssystems aufrechtzuerhalten. Nicht ordnungsgemäß kompilierte Anwendungen können Pufferüberläufe verursachen, die wiederum zu Denial-of-Service-Angriffen führen oder böswilligen Code ausführen können. Weitere Informationen finden Sie in der <a href="https://blogs.microsoft.com/cybertrust/2012/08/15/microsofts-free-security-tools-binscope-binary-analyzer/">Referenz zum binscope-Tool</a>.</td>
</tr>
<tr class="odd">
<td>Nachrichten des System Neustart-Managers einhalten</td>
<td>Wenn Benutzer das Herunterfahren initiieren, haben Sie in den meisten Fällen einen starken Wunsch, das Herunterfahren erfolgreich zu sehen. Sie sind möglicherweise eilig, wenn Sie das Büro verlassen möchten und möchten, dass die Computer deaktiviert werden &quot; &quot; . Apps müssen diesen Wunsch beachten, indem Sie das Herunterfahren nicht blockieren. Obwohl das Herunterfahren in den meisten Fällen nicht entscheidend ist, müssen apps auf die Möglichkeit eines kritischen herunter Fahrens vorbereitet werden.</td>
</tr>
<tr class="even">
<td>Saubere umkehrbare Installation</td>
<td>Eine saubere, umkehrbare Installation ermöglicht es Benutzern, Apps auf Ihren Systemen erfolgreich zu verwalten (bereitzustellen und zu entfernen). Weitere Informationen finden Sie unter Gewusst <a href="/visualstudio/deployment/how-to-install-prerequisites-with-a-clickonce-application?view=vs-2015">wie: Installieren von erforderlichen Komponenten mit einer ClickOnce-Anwendung</a>.</td>
</tr>
<tr class="odd">
<td>Dateien und Treiber digital signieren</td>
<td>Eine digitale Authenticode-Signatur ermöglicht es Benutzern, sicherzustellen, dass die Software echt ist. Außerdem können Sie erkennen, ob eine Datei manipuliert wurde, z. b. Wenn Sie von einem Virus infiziert wurde. Der Kernelmoduscode-Signatur Erzwingung ist ein Windows-Feature, das als Code Integrität (CI) bezeichnet wird. Dadurch wird die Sicherheit des Betriebssystems verbessert, indem die Integrität einer Datei jedes Mal überprüft wird, wenn das Image der Datei in den Arbeitsspeicher geladen wird. CI erkennt, ob bösartiger Code eine System Binärdatei geändert hat. Generiert auch ein Diagnose-und System Überwachungs Protokoll-Ereignis, wenn die Signatur eines Kernel Moduls nicht korrekt überprüft werden kann.<br/></td>
</tr>
<tr class="even">
<td>Installation oder App-Start nicht auf Basis der Überprüfung der Betriebssystemversion blockieren</td>
<td>Es ist wichtig, dass Kunden die Installation oder Ausführung Ihrer APP nicht künstlich blockieren, wenn keine technischen Einschränkungen vorliegen. Wenn Apps für Windows Vista oder spätere Releases geschrieben wurden, sollten Sie im Allgemeinen keinen Grund haben, die Betriebssystemversion zu überprüfen. Weitere Informationen finden Sie unter <a href="/windows/desktop/Win7AppQual/operating-system-versioning">Betriebs System-Versions</a>Verwaltung.</td>
</tr>
<tr class="odd">
<td>Dienste und Treiber nicht im abgesicherten Modus laden</td>
<td>Der abgesicherte Modus ermöglicht es Benutzern, Windows zu diagnostizieren und Probleme zu beheben. Wenn für grundlegende Vorgänge des Systems (z. b. Speichergerätetreiber) oder für Diagnose-und Wiederherstellungs Zwecke (z. b. Antivirussoftware) nicht benötigt wird, dürfen Treiber und Dienste nicht so festgelegt werden, dass Sie im abgesicherten Modus geladen werden. Standardmäßig startet der abgesicherte Modus nicht die meisten Treiber und Dienste, die nicht mit Windows vorinstalliert wurden. Sie sollten deaktiviert bleiben, es sei denn, das System erfordert Sie für grundlegende Vorgänge oder für Diagnose-und Wiederherstellungs Zwecke.<br/> Weitere Informationen finden Sie unter:
<ul>
<li><a href="/windows-hardware/drivers/kernel/determining-whether-the-operating-system-is-running-in-safe-mode">Ermitteln, ob das Betriebs System im abgesicherten Modus ausgeführt wird</a></li>
<li><a href="https://support.microsoft.com/kb/837643">Bestimmen, ob das System von einem Gerätetreiber im abgesicherten Modus ausgeführt wird</a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Befolgen Sie die Richtlinien zur Benutzerkontensteuerung (UAC).</td>
<td>Einige Windows-apps werden im Sicherheitskontext eines Administrator Kontos ausgeführt, und viele erfordern übermäßige Benutzerrechte und Windows-Berechtigungen. Das Steuern des Zugriffs auf Ressourcen ermöglicht es Benutzern, ihre Systeme gegen unerwünschte Änderungen zu kontrollieren (eine unerwünschte Änderung kann bösartig sein, z. b. ein Rootkit, das den Computer über den Computer übernimmt, oder eine Aktion von Personen mit eingeschränkten Berechtigungen, z. b. ein Mitarbeiter, der unzulässige Software auf einem Arbeitscomputer installiert). Die wichtigste Regel zum Steuern des Zugriffs auf Ressourcen besteht darin, den geringsten Zugriffs Standardbenutzer Kontext bereitzustellen, der für einen Benutzer erforderlich ist, um die erforderlichen Aufgaben auszuführen. Die folgenden UAC-Richtlinien bieten bei Bedarf die APP mit den erforderlichen Berechtigungen, ohne dass das System ständig den Sicherheitsrisiken ausgesetzt ist.<br/> Weitere Informationen finden Sie unter:
<ul>
<li><a href="/windows/desktop/uxguide/winenv-uac">Benutzerkontensteuerung</a></li>
<li><a href="/previous-versions/aa480152(v=msdn.10)">UAC: Richtlinien für Anwendungs Updates</a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>Standardmäßig in den richtigen Ordnern installieren</td>
<td>Benutzer sollten über ein konsistentes und sicheres Benutzerkonto mit dem standardmäßigen Installationsort von Dateien verfügen, während gleichzeitig die Option zum Installieren einer APP an dem von Ihnen gewählten Speicherort beibehalten wird. Es ist auch erforderlich, App-Daten am richtigen Speicherort zu speichern, damit mehrere Personen denselben Computer verwenden können, ohne die Daten und Einstellungen der anderen zu beschädigen oder zu überschreiben. Weitere Informationen finden Sie unter <a href="/previous-versions/ms954376(v=msdn.10)">Zusammenfassung der Installations-/Deinstallations Anforderungen</a>.</td>
</tr>
<tr class="even">
<td>Unterstützung von mehr Benutzersitzungen</td>
<td>Windows-Benutzer sollten in der Lage sein, gleichzeitige Sitzungen ohne Konflikte oder Unterbrechungen auszuführen. Weitere Informationen finden Sie unter <a href="/windows/desktop/TermServ/terminal-services-programming-guidelines">Remotedesktopdienste-Programmier Richtlinien</a>.</td>
</tr>
<tr class="odd">
<td>Unterstützung von x64-Versionen von Windows</td>
<td>Da sich 64-Bit-Hardware weiter verbreitet, erwarten Benutzer, dass App-Entwickler die Vorteile der 64-Bit-Architektur nutzen können, indem Sie Ihre apps auf 64-Bit migrieren oder dass 32-Bit-Versionen der APP unter den 64-Bit-Versionen von Windows gut ausgeführt werden.</td>
</tr>
</tbody>
</table>





## <a name="see-also"></a>Siehe auch

-   [Windows-Hardware Zertifizierungsprogramm](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))
-   [Verwenden des zertifizierungskit für Windows-apps](./using-the-windows-app-certification-kit.md)