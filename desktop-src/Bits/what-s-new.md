---
title: Neuigkeiten (BITS)
description: In der folgenden Tabelle sind die Neuerungen für die einzelnen Releases von Background Intelligent Transfer Service (Bits) aufgeführt.
ms.assetid: ef05f2e1-88be-4adb-aca7-a7b1451cfd04
keywords:
- neue Bits
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: b171a1d8cede9e3fd49ac81ab47ffb09f72b6200
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039921"
---
# <a name="whats-new-bits"></a>Neuigkeiten (BITS)

Seit der ersten Veröffentlichung als Teil von Windows XP wurde die Background Intelligent Transfer Service (Bits) ständig verbessert, wodurch Entwickler und Administratoren leistungsfähigere Steuerelemente zum Steuern und Verwalten von Downloads hinzufügen konnten. Es wurde ein umfangreicher Satz von PowerShell-Cmdlets hinzugefügt. Es kann eine Verbindung mit weiteren Typen von HTTP-Servern herstellen. die Netzwerkbandbreite und die Kosten des Benutzers sind eher vorsichtig als je zuvor. 

In der folgenden Tabelle sind die Neuerungen für die einzelnen Releases von Background Intelligent Transfer Service (Bits) aufgeführt.



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
<td>Version 10,3</td>
<td>Neue Funktionen:<br/>
<ul>
<li>" <a href="/windows/win32/api/bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3"><strong>BackgroundCopyJobHttpOptions3</strong></a> " wurde hinzugefügt, um HTTP-Header als schreibgeschützt zu markieren und um einen Validierungs Rückruf für einen Serverzertifikat festzulegen.</li>
<li>Bits behält die Dienst Identität bei, wenn Sie von einem anderen Systemdienst erstellt wird.</li>
<li>Bits überträgt weiterhin Dateien im verbundenen Standby, solange das Gerät angeschlossen ist.</li>
</ul>
Die Bits-Version 10,3 ist im Windows 10-Update vom Mai 2019 enthalten (10,0; Build 18362) und höher.
</td>
</tr>
<tr class="even">
<td>Version 10,2</td>
<td>Neue Funktionen:<br/>
<ul>
<li><a href="/windows/win32/api/bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2"><strong>BackgroundCopyJobHttpOptions2</strong></a> hinzugefügt, um die HTTP-Methode für http-Downloads zu ändern.</li>
<li>Bits verwendet nun die standardmäßige Proxy Reihenfolge, um die Konsistenz mit dem Rest des Systems zu verbleibenden.</li>
<li>Programmierer können die Bits-Proxykonfiguration für Unternehmens Szenarios einfacher festlegen.</li>
<li>Bits ist nun vorsichtiger und unterstützt den [modernen](/windows-hardware/design/device-experiences/modern-standby)Standbymodus.</li>
<li>Bits unterstützt jetzt zusätzlich zu den [Gruppenrichtlinien](./group-policies)Richt [Linien](/windows/client-management/mdm/policy-configuration-service-provider) für mobile Geräte-Manager (MDM).</li>
</ul>
BITS Version 10,2 ist in Windows 10-Update vom Oktober 2018 enthalten (10.0; Build 17763) und höher.
</td>
</tr>
<tr class="odd">
<td>Version 10,1</td>
<td>Neue Funktionen:<br/>
<ul>
<li>" <a href="/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6"><strong>BackgroundCopyFile6</strong></a> " und " <a href="/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3"><strong>IBackgroundCopyCallback3</strong></a> " wurden hinzugefügt, um Szenarios für den zufälligen Zugriff auf http</li>
<li>Hinzufügen von <strong>BITS_JOB_PROPERTY_ON_DEMAND_MODE</strong> und <strong>BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS</strong> zur <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>BITS_JOB_PROPERTY_ID</strong></a> -Enumeration, um das Download-und Benachrichtigungs Verhalten zu optimieren.</li>
</ul>
Die Bits-Version 10,1 ist im Update von Windows 10 Creator enthalten.
</td>
</tr>
<tr class="even">
<td>Version 5.0</td>
<td>Neue Funktionen:<br/>
<ul>
<li>Die <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5</strong></a> -Schnittstelle hinzugefügt, die generische Methoden zum erhalten und Festlegen von Bits-Auftrags Eigenschaften auf die von der <a href="/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4"><strong>IBackgroundCopyJob4</strong></a> -Schnittstelle geerbten Methoden hinzufügt.<br/> Weitere Informationen zur Verwendung der neuen <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5"><strong>IBackgroundCopyJob5</strong></a> -Schnittstelle finden Sie unter <a href="how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md">Steuern, ob ein BITS-Auftrag über eine teure Verbindung heruntergeladen werden darf</a> und <a href="how-to-get-the-last-set-of-http-headers-received-for-each-file-in-a-bits-download-job.md">wie der letzte Satz von HTTP-Headern für jede Datei in einem Bits-Download Auftrag empfangen</a>wird.<br/></li>
<li>Die <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_job_property_value"><strong>BITS_JOB_PROPERTY_VALUE</strong></a> Union und die <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id"><strong>BITS_JOB_PROPERTY_ID</strong></a>und <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_job_transfer_policy"><strong>BITS_JOB_TRANSFER_POLICY</strong></a> Enumerationen wurden hinzugefügt. Verwendungs Beispiele finden Sie in den obigen Themen zu Vorgehensweisen.</li>
<li>Die <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5</strong></a> -Schnittstelle wurde hinzugefügt, die Methoden zum erhalten und Festlegen von generischen Eigenschaften für backgroundcopyfile-Objekte auf die von der <a href="/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4"><strong>IBackgroundCopyFile4</strong></a> -Schnittstelle geerbten Methoden hinzufügt. Durch das Hinzufügen von generischen Eigenschaften ist es möglich, backgroundcopyfile-Funktionen in Zukunft zu verbessern, ohne dass eine neue Schnittstelle erstellt werden muss.</li>
<li>Die erste generische Eigenschaft, die von <a href="/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyfile5"><strong>IBackgroundCopyFile5</strong></a> verfügbar gemacht wird, ist die <strong>httprespongenheaders</strong> -Eigenschaft.</li>
<li>Die <a href="/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value"><strong>BITS_FILE_PROPERTY_VALUE</strong></a> Union und die <a href="/windows/win32/api/bits5_0/ne-bits5_0-bits_file_property_id"><strong>BITS_FILE_PROPERTY_ID</strong></a> -Enumeration wurden hinzugefügt.</li>
</ul>
Die Bits-Version 5,0 ist in den Betriebssystemen Windows Server 2012 und Windows 8 enthalten, bei denen die Version von% Windir% \System32\QMgr.dll &quot; 7.7. xxxx. xxxx &quot; ist.<br/> Die folgenden Features wurden Bits in Windows 10 hinzugefügt.<br/>
<ul>
<li>In Windows 10, Version 1607, ist es möglich, die Bits-com-APIs und Bits-PowerShell-Cmdlets (sofern verfügbar) in einer PowerShell-Remote Sitzung zu verwenden. Dies ist besonders nützlich, wenn Sie Versionen von Windows Server 2016 verwalten, die über keine lokale Anmelde Funktion verfügen. Über PowerShell-Remotesitzungen gestartete BITS-Aufträge werden im Benutzerkontokontext der Sitzung ausgeführt und machen nur Fortschritte, wenn diesem Benutzerkonto mindestens eine aktive lokale Anmeldesitzung oder PowerShell-Remotesitzung zugeordnet ist. Verwenden Sie permanente PowerShell-Remote Sitzungen (siehe <a href="/powershell/module/microsoft.powershell.core/new-pssession">New-PSSession</a>) für Übertragungen mit langer Laufzeit.</li>
<li>In Windows 10, Version 1607, ist es für einen Bits-Auftrags Besitzer nun möglich, Hilfstoken ohne Administratorrechte festzulegen, solange das Hilfsobjekt keine Administrator Funktionen hat. Dadurch werden Sicherheitsrisiken von Tools für Hintergrunddownloads oder -aktualisierungen gemindert, da diese Tools nicht unter einem Konto mit Administratorrechten, sondern unter dem NetworkService-Konto mit niedrigeren Berechtigungen ausgeführt werden.</li>
</ul>
BITS Version 5,0 ist auch in Windows 10 enthalten, wobei die Version von% Windir% \System32\QMgr.dll den Wert &quot; 7.8. xxxx. xxxx &quot; hat.<br/></td>
</tr>
<tr class="odd">
<td>Version 4.0</td>
<td>Neue Funktionen:<br/>
<ul>
<li>Peer Caching verwendet jetzt Windows BranchCache. Dieses neue Peer Cache Modell ersetzt das Modell, das für die Bits-Version 3,0 verwendet wird. Weitere Informationen finden Sie unter <a href="peer-caching.md">Peer Caching</a>.</li>
<li>Es wurde ein flexibleres Ressourcen Zugriffs Modell hinzugefügt, mit dem Anwendungen einem Bits-Übertragungs Auftrag ein paar von Sicherheits Token zuordnen können. Weitere Informationen finden Sie unter <a href="helper-tokens-for-bits-transfer-jobs.md">Helper Tokens für Bits-Übertragungs Aufträge</a>.</li>
<li>Der <a href="bits-compact-server.md">BITS Compact-Server</a>wurde hinzugefügt. dabei handelt es sich um einen eigenständigen HTTP/HTTPS-Datei Server, der die Möglichkeit bietet, eine begrenzte Anzahl von großen Dateien asynchron zwischen Computern zu übertragen.</li>
<li>Eine präzisetere Bandbreitendrosselung wurde hinzugefügt. Weitere Informationen finden Sie unter <a href="group-policies.md">Gruppenrichtlinien</a>.</li>
</ul>
Die Bits-Version 4,0 ist in den Betriebssystemen Windows Server 2008 R2 und Windows 7 enthalten.<br/> Sie können auch Bits 4,0 für Windows Server 2008 mit Service Pack 2 (SP2), Windows Vista mit Service Pack 1 (SP1) und Windows Vista mit Service Pack 2 (SP2) herunterladen. Weitere Informationen zum Herunterladen von Bits 4,0 finden Sie unter <a href="https://support.microsoft.com/kb/968929">KB968929</a>.<br/> Die Version von% Windir% \System32\QMgr.dll ist &quot; 7.5. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Version 3.0</td>
<td>Neue Funktionen:<br/>
<ul>
<li><a href="peer-caching.md">Peer Caching</a> hinzugefügt, mit dem Sie Inhalte von Peers herunterladen und auch Inhalte für Peers in einem Domänen Netzwerk bereitstellen können.</li>
<li>Beim Herunterladen einer Datei wurde eine <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred">Benachrichtigung</a> hinzugefügt.</li>
<li>Der Zugriff auf die <a href="/windows/win32/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname">temporäre Datei</a> wurde während des Downloads hinzugefügt.</li>
<li>Die Möglichkeit, http- <a href="/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags">Umleitungen</a>zu steuern, wurde hinzugefügt.</li>
<li>Weitere <a href="group-policies.md">Gruppenrichtlinien</a> zum Steuern der Peer Zwischenspeicherung und zum Einschränken der Downloadzeiten wurden hinzugefügt.</li>
<li>Dem System Ereignisprotokoll wurden Diagnose-und Problem Behandlungs Ereignisse hinzugefügt.</li>
<li>Unterstützung für die <a href="user-account-control-and-bits.md">Benutzerkontensteuerung</a> (UAC) wurde hinzugefügt.</li>
<li>Unter Windows Vista und höher wird der standardmäßige Bits-Starttyp verzögert automatisch gestartet.</li>
</ul>
<blockquote>
[!Note]<br />
Bits verwendet jetzt Gruppenrichtlinien, um die Anzahl der Aufträge und Dateien einzuschränken, die Sie erstellen können. Dies kann sich auf Anwendungen auswirken, die derzeit eine große Anzahl von Aufträgen erstellen oder einem Auftrag eine große Anzahl von Dateien hinzufügen.
</blockquote>
<br/> <br/> Die Bits-Version 3,0 ist in den Betriebssystemen Windows Server 2008 und Windows Vista enthalten. <br/> Die Version von% Windir% \System32\QMgr.dll ist &quot; 7.0. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Version 2.5</td>
<td>Unterstützung für benutzerdefinierte HTTP-Header, Zertifikat basierte Client Authentifizierung für sichere HTTP-Transporte und IPv6 hinzugefügt. Außerdem wurde die Verwendung von Leistungsindikatoren für Internet Gateway-Geräte (IGD) zur genaueren Berechnung der verfügbaren <a href="network-bandwidth.md">Bandbreite</a>hinzugefügt.<br/> Die Bits 2,5-Funktionen sind in den Betriebssystemen Windows Server 2008, Windows Vista und Windows XP mit Service Pack 3 (SP3) verfügbar. <br/> Sie können auch BITS 2,5 für Windows Server 2003 mit Service Pack 2 (SP2), Windows Server 2003 mit Service Pack 1 (SP1) und Windows XP mit Service Pack 2 (SP2) herunterladen. Um Bits 2,5 herunterzuladen, navigieren Sie zum <a href="https://www.microsoft.com/download/details.aspx?id=4933">Microsoft Download Center</a> , und installieren Sie KB923845.<br/> Die Version von% Windir% \System32\QMgr.dll ist &quot; 6.7. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Version 2.0</td>
<td>Unterstützung für das Ausführen von gleichzeitigen Downloads für den Vordergrund, die Verwendung von SMB-Pfaden (Server Message Block) für Remote Namen, das Herunterladen von Bereichen einer Datei, das Ändern des Präfix oder den Namen eines Remote namens und das Einschränken der Bandbreitennutzung durch Die Richtlinie "jobinactivitytimeout" befindet sich jetzt unter Computer Konfiguration, administrative Vorlagen, Netzwerk, Background Intelligent Transfer Service (Bits).<br/> BITS Version 2,0 ist in Windows XP mit SP2 und Windows Server 2003 mit SP1 enthalten. Sie können auch BITS 2,0 für Windows Server 2003 und Windows XP herunterladen. Um Bits 2,0 herunterzuladen, navigieren Sie zum <a href="https://www.microsoft.com/download/details.aspx?id=19031">Microsoft Download Center</a> , und installieren Sie KB842773.<br/> Die Version von% Windir% \System32\QMgr.dll ist &quot; 6.6. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Version 1.5</td>
<td>Die Funktionen "Upload" und "Upload-Reply", die Befehlszeilen Ausführung für Ereignisse und explizite Anmelde Informationen und Proxy Anmelde Informationen wurden hinzugefügt.<br/> Ab Bits 1,5 können Benutzer mit <a href="/windows/win32/secauthz/restricted-tokens">eingeschränktem Token</a> keine Aufträge erstellen oder ändern.<br/> Die Bits-Version 1,5 ist in Windows Server 2003 enthalten. Eine verteilbare Komponente ist für Windows XP im <a href="https://www.microsoft.com/download/details.aspx?id=22250">Microsoft Download Center</a>verfügbar.<br/> Die Version von% Windir% \System32\QMgr.dll ist &quot; 6.5. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="even">
<td>Version 1.2</td>
<td>Gleiche Funktionalität wie Version 1,0. Enthält interne Upgrades und Verbesserungen.<br/> Die Bits-Version 1,2 ist in Windows XP mit Service Pack 1 (SP1) enthalten.<br/> Die Version von% Windir% \System32\QMgr.dll ist &quot; 6.2. xxxx. xxxx &quot; .<br/></td>
</tr>
<tr class="odd">
<td>Version 1.0</td>
<td>Erste Veröffentlichung Bietet priorisierte, gedrosselt und asynchrone Downloads im Hintergrund oder im Vordergrund. Die Downloads werden nach dem Neustart des Computers und der Netzwerk Trennung automatisch fortgesetzt.<br/> Die Bits-Version 1,0 ist in Windows XP enthalten.<br/> Die Version von% Windir% \System32\QMgr.dll ist &quot; 6.0. xxxx. xxxx &quot; .<br/></td>
</tr>
</tbody>
</table>

