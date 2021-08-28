---
title: Neuigkeiten (BITS)
description: In der folgenden Tabelle sind die Neuen für jedes Release von Background Intelligent Transfer Service (BITS) aufgeführt.
ms.assetid: ef05f2e1-88be-4adb-aca7-a7b1451cfd04
keywords:
- What es new BITS (What es new BITS)
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: 17bd6ececccc1ae36cf9774b41cb151a3aaee8a4ea687474c516e10589d49383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701620"
---
# <a name="whats-new-bits"></a>Neuigkeiten (BITS)

Seit dem ersten Release als Teil von Windows XP wurde das Background Intelligent Transfer Service (BITS) ständig verbessert, und entwickler und administrator haben leistungsfähigere Steuerelemente zum Steuern und Verwalten von Downloads hinzugefügt. Ein umfangreiches Set von PowerShell-Cmdlets wurde hinzugefügt. es kann eine Verbindung mit mehr Typen von HTTP-Servern herstellen. sie ist mit der Netzwerkbandbreite und den Kosten des Benutzers vorsichtiger als je zuvor. 

In der folgenden Tabelle sind die Neuen für jedes Release von Background Intelligent Transfer Service (BITS) aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Version</th>
<th>Beschreibung der Features</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Version 10.3</td>
<td>Neue Funktionen:<br/>
<ul>
<li><a href="/windows/win32/api/bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3"><strong>BackgroundCopyJobHttpOptions3 wurde hinzugefügt,</strong></a> um HTTP-Header als only write-only zu markieren und einen Rückruf zur Überprüfung des Serverzertifikats zu setzen.</li>
<li>BITS behält seine Dienstidentität bei, wenn es von einem anderen Systemdienst erstellt wird.</li>
<li>BITS überträgt weiterhin Dateien im verbundenen Standbymodus, solange das Gerät angeschlossen ist.</li>
</ul>
DIE BITS-Version 10.3 ist im Windows 10 May 2019 Update (10.0; Build 18362) und höher.
</td>
</tr>
<tr class="even">
<td>Version 10.2</td>
<td>Neue Funktionen:<br/>
<ul>
<li><a href="/windows/win32/api/bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2"><strong>BackgroundCopyJobHttpOptions2 wurde hinzugefügt, um</strong></a> die HTTP-Methode für HTTP-Downloads zu ändern.</li>
<li>BITS verwendet jetzt die Standardproxy reihenfolge, um mit dem Rest des Systems konsistenter zu sein.</li>
<li>Programmierer können die BITS-Proxykonfiguration für Unternehmensszenarien einfacher festlegen.</li>
<li>BITS ist nun vorsichtiger bei der Stromversorgung und unterstützt [modernen Standbymodus.](/windows-hardware/design/device-experiences/modern-standby)</li>
<li>BITS unterstützt jetzt zusätzlich zu [](/windows/client-management/mdm/policy-configuration-service-provider) Gruppenrichtlinien auch MDM-Richtlinien (Mobile Device [Manager).](./group-policies)</li>
</ul>
BITS Version 10.2 ist in Windows 10 October 2018 Update(10.0; Build 17763) und höher.
</td>
</tr>
<tr class="odd">
<td>Version 10.1</td>
<td>Neue Funktionen:<br/>
<ul>
<li><a href="/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6"><strong>BackgroundCopyFile6 und</strong></a> <a href="/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3"><strong>IBackgroundCopyCallback3</strong></a> wurden hinzugefügt, um Szenarien mit zufälligem Zugriff für HTTP-Downloads zu ermöglichen.</li>
<li>Der <strong>BITS_JOB_PROPERTY_ON_DEMAND_MODE</strong> und <strong>BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS</strong> der BITS_JOB_PROPERTY_ID <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong></strong></a> hinzugefügt, um das Download- bzw. Benachrichtigungsverhalten zu optimieren.</li>
</ul>
BITS Version 10.1 ist in Windows 10 Creator es Update und höher enthalten.
</td>
</tr>
<tr class="even">
<td>Version 5.0</td>
<td>Neue Funktionen:<br/>
<ul>
<li>Die <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5-Schnittstelle</strong></a> wurde hinzugefügt, die generische Methoden zum Abrufen und Festlegen von BITS-Auftragseigenschaften zu den Methoden hinzufügt, die von der <a href="/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4"><strong>IBackgroundCopyJob4-Schnittstelle geerbt</strong></a> wurden.<br/> Informationen zur Verwendung der neuen <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5-Schnittstelle</strong></a> finden Sie unter How to control whether a BITS job is allowed to download <a href="how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md">over an expensive connection</a> (Steuern, ob ein BITS-Auftrag über eine teure Verbindung heruntergeladen werden darf) und How to get the last set of <a href="how-to-get-the-last-set-of-http-headers-received-for-each-file-in-a-bits-download-job.md">HTTP headers</a>received for each file in a BITS download job (So erhalten Sie den letzten Satz von HTTP-Headern, die für jede Datei in einem BITS-Downloadauftrag empfangen wurden).<br/></li>
<li>Die <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_job_property_value"><strong>-BITS_JOB_PROPERTY_VALUE</strong></a> und <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>die</strong></a>BITS_JOB_PROPERTY_ID <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_transfer_policy"><strong>und</strong></a> BITS_JOB_TRANSFER_POLICY hinzugefügt. Verwendungsbeispiele finden Sie in den obigen Themen zur Verwendung.</li>
<li>Die <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5-Schnittstelle</strong></a> wurde hinzugefügt, die Methoden zum Abrufen und Festlegen generischer Eigenschaften für BackgroundCopyFile-Objekte zu den Methoden hinzufügt, die von der <a href="/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4"><strong>IBackgroundCopyFile4-Schnittstelle geerbt</strong></a> wurden. Durch das Addition generischer Eigenschaften können Die BackgroundCopyFile-Funktionen in Zukunft verbessert werden, ohne dass eine neue Schnittstelle erstellt werden muss.</li>
<li>Die erste generische Eigenschaft, die <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>von IBackgroundCopyFile5 verfügbar</strong></a> gemacht wird, ist die <strong>HttpResponseHeaders-Eigenschaft.</strong></li>
<li>Die <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value"><strong>-BITS_FILE_PROPERTY_VALUE</strong></a> und die <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_file_property_id"><strong>BITS_FILE_PROPERTY_ID-Enumeration</strong></a> wurden hinzugefügt.</li>
</ul>
Bits Version 5.0 ist in den Betriebssystemen Windows Server 2012 und Windows 8 enthalten, wobei die Version von %windir%\System32\QMgr.dll &quot; 7.7.xxxx.xxxx &quot; ist.<br/> Die folgenden Features wurden BITS in Windows 10<br/>
<ul>
<li>In Windows 10 Version 1607 ist es möglich, die BITS-COM-APIs und BITS-PowerShell-Cmdlets (sofern verfügbar) in einer PowerShell-Remotesitzung zu verwenden. Dies ist besonders nützlich, wenn Sie Versionen von Windows Server 2016 verwalten, die keine lokale Anmeldefunktion haben. Über PowerShell-Remotesitzungen gestartete BITS-Aufträge werden im Benutzerkontokontext der Sitzung ausgeführt und machen nur Fortschritte, wenn diesem Benutzerkonto mindestens eine aktive lokale Anmeldesitzung oder PowerShell-Remotesitzung zugeordnet ist. Ziehen Sie die Verwendung persistenter PowerShell-Remotesitzungen (siehe <a href="/powershell/module/microsoft.powershell.core/new-pssession">New-PSSession)</a>für Übertragungen mit langer Ausführungsausführung in Betracht.</li>
<li>In Windows 10 Version 1607 ist es nun möglich, dass ein BITS-Auftragsbesitzer Hilfstoken ohne Administratorrechte festgelegt, solange das Hilfstoken nicht über Administratorfunktionen verfügt. Dadurch werden Sicherheitsrisiken von Tools für Hintergrunddownloads oder -aktualisierungen gemindert, da diese Tools nicht unter einem Konto mit Administratorrechten, sondern unter dem NetworkService-Konto mit niedrigeren Berechtigungen ausgeführt werden.</li>
</ul>
Bits Version 5.0 ist auch in Windows 10 enthalten, wobei die Version von %windir%\System32\QMgr.dll &quot; 7.8.xxxx.xxxx &quot; ist.<br/></td>
</tr>
<tr class="odd">
<td>Version 4.0</td>
<td>Neue Funktionen:<br/>
<ul>
<li>Die Peerzwischenspeicherung verwendet jetzt Windows BranchCache. Dieses neue Peercachingmodell ersetzt das Für BITS-Version 3.0 verwendete Modell. Weitere Informationen finden Sie unter <a href="peer-caching.md">Peercaching.</a></li>
<li>Ein flexibleres Ressourcenzugriffsmodell wurde hinzugefügt, mit dem Anwendungen einem BITS-Übertragungsauftrag ein Sicherheitstokenpaar zuordnen können. Weitere Informationen finden Sie unter <a href="helper-tokens-for-bits-transfer-jobs.md">Hilfstoken für BITS-Übertragungsaufträge.</a></li>
<li>Bits <a href="bits-compact-server.md">Compact Server</a>wurde hinzugefügt. Dabei handelt es sich um einen eigenständigen HTTP/HTTPS-Dateiserver, der die Möglichkeit bietet, eine begrenzte Anzahl großer Dateien asynchron zwischen Computern zu übertragen.</li>
<li>Eine präzisere Bandbreitendrosselung wurde hinzugefügt. Weitere Informationen finden Sie unter <a href="group-policies.md">Gruppenrichtlinien.</a></li>
</ul>
BITS Version 4.0 ist in den Betriebssystemen Windows Server 2008 R2 und Windows 7 enthalten.<br/> Sie können auch BITS 4.0 für Windows Server 2008 mit Service Pack 2 (SP2), Windows Vista mit Service Pack 1 (SP1) und Windows Vista mit Service Pack 2 (SP2) herunterladen. Informationen zum Herunterladen von BITS 4.0 finden Sie unter <a href="https://support.microsoft.com/kb/968929">KB968929</a>.<br/> Die Version von %windir%\System32\QMgr.dll &quot; ist 7.5.xxxx.xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Version 3.0</td>
<td>Neue Funktionen:<br/>
<ul>
<li>Die <a href="peer-caching.md">Peerzwischenspeicherung</a> wurde hinzugefügt, mit der Sie Inhalte von Peers herunterladen und inhalte auch peers in einem Domänennetzwerk zur Verfügung haben.</li>
<li>Benachrichtigung <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred">für</a> den Download einer Datei hinzugefügt.</li>
<li>Zugriff auf die temporäre <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname">Datei wurde hinzugefügt,</a> während der Download läuft.</li>
<li>Die Möglichkeit zum Steuern von HTTP-Umleitungen <a href="/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags">wurde hinzugefügt.</a></li>
<li>Es wurden weitere <a href="group-policies.md">Gruppenrichtlinien hinzugefügt,</a> um die Peerzwischenspeicherung zu steuern und die Downloadzeiten zu begrenzen.</li>
<li>Dem Systemereignisprotokoll wurden Diagnose- und Problembehandlungsereignisse hinzugefügt.</li>
<li>Unterstützung für die Benutzerkontensteuerung (User <a href="user-account-control-and-bits.md">Account Control,</a> UAC) wurde hinzugefügt.</li>
<li>Bei Windows Vista und höher wird der standardmäßige BITS-Starttyp verzögert automatisch gestartet.</li>
</ul>
<blockquote>
[!Note]<br />
BITS verwendet jetzt Gruppenrichtlinien, um die Anzahl von Aufträgen und Dateien zu begrenzen, die Sie erstellen können. Dies kann sich auf Anwendungen auswirken, die derzeit eine große Anzahl von Aufträgen erstellen oder einem Auftrag eine große Anzahl von Dateien hinzufügen.
</blockquote>
<br/> <br/> BITS Version 3.0 ist in den Betriebssystemen Windows Server 2008 und Windows Vista enthalten. <br/> Die Version von %windir%\System32\QMgr.dll &quot; ist 7.0.xxxx.xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Version 2.5</td>
<td>Unterstützung für benutzerdefinierte HTTP-Header, zertifikatbasierte Clientauthentifizierung für sichere HTTP-Transporte und IPv6 wurde hinzugefügt. Außerdem wurde die Verwendung von IGD-Leistungsindikatoren (Internet Gateway Device) hinzugefügt, um die verfügbare Bandbreite genauer zu <a href="network-bandwidth.md">berechnen.</a><br/> Die BITS 2.5-Features sind in den Betriebssystemen Windows Server 2008, Windows Vista und Windows XP mit Service Pack 3 (SP3) verfügbar. <br/> Sie können auch BITS 2.5 für Windows Server 2003 mit Service Pack 2 (SP2), Windows Server 2003 mit Service Pack 1 (SP1) und Windows XP mit Service Pack 2 (SP2) herunterladen. Um BITS 2.5 herunterzuladen, wechseln Sie zum <a href="https://www.microsoft.com/download/details.aspx?id=4933">Microsoft Download Center,</a> und installieren Sie KB923845.<br/> Die Version von %windir%\System32\QMgr.dll &quot; ist 6.7.xxxx.xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Version 2.0</td>
<td>Unterstützung für gleichzeitige Vordergrunddownloads, die Verwendung von Server Message Block-Pfaden (SMB) für Remotenamen, das Herunterladen von Bereichen einer Datei, das Ändern des Präfix oder vollständigen Namens eines Remotenamens und das Einschränken der Clientbandbreitennutzung wurde hinzugefügt. Die JobInactivityTimeout-Richtlinie befindet sich jetzt unter Computerkonfiguration, Administrative Vorlagen, Netzwerk, Background Intelligent Transfer Service (BITS).<br/> BITS Version 2.0 ist in Windows XP mit SP2 und Windows Server 2003 mit SP1 enthalten. Sie können auch BITS 2.0 für Windows Server 2003 und Windows XP herunterladen. Um BITS 2.0 herunterzuladen, wechseln Sie zum <a href="https://www.microsoft.com/download/details.aspx?id=19031">Microsoft Download Center,</a> und installieren Sie KB842773.<br/> Die Version von %windir%\System32\QMgr.dll ist &quot; 6.6.xxxx.xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Version 1.5</td>
<td>Die Upload- und Upload-Antwort-Funktion, die Befehlszeilenausführung für Ereignisse sowie explizite Anmeldeinformationen und Proxyanmeldeinformationen wurden hinzugefügt.<br/> Ab BITS 1.5 können Benutzer mit einem eingeschränkten <a href="/windows/win32/secauthz/restricted-tokens">Token</a> keine Aufträge erstellen oder ändern.<br/> Bits Version 1.5 ist in Windows Server 2003 enthalten. Eine verteilbare ist für Windows XP im <a href="https://www.microsoft.com/download/details.aspx?id=22250">Microsoft Download Center verfügbar.</a><br/> Die Version von %windir%\System32\QMgr.dll &quot; ist 6.5.xxxx.xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Version 1.2</td>
<td>Gleiche Funktionalität wie Version 1.0. Enthält interne Upgrades und Verbesserungen.<br/> BITS Version 1.2 ist in Windows XP mit Service Pack 1 (SP1) enthalten.<br/> Die Version von %windir%\System32\QMgr.dll &quot; ist 6.2.xxxx.xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Version 1.0</td>
<td>Erste Veröffentlichung Stellt priorisierte, gedrosselte und asynchrone Downloads im Hintergrund oder Vordergrund bereit. Die Downloads werden automatisch fortgesetzt, nachdem der Computer neu gestartet und das Netzwerk getrennt wurde.<br/> BITS Version 1.0 ist in xp Windows enthalten.<br/> Die Version von %windir%\System32\QMgr.dll &quot; ist 6.0.xxxx.xxxx &quot; .<br/></td>
</tr>
</tbody>
</table>

