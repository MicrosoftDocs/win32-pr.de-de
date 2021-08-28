---
title: BITS IIS-Erweiterung (Eigenschaften)
description: Background Intelligent Transfer Service (BITS) verwendet eine ISAPI, um IIS zur Unterstützung von Uploadaufträgen zu erweitern.
ms.assetid: 08a40cc1-ec6d-4b65-971a-15c7b06df148
keywords:
- BITS-IIS-Erweiterungseigenschaften BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1afb18e324419834d5a1445d1a1b9e5390f5d932
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480946"
---
# <a name="bits-iis-extension-properties"></a>BITS IIS-Erweiterung (Eigenschaften)

Background Intelligent Transfer Service (BITS) verwendet eine ISAPI, um IIS zur Unterstützung von [**Uploadaufträgen**](/windows/win32/api/bits/ne-bits-bg_job_type)zu erweitern. In der folgenden Tabelle sind die Eigenschaften aufgeführt, die BITS der IIS-Metabasis für die Komponente des virtuellen Verzeichnisses hinzufügt. BITS verwendet diese Eigenschaften, um zu bestimmen, wie die Dateien hochgeladen werden. Die BITS-IIS-Erweiterungseigenschaften sind vererbbar, mit Ausnahme von **BITSUploadEnabled.**