Verwenden Sie QueryInterface on (z. b.), um die Funktionen in Ihrem Programm auf der Grundlage von Bits-Funktionen zu erweitern, um festzustellen, ob das Auftrags Objekt Ihnen das Erstellen der benötigten Version ermöglicht. Weitere Informationen finden Sie unter [bestimmen der Version von Bits auf einem Computer](./determining-the-version-of-bits-on-a-computer.md) zum Konvertieren der QMgr.dll Versionsnummer in die Bits-Version.

## <a name="version-103"></a>Version 10,3

Die folgenden Schnittstellen wurden für diese Version hinzugefügt.
-   [**IBackgroundCopyJobHttpOptions3**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyjobhttpoptions3) 
     [ **Ibackgroundcopyservercertifigatevalidationcallback**](/windows/win32/api/Bits10_3/nn-bits10_3-ibackgroundcopyservercertificatevalidationcallback)


## <a name="version-102"></a>Version 10,2

Die folgenden Schnittstellen wurden für diese Version hinzugefügt.
-   [**IBackgroundCopyJobHttpOptions2**](/windows/win32/api/Bits10_2/nn-bits10_2-ibackgroundcopyjobhttpoptions2)


## <a name="version-101"></a>Version 10,1

Die folgenden Schnittstellen wurden für diese Version hinzugefügt.
-   [**BackgroundCopyFile6**](/windows/win32/api/bits10_1/nn-bits10_1-ibackgroundcopyfile6)
-   [**IBackgroundCopyCallback3**](/windows/win32/api/Bits10_1/nn-bits10_1-ibackgroundcopycallback3)