Um Features in Ihrem Programm basierend auf BITS-Funktionen zu belichten, verwenden Sie QueryInterface für (z. B. ) Ihr Job-Objekt, um zu sehen, ob sie mit dem Job-Objekt die version erstellen können, die Sie benötigen. Alternativ finden Sie weitere Informationen unter [Determining the Version of BITS on a Computer](./determining-the-version-of-bits-on-a-computer.md) (Bestimmen der Bits-Version auf einem Computer), um QMgr.dll Versionsnummer in die BITS-Version zu konvertieren.

## <a name="version-103"></a>Version 10.3

Die folgenden Schnittstellen wurden für diese Version hinzugefügt.
-   [**IBackgroundCopyJobHttpOptions3**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3) 
     [ **IBackgroundCopyServerCertificateValidationCallback**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyservercertificatevalidationcallback)


## <a name="version-102"></a>Version 10.2

Die folgenden Schnittstellen wurden für diese Version hinzugefügt.
-   [**IBackgroundCopyJobHttpOptions2**](/windows/win32/api/Bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2)


## <a name="version-101"></a>Version 10.1

Die folgenden Schnittstellen wurden für diese Version hinzugefügt.
-   [**BackgroundCopyFile6**](/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6)
-   [**IBackgroundCopyCallback3**](/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3)