| Eigenschaft | BESCHREIBUNG | 
|----------|-------------|
| <strong>BITSUploadEnabled</strong> Datentyp: <strong>Boolean</strong><br /> | Gibt an, ob BITS-Uploads im virtuellen Verzeichnis aktiviert sind. Wenn die Einstellung nicht vorhanden ist oder 0 ist, werden BITS-Uploads deaktiviert.<br /> Dies ist eine schreibgeschützte Eigenschaft. Um diese Eigenschaft festzulegen, rufen Sie die <a href="/windows/win32/api/bitscfg/nf-bitscfg-ibitsextensionsetup-enablebitsuploads"><strong>EnableBITSUploads-</strong></a> oder <a href="/windows/win32/api/bitscfg/nf-bitscfg-ibitsextensionsetup-disablebitsuploads"><strong>DisableBITSUploads-Methode</strong></a> der <a href="/windows/win32/api/bitscfg/nn-bitscfg-ibitsextensionsetup"><strong>IBITSExtensionSetup-Schnittstelle</strong></a> auf.<br /> | 
| <strong>BITSSessionTimeout</strong> Datentyp: <strong>DWORD</strong><br /> | Anzahl der Sekunden, in der die Verbindung beibehalten wird, wenn beim Hochladen der Datei kein Fortschritt erzielt wird. Der Timer wird zurückgesetzt, wenn der Fortschritt erfolgt. BITS schließt die Verbindung, wenn das Time out erreicht ist, und bereinigt die der Sitzung zugeordneten Daten.<br /> Das Festlegen eines kurzen Sitzungstime outs kann ein Problem bei Upload-Antwort-Aufträgen sein, da die Antwort nur heruntergeladen wird, wenn der Benutzer angemeldet und mit dem Netzwerk verbunden ist. Es ist möglich, dass für die Sitzung ein Time out erfolgt, bevor die Antwort heruntergeladen wird. In diesem Fall wird die Sitzung abgebrochen und die Antwortdatei gelöscht.<br /> Beachten Sie, dass BITS den Auftrag abbricht, wenn der <a href="/windows/win32/bits/group-policies">JobInactivityTimeout-Gruppenrichtlinie</a> Wert (Standardwert ist 90 Tage) unabhängig von dieser Einstellung erreicht ist.<br /> Der Standardwert ist 1.209.600 (14 Tage).<br /> | 
| <strong>BITSMaximumUploadSize</strong> Datentyp: <strong>Zeichenfolge</strong><br /> | Maximale Anzahl von Bytes, die pro Auftrag hochgeladen werden können. Geben Sie die maximale Anzahl von Bytes als Dezimalzeichenfolge an. Der Zeichenfolgenwert muss kleiner oder gleich "1844674407370955" sein. Eine leere Zeichenfolge entspricht der Angabe von "1844674407370955".<br /> Der Standardwert ist eine leere Zeichenfolge.<br /><blockquote>[!Note]<br />In IIS 7 beträgt das Standardmäßige Uploadlimit 30 Millionen Bytes. Der Wert der <strong>BITSMaximumUploadSize-Eigenschaft</strong> darf den IIS-Grenzwert nicht überschreiten. Ausführliche Informationen und Informationen zum Ändern der IIS-Standardeinstellung finden Sie unter <a href="https://support.microsoft.com//kb/942074">KB942074.</a></blockquote><br /><br /> | 
| <strong>BITSServerNotificationType</strong> Datentyp: <strong>DWORD</strong><br /> | Gibt an, wie die Uploaddatei an die Serveranwendung gesendet wird. Die möglichen Werte sind: 0, 1 und 2.<br /> Der Wert 0 bedeutet, dass die Datei nicht an die Serveranwendung gesendet wird. BITS fügt die Uploaddatei in das Verzeichnis ein, das im Remotenamen angegeben ist (der Remotename, der beim <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-addfile">Hinzufügen der Datei</a> zum Auftrag angegeben wurde), ohne die Serveranwendung zu benachrichtigen. Wenn die Datei derzeit im Zielverzeichnis vorhanden ist, wird sie durch die Uploaddatei ersetzt.<br /> Der Wert 1 bedeutet, dass BITS den Speicherort der Uploaddatei an die Serveranwendung übergibt, die in der <strong>BITSServerNotificationURL-Eigenschaft</strong> angegeben ist. Die Serveranwendung verarbeitet die Datei und generiert bei Bedarf eine Antwortdatei. Standardmäßig entfernt BITS die Upload- und Antwortdateien vom Server, nachdem die Antwort von der Serveranwendung empfangen wurde. Damit BITS die Uploaddatei an den Speicherort kopiert, der durch den Remotedateinamen im Auftrag angegeben wird, fügen Sie den <a href="/windows/win32/bits/notification-protocol-for-server-applications">Header BITS-Copy-File-To-Destination</a> in Ihre Antwort ein. Wenn Sie den Header nicht einschließen und die Upload- und Antwortdateien speichern möchten, müssen Sie die Upload- und Antwortdateien an einen neuen Speicherort kopieren, bevor Sie antworten.<br /> Der Wert 2 bedeutet, dass BITS die Uploaddatei im Anforderungstext an die Serveranwendung übergibt, die in der <strong>BITSServerNotificationURL-Eigenschaft</strong> angegeben ist. Die Serveranwendung verarbeitet die Datei und übergibt die Antwort bei Bedarf im Text der Antwort zurück.<br /> Ausführliche Informationen zu den Anforderungs- und Antwortheadern finden Sie unter <a href="/windows/win32/bits/notification-protocol-for-server-applications">Notification Protocol for Server Applications</a>.<br /> Die Serveranwendung muss innerhalb von fünf Minuten eine Antwort bereitstellen. Wenn die Serveranwendung nicht innerhalb von fünf Minuten antwortt, wechselt der Auftrag in den vorübergehenden Fehlerzustand. Wenn die <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay"><strong>Wiederholungsverzögerung</strong></a> abläuft, sendet der BITS-Server eine weitere Benachrichtigung an die Serveranwendung (die Serveranwendung sollte geschrieben werden, um doppelte Benachrichtigungen zu verarbeiten). <strong>BITS 1.5:</strong> Das Benachrichtigungstime out beträgt 30 Sekunden.<br /><br /> Der Standardwert ist 0.<br /> | 
| <strong>BITSServerNotificationURL</strong> Datentyp: <strong>Zeichenfolge</strong><br /> | Optional. Enthält die URL der Serveranwendung, an die BITS die Uploaddatei sendet. Sie müssen eine URL angeben, wenn der Wert der <strong>BITSServerNotificationType-Eigenschaft</strong> 1 oder 2 ist. Die URL ist auf 2.200 Zeichen beschränkt, ohne das NULL-Abschlusszeichen. Die URL muss eine HTTP-URL sein. BITS unterstützt keine HTTPS-Benachrichtigungs-URLs.<br /> Wenn die URL zum Zeitpunkt des Uploads nicht verfügbar ist, versucht BITS den Upload so lange, bis die Benachrichtigungs-URL vorhanden ist oder der Wiederholungszeitraum abläuft.<br /> Beachten Sie Folgendes: Wenn der im Auftrag angegebene Remotename eine Abfragezeichenfolge enthält, wird die Abfragezeichenfolge an die von Ihnen angegebene URL angefügt. Wenn der Remotename beispielsweise enthält https://myserver/myvdir/subdir/file.asp?ACCOUNT=86433 und Sie die <strong>BITSServerNotificationURL-Einstellung</strong> als https://otherserver/myvdir2/bag.asp angeben, lautet die URL, an die BITS https://otherserver/myvdir2/bag.asp?ACCOUNT=86433 beiträget, .<br /> Wenn die ursprüngliche URL https://myserver/myvdir/file.txt und die Benachrichtigungs-URL myasp.asp lautet, verwendet BITS http://myserver/myvdir/myasp.asp als Benachrichtigungs-URL.<br /> Wenn der Pfad- und Dateinamenteil der URL Unicode-Zeichen enthält, die der Codepage auf client und server nicht gemeinsam sind, schlägt die URL-Übersetzung auf dem Server fehl, und der BITS-Auftrag wird in den Fehlerzustand versetzt. Wenn der Serverteil der URL Unicode-Zeichen enthält, müssen Sie den Serverteil mithilfe von <a href="/windows/win32/intl/handling-internationalized-domain-names--idns">Internationalized Domain Names</a> (IDN) codieren.<br /> | 
| <strong>BITSHostId</strong> Datentyp: <strong>Zeichenfolge</strong><br /> | Legen Sie diese Eigenschaft fest, wenn die Serverinstallation eine Webfarm ist, die keinen freigegebenen Speicher verwendet.<br /> Geben Sie den Servernamen oder die IP-Adresse des Servers an, mit dem die Verbindung erneut hergestellt werden soll, nachdem der Uploadvorgang unterbrochen wurde. In der Regel geben Sie den Namen des Servers an, den Sie konfigurieren. Die URL ist auf 300 Zeichen beschränkt, ohne das NULL-Abschlusszeichen.<br /> Wenn Sie diese Eigenschaft nicht angeben und der Uploadvorgang unterbrochen wird, kann bits den Auftrag auf einem anderen Server in der Farm fortsetzen. Der vorherige Server enthält jedoch weiterhin die Teiluploaddatei von vor der Unterbrechung. BITS entfernt die Teildatei, nachdem <strong>BITSSessionTimeout</strong> abgelaufen ist.<br /><blockquote>[!Note]<br />Verwenden Sie die <strong>BITSHostId-Eigenschaft</strong> nicht, wenn SSL in einer Webfarm verwendet wird, die Netzwerklastenausgleich (Network Load Balancing, NLB) oder DNS-Namen mit mehreren IP-Adressen verwendet, es sei denn, Sie schließen den Clusternamen und die einzelnen Servernamen in das Zertifikat ein. (Wenn der in <strong>BITSHostId</strong> angegebene Servername nicht mit dem allgemeinen Namen im Zertifikat übereinstimmt, schlägt der Auftrag fehl.) Legen Sie stattdessen für NLB den <a href="/previous-versions/tn-archive/bb687542(v=technet.10)">Affinity-Parameter</a> auf <strong>Single</strong> fest, um sicherzustellen, dass der Client in Zukunft mit demselben Server kommuniziert.</blockquote><br /><br /> | 
| <strong>BITSHostIdFallbackTimeout</strong> Datentyp: <strong>DWORD</strong><br /> | Anzahl von Sekunden, in der der BITS-Client versucht, erneut eine Verbindung mit dem <strong>BITSHostId-Servernamen</strong> herzustellen, bevor er auf den Hostnamen zurückgesetzt wird, der im Remotedateinamen des Auftrags angegeben ist. Der Timer beginnt, wenn BITS keine Verbindung mit dem <strong>BITSHostId-Server</strong> herstellen kann. Der Timer wird zurückgesetzt, wenn der Client erfolgreich eine Verbindung mit dem Server herstellt.<br /> Beachten Sie, dass der Wert für kein Statustimeout des Auftrags (siehe <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout"><strong>IBackgroundCopyJob::SetNoProgressTimeout</strong></a>) länger als dieser Timeoutwert sein sollte. Wenn dies nicht der Fall ist, schlägt der Auftrag fehl, bevor der Fallbacktimeoutwert abläuft.<br /> Legen Sie diese Eigenschaft nur fest, wenn Sie die <strong>BITSHostId-Eigenschaft</strong> festlegen.<br /> Der Standardwert ist 86.400 (1 Tag).<br /> | 
| <strong>BITSAllowOverwrites</strong> Datentyp: <strong>Ganze Zahl</strong><br /> | Gibt an, ob eine Uploaddatei eine vorhandene Datei mit dem gleichen Namen überschreiben kann. Die Uploaddatei überschreibt die vorhandene Datei, wenn <strong>BITSAllowOverwrites</strong> 1 ist.<br /> Der Standardwert ist 0.<br /><strong>IIS 6.0:</strong> Sie können diese Eigenschaft nur über ein Skript festlegen. Sie können sie nicht über die Eigenschaftenseite der BITS-Erweiterung auf der IIS-Benutzeroberfläche festlegen.<br /><br /> | 
| <strong>BITSCleanupUseDefault</strong> Datentyp: <strong>Boolean</strong><br /> | Gibt an, ob der Bereinigungstask die Standardzeitpläne verwendet. Standardmäßig wird die Bereinigungsaufgabe alle 12 Stunden ausgeführt.<br /> Legen Sie auf 1 fest, um den Standardzeitplan zu verwenden. andernfalls 0, um einen Zeitplan anzugeben.<br /> Verwenden Sie zum Angeben eines Zeitplans die Eigenschaften <strong>BITSCleanupCount</strong> und <strong>BITSCleanupUnits.</strong><br /> Der Cleanuptask bereinigt das virtuelle Verzeichnis, indem Aufträge gelöscht werden, die innerhalb des Sitzungstimeoutzeitraums nicht geändert wurden (siehe <strong>BITSSessionTimeout</strong>).<br /> Der Standardwert ist 1. Verwenden Sie den Standardzeitplan.<br /><strong>IIS 6.0:</strong> Wird nicht unterstützt.<br /> | 
| <strong>BITSCleanupCount</strong> Datentyp: <strong>Ganze Zahl</strong><br /> | Gibt das Intervall an, das zwischen der Ausführung des Bereinigungstasks gewartet werden soll. Das Intervall, das Sie angeben können, hängt von den Einheiten ab. Mögliche Intervallwerte finden Sie in der <strong>BITSCleanupUnits-Eigenschaft.</strong><br /> Diese Eigenschaft wird ignoriert, wenn <strong>BITSCleanupUseDefault</strong> 0 ist.<br /><strong>IIS 6.0:</strong> Wird nicht unterstützt.<br /><br /> | 
| <strong>BITSCleanupUnits</strong> Datentyp: <strong>Ganze Zahl</strong><br /> | Gibt die Einheiten für das Bereinigungsintervall an, das in der <strong>BITSCleanupCount-Eigenschaft</strong> angegeben ist. Diese Eigenschaft wird ignoriert, wenn <strong>BITSCleanupUseDefault</strong> 0 ist.<br /> Mögliche Werte sind:<dl> 0: Die Einheiten sind Minuten. Mögliche Werte sind 1 bis 60.<br />1: Die Einheiten sind Stunden. Dies ist die Standardoption. Mögliche Werte sind 1 bis 24.<br />2: Die Einheiten sind Tage. Mögliche Werte sind 1 bis 360.<br /></dl><br /><strong>IIS 6.0:</strong> Wird nicht unterstützt.<br /><br /> | 
| <strong>BITSNumberOfSessionsLimit</strong> Datentyp: <strong>Ganze Zahl</strong><br /> | Schränkt die Anzahl der Uploadsitzungen ein, die gleichzeitig für einen Benutzer vorhanden sein können. Wenn die Anzahl der Sitzungen für einen Benutzer diesen Grenzwert überschreitet, werden beim Ausführen des Bereinigungstasks die letzten Sitzungen gelöscht, bis die Anzahl der Sitzungen für den Benutzer unter dem Grenzwert liegt.<br /> Der Standardwert ist 50 Sitzungen.<br /><strong>IIS 6.0:</strong> Wird nicht unterstützt.<br /><br /> | 
| <strong>BITSSessionLimitEnable</strong> Datentyp: <strong>Boolean</strong><br /> | Gibt an, ob BITS die Anzahl der Uploadsitzungen pro Benutzer einschränkt. Wenn die Einstellung nicht vorhanden ist oder 0 ist, ist der Grenzwert deaktiviert.<br /> Um den Grenzwert anzugeben, legen Sie die <strong>BITSNumberOfSessionsLimit-Eigenschaft</strong> fest.<br /> Der Standardwert ist 1.<br /><strong>IIS 6.0:</strong> Wird nicht unterstützt.<br /><br /> | 




 

Das folgende Beispiel zeigt, wie die BITS-IIS-Erweiterungseigenschaften mithilfe Windows Skripthosts festgelegt werden. Wenn das virtuelle Verzeichnis auf eine Remotefreigabe verweist, legen Sie auch die **IIS-Eigenschaften UNCUserName** und **UNCPassword** fest.


```JScript
if (WScript.Arguments.length < 2)
{
    WScript.Echo("Usage: bitsvdir virtual_directory local_directory");
    WScript.Quit(1);
}

VirtualDirectoryName = WScript.Arguments(0);
LocalDirectoryName = WScript.Arguments(1);

ServerObj = GetObject("IIS://LocalHost/W3SVC/1/ROOT");
VirtualDir = ServerObj.Create("IIsWebVirtualDir", VirtualDirectoryName );

VirtualDir.Path = LocalDirectoryName;
VirtualDir.AppIsolated = 0;
VirtualDir.AccessScript = true;
VirtualDir.AccessRead = false;
VirtualDir.AccessWrite = false;
VirtualDir.SetInfo();

// Set BITS specific IIS configuration settings
VirtualDir.EnableBITSUploads();
VirtualDir.BITSMaximumUploadSize = "4294967296";
VirtualDir.SetInfo();

WScript.Echo( "Created virtual directory " + VirtualDirectoryName + 
              " with a local directory of " + LocalDirectoryName );
WScript.Quit( 0 );
```



 