Die folgenden Konstanten wurden zur Verwendung mit der [BITS_JOB_PROPERTY_ID-Enumeration](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id)hinzugefügt.

-   **Bits- \_ Auftrags \_ Eigenschaft \_ im \_ Bedarfs \_ Modus**
-   **\_ \_ \_ minimale \_ Benachrichtigungs \_ Intervall \_ für Bits-Auftrags Eigenschaft (MS)**


## <a name="version-50"></a>Version 5.0

Die folgenden Schnittstellen wurden für diese Version hinzugefügt:

-   [**IBackgroundCopyJob5**](/windows/win32/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5)

## <a name="version-40"></a>Version 4.0

Die folgenden Schnittstellen wurden für diese Version hinzugefügt:

-   [**Ibitstoken**](/windows/win32/api/Bits4_0/nn-bits4_0-ibitstokenoptions)
-   [**IBackgroundCopyFile4**](/windows/win32/api/Bits4_0/nn-bits4_0-ibackgroundcopyfile4)

## <a name="version-30"></a>Version 3.0

Die folgenden Schnittstellen wurden für diese Version hinzugefügt:

-   [**IBackgroundCopyCallback2**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2)
-   [**IBackgroundCopyFile3**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyfile3)
-   [**IBackgroundCopyJob4**](/windows/win32/api/Bits3_0/nn-bits3_0-ibackgroundcopyjob4)
-   [**Ibitspeer**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeer)
-   [**Ibitspeercacheadministration**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration)
-   [**Ibitspeercacherecord**](/windows/win32/api/Bits3_0/nn-bits3_0-ibitspeercacherecord)
-   [**Ienumbitspeercacherecords**](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeercacherecords)
-   [**Ienumbitspeer**](/windows/win32/api/Bits3_0/nn-bits3_0-ienumbitspeers)

