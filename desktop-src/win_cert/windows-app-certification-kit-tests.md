---
title: Tests im Zertifizierungskit für Windows-Apps
description: Im folgenden finden Sie Testdetails zur Zertifizierung von dekstopp-apps.
ms.assetid: FA160F46-C266-4F89-B77F-166FEA9ED96B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a353eef0cd73fecac275b750345b3dd97d05dc87
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342366"
---
# <a name="windows-app-certification-kit-tests"></a>Tests im Zertifizierungskit für Windows-Apps

Im folgenden finden Sie Testdetails zur Zertifizierung von dekstopp-apps. Weitere Informationen finden Sie unter [Verwenden des zertifizierungskit für Windows-apps](using-the-windows-app-certification-kit.md).

-   [Saubere umkehrbare Installation](#clean-reversible-install)
-   [Installieren Sie den richtigen Ordner Test.](#install-to-the-correct-folders-test)
-   [Digital signierter Dateitest](#digitally-signed-file-test)
-   [X64-Windows-Test unterstützen](#support-x64-windows-test)
-   [Test der OS-Versions Überprüfung](#os-version-checking-test)
-   [Benutzerkontensteuerung (User Account Control, UAC) Test](#user-account-control-uac-test)
-   [Nachrichten des Systemneustart-Managers einhalten](#adhere-to-system-restart-manager-messages)
-   [Test im abgesicherten Modus](#safe-mode-test)
-   [Test der mehr Benutzersitzung](#multiuser-session-test)
-   [Abstürze und Abstürze-Test](#crashes-and-hangs-test)
-   [Kompatibilitäts-und resilienztest](#compatibility-and-resiliency-test)
-   [Bewährte Windows-Sicherheitsmethoden testen](#windows-security-best-practices-test)
-   [Test der Windows-Sicherheitsfeatures](#windows-security-features-test)
-   [Hoher dpi-Test](#high-dpi-test)

## <a name="clean-reversible-install"></a>Saubere umkehrbare Installation

Installieren und Deinstallieren der APP und überprüfen auf verbleibende Dateien und Registrierungseinträge.

-   Hintergrund
    -   Eine saubere, umkehrbare Installation ermöglicht Benutzern das Bereitstellen und Entfernen von apps. Zum bestanden dieses Tests muss die APP die folgenden Schritte ausführen:
        -   Die APP zwingt den Neustart des Systems nicht sofort nach der Installation oder dem Deinstallieren der app. *Der Installations-oder Deinstallations Vorgang einer APP sollte nach Abschluss des Vorgangs nie einen Systemneustart erfordern. Wenn dies erfordert, dass das System neu gestartet wird, sollten Benutzer in der Lage sein, das System bei Bedarf neu zu starten.*
        -   Die APP ist nicht von 8,3-Kurzdateinamen (SFN) abhängig. *Die Installations-und Deinstallations Prozesse der APP müssen lange Dateinamen und Ordner Pfade verwenden können.*
        -   Die APP blockiert keine unbeaufsichtigte Installation/Deinstallation.
        -   Die APP macht die erforderlichen Einträge in der Systemregistrierung. *Für Windows-Inventur Tools und telemetrietools sind umfassende Informationen zu installierten apps erforderlich. App-Installationsprogramme müssen die richtigen Registrierungseinträge erstellen, um eine erfolgreiche Erkennung und deinstallieren zuzulassen.*
    -   Wenn Sie ein MSI-basiertes Installationsprogramm verwenden, erstellt MSI die unten aufgeführten Registrierungseinträge automatisch. Wenn Sie keinen MSI-Installer verwenden, muss das Installations Modul während der Installation die folgenden Registrierungseinträge erstellen:
        -   DisplayName
        -   InstallLocation
        -   Publisher
        -   UninstallString
        -   VersionMajor oder MajorVersion
        -   VersionMinor oder MinorVersion
    -   Die APP muss alle zugehörigen Einträge in "Software" entfernen.
-   Testdetails
    -   Dieser Test überprüft die Installations-und Deinstallations Vorgänge der APP auf das erforderliche Verhalten.
-   Korrekturmaßnahme
    -   Überprüfen Sie den Entwurf und das Verhalten der APP anhand der oben beschriebenen Anforderungen.

## <a name="install-to-the-correct-folders-test"></a>Installieren Sie den richtigen Ordner Test.

Mit dieser Option wird überprüft, ob die Programm-und Datendateien der app in die richtigen Ordner geschrieben werden.

-   Hintergrund
    -   Apps müssen System-und benutzerspezifische Ordner ordnungsgemäß ausführen, damit Sie auf die benötigten Daten und Einstellungen zugreifen können und gleichzeitig die Daten und Einstellungen des Benutzers vor unbefugtem Zugriff schützen.
-   Ordner "Programme"
    -   Die APP muss standardmäßig im Ordner "Programme" installiert werden (% Program Files% für native 32-Bit-und 64-Bit-apps und% Program Files (x86)% für 32-Bit-apps, die auf x64 ausgeführt werden).
    -   **Hinweis:** Aufgrund der Sicherheits Berechtigungen, die für diesen Ordner konfiguriert wurden, darf die APP keine Benutzerdaten oder App-Daten in einem Programmdatei Ordner speichern.
    -   Die ACLs in Windows-Systemordnern erlauben nur Administrator Konten, Lese-und Schreibzugriff auf diese zu erhalten. Daher haben Standardbenutzer Konten keinen Zugriff auf diese Ordner. Mit der Dateivirtualisierung können apps jedoch eine Datei (z. b. eine Konfigurationsdatei) an einem System Speicherort speichern, der in der Regel nur von Administratoren beschreibbar ist. Das Ausführen von Programmen als Standardbenutzer in dieser Situation kann zu Fehlern führen, wenn Sie nicht auf eine erforderliche Datei zugreifen können.
    -   Apps sollten [bekannte Ordner](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)) verwenden, um sicherzustellen, dass Sie auf Ihre Daten zugreifen können.
    -   **Hinweis:** Windows bietet die Dateivirtualisierung, um die APP-Kompatibilität zu verbessern und Probleme auszuschließen, wenn apps unter Windows als Standardbenutzer ausgeführt werden. Ihre APP sollte sich nicht darauf verlassen, dass die Virtualisierung in zukünftigen Versionen von Windows vorhanden ist.
-   Benutzerspezifische App-Datenordner
    -   In Installationen, die pro Computer installiert sind, darf die APP während der Installation keine benutzerspezifischen Daten schreiben. Benutzerspezifische Installationsdaten sollten nur dann geschrieben werden, wenn ein Benutzer die APP zum ersten Mal startet. Dies liegt daran, dass bei der Installation kein richtiger Benutzer Speicherort zum Speichern von Daten vorhanden ist. Versuche einer APP, das Standard Zuordnungs Verhalten auf Computer Ebene nach der Installation zu ändern, sind nicht erfolgreich. Stattdessen müssen die Standardwerte auf der Ebene einzelner Benutzer beansprucht werden, wodurch verhindert wird, dass mehrere Benutzer die Standardwerte der anderen überschreiben.
    -   Alle App-Daten, die für einen bestimmten Benutzer exklusiv sind und nicht für andere Benutzer des Computers freigegeben werden sollen, müssen in den Benutzern \\ <username> \\ AppData gespeichert werden.
    -   Alle App-Daten, die für Benutzer auf dem Computer freigegeben werden müssen, sollten innerhalb von ProgramData gespeichert werden.
-   Andere Systemordner und Registrierungsschlüssel
    -   Die APP sollte niemals direkt in das Windows-Verzeichnis und die Unterverzeichnisse schreiben. Verwenden Sie die richtigen Methoden zum Installieren von Dateien, z. b. Schriftarten oder Treibern, in diesen Verzeichnissen.
    -   Apps sollten beim Start nicht automatisch gestartet werden, z. b. durch Hinzufügen eines Eintrags zu einem oder mehreren der folgenden Speicherorte:
        -   Registrierungs Lauf Schlüssel HKLM und oder HKCU unter Software \\ Microsoft \\ Windows \\ CurrentVersion
        -   Registrierungs Lauf Schlüssel HKLM und oder HKCU unter Software \\ Wow6432Node \\ Microsoft \\ Windows \\ CurrentVersion
        -   Startmenü allprogramme > Start
-   Testdetails
    -   Mit diesem Test wird überprüft, ob die APP die spezifischen Speicherorte im Dateisystem verwendet, die Windows zum Speichern von Programmen und Softwarekomponenten, freigegebenen App-Daten und App-Daten verwendet, die für einen Benutzer spezifisch sind.
-   Maßnahmen
    -   Überprüfen Sie, wie die APP die Ordner des Systems verwendet, und stellen Sie sicher, dass Sie ordnungsgemäß verwendet wird.
-   Ausnahmen und waivers
    -   Für Desktop-Apps, die in den globalen Assemblycache (GAC) schreiben, ist ein Verzicht erforderlich (.net-apps sollten die Assemblyabhängigkeiten privat halten und im Verzeichnis der APP speichern, es sei denn, die Freigabe einer Assembly ist explizit erforderlich).
    -   Die Installation im Ordner "Programme" ist für Desktop-SW-Pakete keine Voraussetzung für das Erreichen eines SW-Logos, sondern nur in der Kategorie "SW Fundamentals".

## <a name="digitally-signed-file-test"></a>Digital signierter Dateitest

Testet ausführbare Dateien und Gerätetreiber, um sicherzustellen, dass Sie über eine gültige digitale Signatur verfügen.

-   Hintergrund
    -   Digital signierte Dateien ermöglichen es, die Datei zu überprüfen und zu ermitteln, ob die Datei manipuliert wurde.
    -   Die Kernel Modus-Code Signatur Erzwingung ist ein Windows-Feature, das auch als Code Integrität (CI) bezeichnet wird. CI verbessert die Sicherheit von Fenstern durch Überprüfen der Integrität einer Datei bei jedem Laden in den Arbeitsspeicher. CI erkennt, ob bösartiger Code eine System Binärdatei geändert hat, und generiert ein Diagnose-und System Überwachungs Protokoll-Ereignis, wenn die Signatur eines Kernel Moduls nicht korrekt überprüft werden kann.
    -   Wenn für die APP erweiterte Berechtigungen erforderlich sind, zeigt die Eingabeaufforderung für erhöhte Rechte Kontextinformationen über die ausführbare Datei an, die erhöhten Zugriff anfordert. Abhängig davon, ob die APP Authenticode signiert ist, wird dem Benutzer möglicherweise die Zustimmungsaufforderung oder die Anmeldeaufforderung angezeigt.
    -   Starke Namen verhindern, dass Drittanbieter Ihren Code Spoofing, solange Sie den privaten Schlüssel schützen. Der .NET Framework überprüft die digitale Signatur entweder beim Laden der Assembly oder bei der Installation im GAC. Ohne Zugriff auf den privaten Schlüssel kann ein böswilliger Benutzer den Code nicht ändern und ihn nicht erneut signieren.
-   Testdetails
    -   Alle ausführbaren Dateien, z. b. die Dateierweiterungen exe,. dll,. ocx,. sys,. cpl,. drv und. scr, müssen mit einem Authenticode-Zertifikat signiert werden.
    -   Alle Kernelmodustreiber, die von der APP installiert werden, müssen über das WHQL-oder DRS-Programm eine Microsoft-Signatur erhalten. Alle Dateisystem Filter-Treiber müssen mit WHQL signiert sein.
-   Korrekturmaßnahme
    -   Signieren Sie die ausführbaren Dateien der app.
    -   Verwenden Sie makecert.exe, um ein Zertifikat zu generieren oder einen Code Signatur Schlüssel von einer der kommerziellen Zertifizierungsstellen (CAS) zu erhalten, z. b. VeriSign, Thawte oder eine Microsoft-Zertifizierungsstelle.
-   Ausnahmen und Ausnahmegenehmigungen
    -   Waivers werden nur für nicht signierte Redistributables von Drittanbietern berücksichtigt. Ein Kommunikations Nachweis ist erforderlich, um eine signierte Version der verteilbaren verteilbaren Dateien anzufordern.
    -   Geräte Wert-hinzugefügte Softwarepakete sind von der Kernelmodustreiber-Zertifizierung ausgenommen, da die Treiber von der Windows-Hardware Zertifizierung zertifiziert werden müssen.

## <a name="support-x64-windows-test"></a>X64-Windows-Test unterstützen

Testen Sie die APP, um sicherzustellen, dass die exe-Datei für die Plattformarchitektur erstellt wird, auf der Sie installiert wird.

-   Hintergrund
    -   Die ausführbare Datei muss für die Prozessorarchitektur erstellt werden, auf der Sie installiert ist. Einige ausführbare Dateien können auf einer anderen Prozessorarchitektur ausgeführt werden, dies ist jedoch nicht zuverlässig.
    -   Die Architektur Kompatibilität ist wichtig, da 32-Bit-Prozesse keine 64-Bit-DLLs laden können und 64-Bit-Prozesse keine 32-Bit-DLLs laden können. Ebenso unterstützt 64-Bit-Versionen von Windows nicht das Ausführen von 16-Bit-Windows-basierten Anwendungen, da Handles 32 signifikante Bits auf 64-Bit-Windows an aufweisen, sodass Sie nicht an 16-Bit-Anwendungen weitergegeben werden können. Daher schlägt der Versuch, eine 16-Bit-Anwendung zu starten, auf 64-Bit-Versionen von Windows fehl.
    -   32-Bit-Gerätetreiber können nicht auf 64-Bit-Versionen von Windows ausgeführt werden und müssen daher in die 64-Bit-Architektur portiert werden.
    -   Für Benutzermodusanwendungen enthält 64-Bit-Windows WOW64, das die Ausführung von 32-Bit-Windows-Anwendungen auf Systemen ermöglicht, auf denen 64-Bit-Windows ausgeführt wird, wenn jedoch ein Leistungsverlust auftritt. Für Gerätetreiber ist keine äquivalente übersetzungsebene vorhanden.
    -   Um die Kompatibilität mit 64-Bit-Versionen von Windows zu gewährleisten, müssen apps 32 eine systemeigene Unterstützung für 64-Bit-und Windows-basierte Windows-basierte apps in 64 der Windows-Version unterstützen:
        -   Apps und deren Installer dürfen keinen 16-Bit-Code enthalten oder auf eine 16-Bit-Komponente zurückgreifen.
        -   Das App-Setup muss die richtigen Treiber und Komponenten auf 64-Bit-Versionen von Windows erkennen und installieren.
        -   Alle Shell-Plug-Ins müssen auf 64-Bit-Versionen von Windows ausgeführt werden.
        -   Apps, die unter dem WOW64-Emulator ausgeführt werden, sollten nicht versuchen, WOW64-Virtualisierungsmechanismen zu umgehen. Wenn es bestimmte Szenarien gibt, in denen apps erkennen müssen, ob Sie in einem WOW64-Emulator ausgeführt werden, sollten Sie dies durch Aufrufen von [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)tun.
-   Testdetails
    -   Die APP sollte keine 16-Bit-Binärdateien installieren. Die APP sollte keinen 32-Bit-Kernelmodustreiber installieren, wenn Sie auf einem 64-Bit-Computer ausgeführt werden soll.
-   Korrekturmaßnahmen
    -   Erstellen Sie die ausführbaren Dateien und Treiber für die Prozessorarchitektur, für die Sie diese installieren möchten.

## <a name="os-version-checking-test"></a>Test der OS-Versions Überprüfung

Testet, wie die APP auf die Version von Windows prüft, auf der Sie ausgeführt wird.

-   Hintergrund
    -   Apps überprüfen Sie die Betriebssystemversion, indem Sie eine Version testen, die größer oder gleich der erforderlichen Version ist, um die Kompatibilität mit zukünftigen Versionen von Windows sicherzustellen.
-   Testdetails
    -   Simuliert die Ausführung der app in verschiedenen Versionen von Windows, um zu sehen, wie Sie reagiert.
-   Maßnahmen
    -   Testen Sie die richtige Version von Windows, indem Sie testen, ob die aktuelle Version größer oder gleich der Version ist, die Ihre APP, Ihr Dienst oder Ihr Treiber benötigt.
    -   Treiber Installationsprogramme und Deinstallations Module dürfen die Betriebssystemversion niemals überprüfen.
-   Ausnahmen und waivers
    -   Für apps, die die folgenden Kriterien erfüllen, werden waivers berücksichtigt: *(gilt nur für die Desktop-App-Zertifizierung)* .
        -   Apps, die als ein Paket übermittelt werden, das unter Windows XP, Windows Vista und Windows 7 ausgeführt wird und die Betriebssystemversion überprüfen muss, um zu bestimmen, welche Komponenten auf einem bestimmten Betriebssystem installiert werden müssen.
        -   Apps, die nur die Mindestversion des Betriebssystems überprüfen (nur während der Installation, nicht zur Laufzeit), indem Sie nur die genehmigten API-Aufrufe verwenden und die Mindestanforderungen an die Version im App-Manifest nach Bedarf auflisten.
        -   Sicherheits-apps wie Antiviren-und Firewallanwendungen, System Dienstprogramme wie defragmentierungsdienstprogramme und Sicherungs-apps sowie Diagnosetools, die die Betriebssystemversion überprüfen, indem Sie nur die genehmigten API-Aufrufe verwenden.

## <a name="user-account-control-uac-test"></a>Benutzerkontensteuerung (User Account Control, UAC) Test

Testet die APP, um zu überprüfen, ob Sie unnötig erhöhte Berechtigungen zum Ausführen benötigt.

-   Hintergrund
    -   Eine APP, die nur dann ausgeführt oder installiert wird, wenn der Benutzer ein Administrator ist, zwingt die Benutzer, die APP mit unnötigerweise erhöhten Berechtigungen auszuführen, sodass die Eingabe des Benutzer Computers durch Schadsoftware zugelassen werden kann.
    -   Wenn Benutzer immer gezwungen werden, Apps mit erhöhten Zugriffs Token auszuführen, kann die APP als Einstiegspunkt für trügerischen oder bösartigen Code verwendet werden. Diese Malware kann das Betriebssystem ganz einfach ändern oder sich noch schlimmer auf andere Benutzer auswirken. Es ist nahezu unmöglich, einen Benutzer mit vollständigem Administrator Zugriff zu steuern, da Administratoren apps installieren und Apps oder Skripts auf dem Computer ausführen können. IT-Manager suchen immer nach Methoden zum Erstellen von "Standard-Desktops", bei denen sich Benutzer als Standardbenutzer anmelden. Standard Desktops verringern die Helpdeskkosten erheblich und reduzieren den IT-Aufwand.
    -   Bei den meisten Anwendungen sind zur Laufzeit keine Administratorrechte erforderlich. Ein Standardbenutzer Konto sollte in der Lage sein, diese auszuführen. Windows-apps müssen ein Manifest (eingebettet oder extern) aufweisen, um die Ausführungs Ebene zu definieren, die dem Betriebssystem die Berechtigungen angibt, die zum Ausführen der APP erforderlich sind. Das App-Manifest gilt nur für exe-Dateien, nicht für DLL-Dateien. Die Benutzerkontensteuerung (User Account Control, UAC) überprüft DLLs während der Prozesserstellung nicht. UAC-Regeln gelten nicht für Microsoft-Dienste. Das App-Manifest kann eingebettet oder extern sein.
    -   Um ein Manifest zu erstellen, erstellen Sie eine Datei mit dem Namen <APP \_ -Name # C1.exe. Manifest, und speichern Sie Sie im selben Verzeichnis wie die exe-Datei. Beachten Sie, dass alle externen Manifeste ignoriert werden, wenn die APP über ein internes Manifest verfügt.
        -   Beispielsweise <requestedExecutionLevel Level = "" asInvoker \| highestAvailable \| requilministrator "" UIAccess = "true \| false" "/>
        -   Der Hauptprozess der APP muss als Standardbenutzer (**asInvoker**) ausgeführt werden. Alle administrativen Funktionen müssen in einen separaten Prozess verschoben werden, der mit Administratorrechten ausgeführt wird.
        -   Benutzer seitige apps, für die erhöhte Rechte erforderlich sind, müssen mit Authenticode signiert sein.
-   Testdetails
    -   Alle Benutzer mit exe müssen mit dem asInvoker-Attribut markiert werden. Wenn Sie als highestAvailable oder requilesministrator gekennzeichnet sind, sollten Sie ordnungsgemäß mit Authenticode signiert werden. Für jede APP-exe sollte das UIAccess-Attribut nicht auf "true" festgelegt sein. Alle exe-Informationen, die als Dienst ausgeführt werden, werden von dieser speziellen Überprüfung ausgeschlossen.
-   Maßnahmen
    -   Überprüfen Sie die Manifest-Datei der APP auf die richtigen Einträge und Berechtigungsstufen.
-   Ausnahmen und Ausnahmegenehmigungen
    -   Für apps, die ihren Hauptprozess mit erweiterten Berechtigungen ausführen (**requilministrator** oder **highestAvailable**), ist ein Verzicht erforderlich. Der Hauptprozess ist der Prozess, der den Einstiegspunkt des Benutzers für die APP bereitstellt.
    -   Waivers werden für die folgenden Szenarien berücksichtigt:
        -   Verwaltungs-oder System Tools mit der Ausführungs Ebene, die auf **highestAvailable**, **requilministrator** oder beides festgelegt ist.
        -   Nur die Barrierefreiheit oder die Benutzeroberflächenautomatisierungs-Framework-App legt das UIAccess-Flag auf "true" fest, um die Benutzeroberflächen Berechtigungs Isolation (UIPI Zum ordnungsgemäßen Starten der APP-Nutzung muss dieses Flag mit Authenticode signiert sein, und es muss sich an einem geschützten Speicherort im Dateisystem befinden, z. b. in Programmdateien.

## <a name="adhere-to-system-restart-manager-messages"></a>Nachrichten des Systemneustart-Managers einhalten

Testet, wie die APP auf das Herunterfahren und Neustarten von Nachrichten reagiert.

-   Hintergrund
    -   Apps müssen so schnell wie möglich beendet werden, wenn Sie benachrichtigt werden, dass das System heruntergefahren wird, um für den Benutzer ein reaktionsfähiges Herunterfahren oder ausschalten zu bieten.
    -   Bei einem kritischen Herunterfahren werden apps, die für [**WM \_ queryendsession**](/windows/desktop/Shutdown/wm-queryendsession) den Wert "false" zurückgeben, mit " **WM \_ EndSession** " und "Closed" gesendet, während diejenigen, die als Reaktion auf WM- \_ queryendsession als Timeout gelten, erzwungen werden
-   Testdetails
    -   Untersucht, wie die APP auf Herunterfahren und Beenden von Nachrichten reagiert.
-   Maßnahmen
    -   Wenn Ihre APP diesen Test nicht bestanden hat, überprüfen Sie, wie diese Windows-Meldungen verarbeitet werden:
        -   [**WM \_ Queryendsession**](/windows/desktop/Shutdown/wm-queryendsession) mit *LPARAM*  =  **EndSession \_ CloseApp**(0x1): Desktop-Apps müssen sofort bei der Vorbereitung eines Neustarts Antworten (true). Konsolen-Apps können [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) aufrufen, um die Benachrichtigung zum Herunterfahren zu empfangen. Dienste können [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) aufrufen, um Benachrichtigungen zum Herunterfahren in einer Handlerroutine zu empfangen.
        -   [**WM \_ EndSession**](/windows/desktop/Shutdown/wm-queryendsession) mit *LPARAM*  =  **EndSession \_ CloseApp**(0x1): apps müssen einen Wert von 0 innerhalb von 30 Sekunden zurückgeben und heruntergefahren werden. Apps sollten mindestens vorbereitet werden, indem Sie alle Benutzerdaten speichern und die Informationen angeben, die nach einem Neustart benötigt werden.
    -   Konsolen-apps, die die **STRG \_ C- \_ Ereignis** Benachrichtigung empfangen, sollten sofort heruntergefahren werden. Treiber dürfen kein Veto gegen ein System Shutdown-Ereignis haben.
    -   **Hinweis:** Apps, die das Herunterfahren aufgrund eines Vorgangs blockieren müssen, der nicht unterbrochen werden kann, sollten [**shutdownblockreasoncreate**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasoncreate) verwenden, um eine Zeichenfolge zu registrieren, die den Grund für den Benutzer erläutert. Nachdem der Vorgang abgeschlossen wurde, sollte die APP [**shutdownblockreasondestroy**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasondestroy) anrufen, um anzugeben, dass das System heruntergefahren werden kann.

## <a name="safe-mode-test"></a>Test im abgesicherten Modus

Testet, ob der Treiber oder der Dienst für den Start im abgesicherten Modus konfiguriert ist.

-   Hintergrund
    -   Der abgesicherte Modus ermöglicht es Benutzern, Probleme mit Windows zu diagnostizieren und zu beheben. Nur Treiber und Dienste, die für den grundlegenden Betrieb des Betriebssystems erforderlich sind oder Diagnose-und Wiederherstellungs Dienste bereitstellen, sollten im abgesicherten Modus geladen werden. Wenn andere Dateien im abgesicherten Modus geladen werden, ist es schwieriger, Probleme mit dem Betriebssystem zu beheben.
    -   Standardmäßig werden nur die Treiber und Dienste, die mit Windows vorinstalliert sind, im abgesicherten Modus gestartet. Alle anderen Treiber und Dienste sollten deaktiviert werden, es sei denn, das System erfordert Sie für grundlegende Vorgänge oder für Diagnose-und Wiederherstellungs Zwecke.
-   Testdetails
    -   Treiber, die von der APP installiert werden, sollten nicht zum Laden im abgesicherten Modus markiert werden.
-   Maßnahmen
    -   Wenn der Treiber oder der Dienst nicht im abgesicherten Modus gestartet werden soll, entfernen Sie die Einträge der APP aus den Registrierungs Schlüsseln.
-   Ausnahmen und Ausnahmegenehmigungen
    -   Treiber und Dienste, die im abgesicherten Modus gestartet werden müssen, erfordern eine Zertifizierung. Die Anforderung zum Anfordern von Anforderungen muss alle Treiber und Dienste enthalten, die den Registrierungs Schlüsseln SafeBoot hinzugefügt werden sollen. Außerdem werden die technischen Gründe beschrieben, warum der Treiber oder der Dienst im abgesicherten Modus ausgeführt werden muss. Der APP-Installer muss alle Treiber und Dienste in diesen Registrierungs Schlüsseln registrieren:
        -   HKLM/System/CurrentControlSet/Control/SafeBoot/minimal
        -   HKLM/System/CurrentControlSet/Control/SafeBoot/Network
-   **Hinweis:** Sie müssen die Treiber und Dienste, die Sie im abgesicherten Modus starten möchten, testen, um sicherzustellen, dass Sie ohne Fehler im abgesicherten Modus funktionieren.

## <a name="multiuser-session-test"></a>Test der mehr Benutzersitzung

Testen Sie, wie sich die APP verhält, wenn Sie in mehreren Sitzungen gleichzeitig ausgeführt wird.

-   Hintergrund
    -   Windows-Benutzer müssen in der Lage sein, gleichzeitige Sitzungen auszuführen. Apps müssen sicherstellen, dass die normale Funktionalität der APP nicht beeinträchtigt wird, wenn Sie in mehreren Sitzungen entweder lokal oder Remote ausgeführt werden. App-Einstellungen und Datendateien müssen Benutzer spezifisch sein, und der Datenschutz und die Einstellungen des Benutzers müssen auf die Sitzung des Benutzers beschränkt sein.
-   Testdetails
    -   Führt mehrere gleichzeitige Instanzen der APP aus, um Folgendes zu testen:
        -   Mehrere Instanzen einer APP, die gleichzeitig ausgeführt werden, sind voneinander isoliert.
    -   Dies bedeutet, dass Benutzerdaten aus einer Instanz nicht für eine andere Instanz sichtbar sind. Sound in einer inaktiven Benutzersitzung sollte nicht in einer aktiven Benutzersitzung gehört werden. In Fällen, in denen mehrere App-Instanzen freigegebene Ressourcen verwenden, muss die APP sicherstellen, dass kein Konflikt vorliegt.
        -   Wenn die APP für mehrere Benutzer installiert wurde, werden die Daten in den richtigen Ordnern und Registrierungs Speicherorten gespeichert.
        -   Die APP kann in mehreren Benutzersitzungen (schnelle Benutzerumschaltung) sowohl für den lokalen als auch für den Remote Zugriff ausgeführt werden.
    -   Um dies zu gewährleisten, muss die APP andere Terminaldienst Sitzungen (TS) für vorhandene Instanzen der APP überprüfen. Wenn die APP nicht mehrere Benutzersitzungen oder den Remote Zugriff unterstützt, muss Sie dem Benutzer klar gesagt werden, wenn er in einer solchen Sitzung gestartet wird.
-   Korrekturmaßnahme
    -   Stellen Sie sicher, dass die APP keine systemweiten Datendateien oder-Einstellungen in benutzerspezifischen Daten speichern speichert, wie z. b. Benutzer Profile oder HKCU. Wenn dies der Fall ist, werden diese Informationen anderen Benutzern nicht zur Verfügung gestellt.
    -   Ihre APP muss bei der Installation systemweite Konfigurations-und Datendateien installieren und die benutzerspezifischen Dateien und Einstellungen nach der Installation erstellen, wenn Sie von einem Benutzer ausgeführt wird.
    -   Stellen Sie sicher, dass die APP nicht mehrere gleichzeitige Sitzungen blockiert (entweder lokal oder Remote). Die APP darf nicht von globalen Mutexen oder anderen benannten Objekten abhängig sein, um mehrere gleichzeitige Sitzungen zu überprüfen oder zu blockieren.
    -   Wenn die APP mehrere gleichzeitige Sitzungen pro Benutzer nicht zulassen kann, verwenden Sie benutzerspezifische oder Sitzungs spezifische Namespaces für Mutexen und andere benannte Objekte.

## <a name="crashes-and-hangs-test"></a>Abstürze und Abstürze-Test

Überwachen die App während des Zertifizierungstests, um aufzuzeichnen, wann sie abstürzt oder sich aufhängt.

-   Hintergrund
    -   App-Fehler, wie z. b. Abstürze und Abstürze, sind eine wesentliche Unterbrechung der Benutzer und verursachen Frustration Wenn solche Fehler vermieden werden, verbessert sich die APP-Stabilität und-Zuverlässigkeit und bietet Benutzern eine bessere App-Benutzer Leistung. Apps, die nicht mehr reagieren oder abstürzen, können zu einem Datenverlust und zu einer Beeinträchtigung des Benutzererlebnisses führen.
-   Testdetails
    -   Die App wird beim Zertifizierungstest durchgehend auf Flexibilität und Stabilität geprüft.
    -   Das Windows-zertifizierungskit für apps ruft [**iapplicationactivationmanager:: activateapplication**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication) auf, um Windows Store-Apps zu starten. Damit eine App mit **ActivateApplication** gestartet werden kann, muss die Benutzerkontensteuerung (UAC) aktiviert sein und die Bildschirmauflösung mindestens 1024 x 768 oder 768 x 1024 betragen. Ist eine dieser Bedingungen nicht erfüllt, fällt die App bei diesem Test durch.
-   Korrekturmaßnahmen
    -   Stellen Sie sicher, dass die Benutzerkontensteuerung (UAC) auf dem Test-PC aktiviert ist.
    -   Führen Sie den Test auf einem PC mit ausreichend großem Bildschirm aus.
    -   Falls die App nicht gestartet werden kann, obwohl die Testplattform die Voraussetzungen für [**ActivateApplication**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication) erfüllt, können Sie das Problem mithilfe des Aktivierungsereignisprotokolls beheben. So finden Sie die Einträge im Ereignisprotokoll:
        1.  Öffnen Sie eventvwr.exe, und navigieren Sie zum \\ Anwendungs Knoten "Windows-Protokolle" \\ .
        2.  Filtern Sie die Ansicht entsprechend, um folgende Ereigniskennungen anzuzeigen: 5900-6000.
        3.  Prüfen Sie die Protokolleinträge, um zu ermitteln, weshalb die App nicht gestartet wurde.
    -   Führen Sie für die Datei mit dem Problem eine Problembehandlung durch, um das Problem zu identifizieren und zu beheben. Erstellen Sie die App neu, und wiederholen Sie den Test.
-   Zusätzliche Ressourcen
    -   [Verwenden von Application Verifier während des Lebenszyklus der Software Entwicklung](https://blogs.msdn.com/b/ntdebugging/archive/2014/01/13/debugging-a-windows-8-1-store-app-crash-dump.aspx)
    -   [Application Verifier]( https://go.microsoft.com/fwlink/p/?LinkId=708300)
    -   [Verwenden von Application Verifier](https://www.microsoft.com/?ref=go)
    -   [AppInit-DLLs](https://www.microsoft.com/?ref=go)
    -   [Minimieren der Startzeit (Windows Store-Apps mit C#/VB/C++ und XAML)](/previous-versions/windows/apps/hh994639(v=win.10))

## <a name="compatibility-and-resiliency-test"></a>Kompatibilitäts-und resilienztest

-   Hintergrund
    -   Durch diese Überprüfung werden zwei Aspekte einer APP überprüft, die ausführbaren Anwendungs Hauptdateien, z. b., dass sich der Benutzer mit dem App-Einstiegspunkt aus Kompatibilitätsgründen und die richtige GUID deklarieren müssen. Um diesen neuen Test zu unterstützen, weist der Bericht einen untergeordneten Knoten unter ' Kompatibilität & Resilienz ' auf. Die APP schlägt fehl, wenn eine oder beide dieser Bedingungen fehlen.
-   Testdetails
    -   **Kompatibilität:** Apps müssen voll funktionsfähig sein, ohne Windows-Kompatibilitäts Modi, AppHelp-Nachrichten oder andere Kompatibilitäts Korrekturen zu verwenden. Mithilfe eines Kompatibilitäts Manifests kann Windows der APP das richtige Kompatibilitäts Verhalten unter den verschiedenen Versionen des Betriebssystems bereitstellen.
    -   **AppInit:** Apps dürfen keine DLLs auflisten, die in den HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows \\ AppInit \_ DLLs-Registrierungsschlüssel geladen werden.
    -   **Switchback:** Die Anwendung muss das switchbackmanifest bereitstellen. Wenn das Manifest fehlt, gibt das Windows-zertifizierungskit für apps eine Warnmeldung aus. Das Windows-zertifizierungskit für Apps überprüft auch, ob das Manifest eine gültige Betriebssystem-gu
-   Maßnahmen
    -   Korrigieren Sie die Komponente der APP, die den Kompatibilitäts Fix verwendet.
    -   Stellen Sie sicher, dass die APP nicht auf Kompatibilitäts Korrekturen für ihre Funktionalität angewiesen ist.
    -   Stellen Sie sicher, dass Ihre APP angezeigt wird und der Kompatibilitäts Abschnitt die entsprechenden Werte enthält.
-   Zusätzliche Informationen
    -   Weitere Informationen finden Sie unter [AppInit-DLLs](/previous-versions/windows/apps/hh994639(v=win.10)) .

## <a name="windows-security-best-practices-test"></a>Bewährte Windows-Sicherheitsmethoden testen

-   Hintergrund
    -   Eine APP sollte nicht die standardmäßigen Windows-Sicherheitseinstellungen ändern.
-   Testdetails
    -   Testet die Sicherheit der app durch Ausführen der Angriffsfläche Analyzer. Der Ansatz besteht darin, Fehlerkategorien pro Test hinzuzufügen. Beispielsweise können einige Kategorien für den Sicherheitstest Folgendes umfassen:
        -   Initialisierungsfehler
        -   Fehler bei der Sicherheitsarchitektur
        -   Möglicher Pufferüberlauf Fehler
        -   Absturzfehler
    -   Weitere Informationen finden Sie [hier](/previous-versions/windows/hh920280(v=win.10)).
-   Maßnahmen
    -   Beheben Sie das durch die Tests identifizierte Problem, und beheben Sie es. Erstellen Sie die App neu, und wiederholen Sie den Test.

## <a name="windows-security-features-test"></a>Test der Windows-Sicherheitsfeatures

-   Hintergrund
    -   Anwendungen müssen die Windows-Sicherheitsfeatures ablehnen. Durch Ändern der standardmäßigen Windows-Sicherheitsvorkehrungen können Kunden einem erhöhten Risiko ausgesetzt werden.
-   Testdetails
    -   Testet die Sicherheit der App durch Ausführen des BinScope Binary Analyzers. Weitere Informationen finden Sie [hier](/previous-versions/windows/hh920280(v=win.10)).
-   Maßnahmen
    -   Beheben Sie das durch die Tests identifizierte Problem, und beheben Sie es. Erstellen Sie die App neu, und wiederholen Sie den Test.

## <a name="high-dpi-test"></a>Hoher dpi-Test

Es wird dringend empfohlen, dass die Win32-apps dpi-fähig sind. Der Schlüssel ist der Schlüssel, mit dem die Benutzeroberfläche der APP über eine Vielzahl von Anzeigeeinstellungen mit hoher dpi hinweg konsistent aussehen kann. Bei einer nicht-dpi-fähigen APP, die mit einer Einstellung mit hoher dpi-Anzeige ausgeführt wird, treten möglicherweise Probleme auf, wie z. b. falsche Skalierung von Benutzeroberflächen Elementen, ausgeschnittenen Text Es gibt zwei Möglichkeiten, eine APP zu deklarieren, die dpi-fähig ist. Eine besteht darin, dpi zu deklarieren.

-   Hintergrund
    -   Durch diese Überprüfung werden zwei Aspekte einer APP überprüft, d. h. die Haupt ausführbaren Dateien, z. b. Benutzer seitige App-Einstiegspunkte müssen für hochauflösende Informationen angezeigt werden, und dass die richtigen APIs aufgerufen werden, um High-dpi zu unterstützen. Die APP schlägt fehl, wenn eine oder beide dieser Bedingungen fehlen. Mit dieser Überprüfung wird ein neuer Abschnitt im Desktop Bericht eingeführt, siehe Beispiel unten.
-   Testdetails
    -   Der Test generiert eine Warnung, wenn Folgendes erkannt wird:
        -   Die Haupt-exe deklariert nicht das dpi-Bewusstsein im Manifest und ruft keine SetProcessDPIAware-API auf. (Warnen Sie den Entwickler, wenn er vergisst, das dpi-Manifest hinzuzufügen).
        -   Die Haupt-exe deklariert nicht das dpi-Bewusstsein im Manifest, sondern ruft die SetProcessDPIAware-API auf (warnen Sie den Entwickler, dass er das Manifest verwenden soll, um die dpi-Informationen zu deklarieren, anstatt die API aufzurufen)
        -   Die mainexe deklariert das dpi-Bewusstsein im Manifest, ruft aber auch die SetProcessDPIAware-API auf (warnen Sie den Entwickler, dass diese API nicht erforderlich ist).
        -   Bei den Binärdateien, bei denen es sich nicht um Haupt-exe handelt, sollte eine Warnung ausgegeben werden, wenn Sie die API aufrufen (das Aufrufen der API wird nicht empfohlen).
-   Maßnahmen
    -   Die Verwendung der SetProcessDPIAware ()-Funktion ist nicht empfehlenswert. Wenn eine DLL dpi-Einstellungen während der Initialisierung zwischenspeichert, wird durch das Aufrufen von SetProcessDPIAware () in der APP möglicherweise eine Racebedingung generiert. Das Aufrufen der SetProcessDPIAware ()-Funktion in einer dll ist entweder nicht empfehlenswert.
-   Zusätzliche Informationen
    -   [Schreiben von High-dpi-apps](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))

 

 