Die folgenden Konstanten wurden hinzugefügt, um mit der -Enumeration BITS_JOB_PROPERTY_ID [zu verwenden.](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id)

-   **\_ \_ BITS-AUFTRAGSEIGENSCHAFT \_ IM \_ \_ BEDARFSMODUS**
-   **BITS \_ JOB \_ PROPERTY \_ MINIMUM \_ NOTIFICATION \_ INTERVAL \_ MS**


## <a name="version-50"></a>Version 5.0

Für diese Version wurden die folgenden Schnittstellen hinzugefügt:

-   [**IBackgroundCopyJob5**](/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5)

## <a name="version-40"></a>Version 4.0

Für diese Version wurden die folgenden Schnittstellen hinzugefügt:

-   [**IBitsToken**](/windows/win32/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
-   [**IBackgroundCopyFile4**](/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4)

## <a name="version-30"></a>Version 3.0

Für diese Version wurden die folgenden Schnittstellen hinzugefügt:

-   [**IBackgroundCopyCallback2**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2)
-   [**IBackgroundCopyFile3**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyfile3)
-   [**IBackgroundCopyJob4**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4)
-   [**IBitsPeer**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeer)
-   [**IBitsPeerCacheAdministration**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration)
-   [**IBitsPeerCacheRecord**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacherecord)
-   [**IEnumBitsPeerCacheRecords**](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeercacherecords)
-   [**IEnumBitsPeers**](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeers)

Die folgenden Konstanten wurden zur Verwendung mit der [**IBackgroundCopyJobHttpOptions::SetSecurityFlags-Methode**](/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags) hinzugefügt:

-   **BG \_ HTTP \_ REDIRECT \_ POLICY \_ ALLOW \_ SILENT**
-   **BG \_ HTTP \_ REDIRECT \_ POLICY \_ ALLOW \_ REPORT**
-   **BG \_ HTTP \_ REDIRECT \_ POLICY \_ DISALLOW**
-   **BG \_ HTTP \_ REDIRECT \_ POLICY \_ MASK**
-   **BG \_ HTTP REDIRECT POLICY ALLOW HTTPS TO HTTP (BG-HTTP-UMLEITUNGSRICHTLINIE ZULASSEN VON HTTPS \_ ZU \_ \_ \_ \_ \_ HTTP)**

## <a name="version-25"></a>Version 2.5

Die folgende Schnittstelle und Enumeration wurden für Version 2.5 hinzugefügt:

-   [**IBackgroundCopyJobHttpOptions**](/windows/win32/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions)
-   [**STANDORT \_ DES BG-ZERTIFIKATSPEICHERS \_ \_**](/windows/win32/api/Bits2_5/ne-bits2_5-bg_cert_store_location)

## <a name="version-20"></a>Version 2.0

Die folgenden Schnittstellen, Strukturen und Themen wurden für Version 2.0 hinzugefügt:

-   [**IBackgroundCopyJob3**](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3)
-   [**IBackgroundCopyFile2**](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyfile2)
-   [**\_ \_ BG-DATEIBEREICH**](/windows/win32/api/Bits2_0/ns-bits2_0-bg_file_range)
-   [Gruppenrichtlinien](group-policies.md)

Informationen zu gleichzeitigen Vordergrunddownloads finden Sie im Abschnitt Hinweise zu [**BG \_ JOB \_ PRIORITY**](/windows/win32/api/Bits/ne-bits-bg_job_priority).

Informationen zur Verwendung des SMB-Protokolls finden Sie unter [**BG \_ FILE \_ INFO**](/windows/win32/api/Bits/ns-bits-bg_file_info).

## <a name="version-15"></a>Version 1.5

Die folgenden Schnittstellen und Themen wurden für Version 1.5 hinzugefügt:

-   [**IBackgroundCopyJob2**](/windows/win32/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
-   [Abrufen der Antwort aus einem Upload-Reply Auftrag](retrieving-the-reply-from-an-upload-reply-job.md)
-   [Registrieren für die Ausführung eines Programms](registering-to-execute-a-program.md)
-   [BITS-Server Einstellungen für Hochladen Aufträge](bits-server-settings-for-upload-jobs.md)
-   [Einrichten des Servers für Uploads](setting-up-the-server-for-uploads.md)
-   [Verwenden von BITS-Benachrichtigungsanforderungs-/Antwortheadern](using-bits-notification-request-response-headers.md)

 
## <a name="updating-bits-versions"></a>Aktualisieren von BITS-Versionen
 
Sie können BITS 4.0 für Windows Server 2008 mit Service Pack 2 (SP2), Windows Vista mit Service Pack 1 (SP1) und Windows Vista mit Service Pack 2 (SP2) herunterladen. Informationen zum Herunterladen von BITS 4.0 finden Sie unter [KB968929](https://support.microsoft.com/kb/968929).