Die folgenden Konstanten wurden zur Verwendung mit der [**ibackgroundcopyjobhttpoptions:: setsecurityflags**](/windows/win32/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags) -Methode hinzugefügt:

-   **BG \_ http- \_ Umleitungs Richtlinie unbeaufsichtigt \_ \_ zulassen \_**
-   **Bericht "BG \_ http- \_ Umleitungs \_ Richtlinie \_ zulassen \_ "**
-   **BG \_ http- \_ Umleitungs \_ Richtlinie nicht \_ zulassen**
-   **BG- \_ http- \_ Umleitungs \_ Richtlinien \_ Maske**
-   **BG \_ http- \_ Umleitungs \_ Richtlinie \_ \_ \_ \_ HTTP-Umleitung zulassen**

## <a name="version-25"></a>Version 2.5

Die folgende Schnittstelle und Enumeration wurden für Version 2,5 hinzugefügt:

-   [**Ibackgroundcopyjobhttpoptions**](/windows/win32/api/Bits2_5/nn-bits2_5-ibackgroundcopyjobhttpoptions)
-   [**BG \_ - \_ Zertifikat \_ Speicherort**](/windows/win32/api/Bits2_5/ne-bits2_5-bg_cert_store_location)

## <a name="version-20"></a>Version 2.0

Die folgenden Schnittstellen, Strukturen und Themen wurden für Version 2,0 hinzugefügt:

-   [**IBackgroundCopyJob3**](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyjob3)
-   [**IBackgroundCopyFile2**](/windows/win32/api/Bits2_0/nn-bits2_0-ibackgroundcopyfile2)
-   [**BG- \_ Datei \_ Bereich**](/windows/win32/api/Bits2_0/ns-bits2_0-bg_file_range)
-   [Gruppenrichtlinien](group-policies.md)

Weitere Informationen zu gleichzeitigen Downloads im Vordergrund finden Sie im Abschnitt "Hinweise" für die [**BG- \_ Auftrags \_ Priorität**](/windows/win32/api/Bits/ne-bits-bg_job_priority).

Weitere Informationen zur Verwendung des SMB-Protokolls finden Sie unter [**BG- \_ Datei \_ Info**](/windows/win32/api/Bits/ns-bits-bg_file_info).

## <a name="version-15"></a>Version 1.5

Die folgenden Schnittstellen und Themen wurden für Version 1,5 hinzugefügt:

-   [**IBackgroundCopyJob2**](/windows/win32/api/Bits1_5/nn-bits1_5-ibackgroundcopyjob2)
-   [Abrufen der Antwort von einem Upload-Reply Auftrag](retrieving-the-reply-from-an-upload-reply-job.md)
-   [Registrieren zum Ausführen eines Programms](registering-to-execute-a-program.md)
-   [BITS-Server Einstellungen für Upload-Aufträge](bits-server-settings-for-upload-jobs.md)
-   [Einrichten des Servers für Uploads](setting-up-the-server-for-uploads.md)
-   [Verwenden von Bits-Benachrichtigungs Anforderung/Antwort-Headern](using-bits-notification-request-response-headers.md)

 
## <a name="updating-bits-versions"></a>Aktualisieren von Bits-Versionen
 
Sie können Bits 4,0 für Windows Server 2008 mit Service Pack 2 (SP2), Windows Vista mit Service Pack 1 (SP1) und Windows Vista mit Service Pack 2 (SP2) herunterladen. Weitere Informationen zum Herunterladen von Bits 4,0 finden Sie unter [KB968929](https://support.microsoft.com/kb/968929).
