---
title: BITS IIS-Erweiterung (Eigenschaften)
description: Background Intelligent Transfer Service (Bits) verwendet eine ISAPI zum Erweitern von IIS zur Unterstützung von Uploadaufträgen.
ms.assetid: 08a40cc1-ec6d-4b65-971a-15c7b06df148
keywords:
- Bits der IIS-Erweiterungs Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c09412f6aa0be1ab76e6e45ea0920e1caf1054d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516970"
---
# <a name="bits-iis-extension-properties"></a>BITS IIS-Erweiterung (Eigenschaften)

Background Intelligent Transfer Service (Bits) verwendet eine ISAPI zum Erweitern von IIS zur Unterstützung von [**Uploadaufträgen**](/windows/win32/api/bits/ne-bits-bg_job_type). In der folgenden Tabelle werden die Eigenschaften aufgelistet, die von Bits zur IIS-Metabase für die virtuelle Verzeichnis Komponente hinzugefügt werden. Bits verwendet diese Eigenschaften, um zu bestimmen, wie die Dateien hochgeladen werden. Die BITS-IIS-Erweiterungs Eigenschaften sind vererbbar, mit Ausnahme von **bitsuploadaktiviertem**.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Bitsuploadaktivierte</strong> Datentyp: <strong>boolescher</strong> Wert<br/></td>
<td>Gibt an, ob BITS-Uploads für das virtuelle Verzeichnis aktiviert sind. Wenn die Einstellung nicht vorhanden ist oder den Wert 0 hat, sind BITS-Uploads deaktiviert.<br/> Dies ist eine schreibgeschützte Eigenschaft. Um diese Eigenschaft festzulegen, wenden Sie die Methode <a href="/windows/win32/api/bitscfg/nf-bitscfg-ibitsextensionsetup-enablebitsuploads"><strong>enablebitsuploads</strong></a> oder <a href="/windows/win32/api/bitscfg/nf-bitscfg-ibitsextensionsetup-disablebitsuploads"><strong>disablebitsuploads</strong></a> der <a href="/windows/win32/api/bitscfg/nn-bitscfg-ibitsextensionsetup"><strong>ibitsextensionsetup</strong></a> -Schnittstelle an.<br/></td>
</tr>
<tr class="even">
<td><strong>Bitssessiontimeout</strong> Datentyp: <strong>DWORD</strong><br/></td>
<td>Die Anzahl der Sekunden, die die Verbindung aufrechterhalten wird, wenn der Upload der Datei nicht fortgesetzt wird. der Zeitgeber wird zurückgesetzt, wenn der Fortschritt ausgeführt wird. Bits schließt die Verbindung, wenn das Timeout erreicht ist, und bereinigt die Daten, die der Sitzung zugeordnet sind.<br/> Das Festlegen eines kurzen Sitzungs Timeouts kann ein Problem für Upload-Antwort-Aufträge sein, da die Antwort nur heruntergeladen wird, wenn der Benutzer angemeldet und mit dem Netzwerk verbunden ist. Es ist möglich, dass für die Sitzung ein Timeout auftritt, bevor die Antwort heruntergeladen wird. in diesem Fall wird die Sitzung abgebrochen, und die Antwortdatei wird gelöscht.<br/> Beachten Sie, dass Bits den Auftrag abbricht, wenn der Wert von " <a href="/windows/win32/bits/group-policies">jobinactivitytimeout</a> Gruppenrichtlinie" (Standardwert: 90 Tage) unabhängig von dieser Einstellung erreicht wird.<br/> Der Standardwert ist 1.209.600 (14 Tage).<br/></td>
</tr>
<tr class="odd">
<td><strong>Bizmaximumuploadsize</strong> Datentyp: <strong>Zeichenfolge</strong><br/></td>
<td>Maximale Anzahl von Bytes, die pro Auftrag hochgeladen werden können. Geben Sie die maximale Anzahl von Bytes als Dezimal Zeichenfolge an. der Zeichen folgen Wert muss kleiner oder gleich 1844674407370955 sein &quot; &quot; . Eine leere Zeichenfolge ist mit der Angabe von &quot; 1844674407370955 identisch &quot; .<br/> Der Standardwert ist eine leere Zeichenfolge.<br/>
<blockquote>
[!Note]<br />
In IIS 7 beträgt das standardmäßige Uploadlimit 30 Millionen Bytes. Der Wert der <strong>bitmaximumuploadsize</strong> -Eigenschaft darf das IIS-Limit nicht überschreiten. Weitere Informationen und Informationen zum Ändern der IIS-Standardeinstellungen finden Sie unter <a href="https://support.microsoft.com//kb/942074">KB942074</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>Bitsservernotificationtype</strong> Datentyp: <strong>DWORD</strong><br/></td>
<td>Gibt an, wie die Uploaddatei an die Serveranwendung gesendet wird. Mögliche Werte sind: 0, 1 und 2.<br/> Der Wert 0 bedeutet, dass die Datei nicht an die Serveranwendung gesendet wird. Bits fügt die Uploaddatei in das Verzeichnis ein, das im Remote Namen angegeben ist (der Remote Name, der beim <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-addfile">Hinzufügen der Datei</a> zum Auftrag angegeben wurde), ohne die Serveranwendung zu benachrichtigen. Wenn die Datei derzeit im Zielverzeichnis vorhanden ist, wird Sie durch die Uploaddatei ersetzt.<br/> Der Wert 1 bedeutet, dass Bits den Speicherort der Uploaddatei an die in der Eigenschaft <strong>bitsservernotificationurl</strong> angegebene Serveranwendung übergibt. Die Serveranwendung verarbeitet die Datei und generiert bei Bedarf eine Antwortdatei. Standardmäßig entfernt Bits die Upload-und Antwort Dateien vom Server, nachdem die Antwort von der Serveranwendung empfangen wurde. Um Bits die Uploaddatei an den Speicherort zu kopieren, der durch den Remote Dateinamen im Auftrag angegeben ist, fügen Sie den <a href="/windows/win32/bits/notification-protocol-for-server-applications">Bits-Copy-File-to-Destination-</a> Header in die Antwort ein. Wenn Sie den-Header nicht einschließen und die Upload-und Antwort Dateien speichern möchten, müssen Sie die Upload-und die Antwort Dateien vor der Antwort an einen neuen Speicherort kopieren.<br/> Der Wert 2 bedeutet, dass Bits die Uploaddatei im Anforderungs Text an die in der Eigenschaft <strong>bitsservernotificationurl</strong> angegebene Serveranwendung übergibt. Die Serveranwendung verarbeitet die Datei und übergibt Sie bei Bedarf im Text der Antwort zurück.<br/> Ausführliche Informationen zu den Anforderungs-und Antwort Headern finden Sie unter <a href="/windows/win32/bits/notification-protocol-for-server-applications">Benachrichtigungs Protokoll für Server Anwendungen</a>.<br/> Die Serveranwendung muss innerhalb von fünf Minuten eine Antwort bereitstellen. Wenn die Serveranwendung nicht innerhalb von fünf Minuten antwortet, wechselt der Auftrag in den vorübergehenden Fehlerzustand. Wenn die <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay"><strong>Wiederholungs Verzögerung</strong></a> abläuft, sendet der BITS-Server eine weitere Benachrichtigung an die Serveranwendung (die Serveranwendung muss geschrieben werden, um doppelte Benachrichtigungen zu verarbeiten). <strong>Bits 1,5:</strong> Das Benachrichtigungs Timeout beträgt 30 Sekunden.<br/> <br/> Der Standardwert ist 0.<br/></td>
</tr>
<tr class="odd">
<td><strong>Bitsservernotificationurl</strong> Datentyp: <strong>Zeichenfolge</strong><br/></td>
<td>Dies ist optional. Enthält die URL der Serveranwendung, an die Bits die Uploaddatei sendet. Sie müssen eine URL angeben, wenn der Wert der Eigenschaft <strong>bitsservernotificationtype</strong> 1 oder 2 ist. Die URL ist auf 2.200 Zeichen beschränkt, ohne das NULL-Terminator. Die URL muss eine HTTP-URL sein. Bits unterstützt keine HTTPS-Benachrichtigungs-URLs.<br/> Wenn die URL zum Zeitpunkt des Uploads nicht verfügbar ist, führt Bits den Upload erneut aus, bis die Benachrichtigungs-URL vorhanden ist oder bis der Wiederholungs Zeitraum abläuft.<br/> Beachten Sie Folgendes: Wenn der im Auftrag angegebene Remote Name eine Abfrage Zeichenfolge enthält, wird die Abfrage Zeichenfolge an die von Ihnen angegebene URL angehängt. Wenn z. b. der Remote Name enthält https://myserver/myvdir/subdir/file.asp?ACCOUNT=86433 und Sie die Einstellung " <strong>bitsservernotificationurl</strong> " als angeben https://otherserver/myvdir2/bag.asp , ist die URL, an die Bits-Beiträge gesendet werden https://otherserver/myvdir2/bag.asp?ACCOUNT=86433 .<br/> Wenn die ursprüngliche URL lautet https://myserver/myvdir/file.txt und die Benachrichtigungs-URL myasp. asp lautet, verwendet Bits http//MyServer/MyVDir/myasp. ASP als Benachrichtigungs-URL.<br/> Wenn der Pfad und der Dateiname der URL Unicode-Zeichen enthalten, die nicht gemeinsam mit der Codepage auf dem Client und dem Server verwendet werden, schlägt die URL-Übersetzung auf dem Server fehl, und der BITS-Auftrag wird in den Fehlerzustand versetzt. Wenn der Serverteil der URL Unicode-Zeichen enthält, müssen Sie den Serverteil mithilfe von <a href="/windows/win32/intl/handling-internationalized-domain-names--idns">internationalisierten Domänen Namen</a> (IDN) codieren.<br/></td>
</tr>
<tr class="even">
<td><strong>Bitshostid</strong> Datentyp: <strong>Zeichenfolge</strong><br/></td>
<td>Legen Sie diese Eigenschaft fest, wenn die Server Installation eine Webfarm ist, die keinen freigegebenen Speicher verwendet.<br/> Geben Sie den Servernamen oder die IP-Adresse des Servers an, mit dem die Verbindung wieder hergestellt werden soll, wenn der Uploadvorgang In der Regel geben Sie den Namen des Servers an, den Sie konfigurieren. Die URL ist auf 300 Zeichen beschränkt, ohne das NULL-Terminator.<br/> Wenn Sie diese Eigenschaft nicht angeben und der Uploadvorgang unterbrochen wird, können Bits den Auftrag auf einem anderen Server in der Farm fortsetzen. Der vorherige Server enthält jedoch noch die partielle Uploaddatei vor der Unterbrechung. Bits entfernt die partielle Datei nach Ablauf von <strong>bitssessiontimeout</strong> .<br/>
<blockquote>
[!Note]<br />
Verwenden Sie die Eigenschaft <strong>bitshostid</strong> nicht, wenn SSL in einer Webfarm verwendet wird, in der Netzwerk Lastenausgleich (NLB) oder DNS-Namen mit mehreren IP-Adressen verwendet werden, es sei denn, Sie fügen den Cluster Namen und die einzelnen Servernamen in das Zertifikat ein. (Wenn der in <strong>bitshostid</strong> angegebene Servername nicht mit dem allgemeinen Namen des Zertifikats identisch ist, kann der Auftrag nicht ausgeführt werden.) Legen Sie stattdessen für den NLB-Parameter den <a href="/previous-versions/tn-archive/bb687542(v=technet.10)">Affinitäts</a> Parameter auf " <strong>Single</strong> " fest, um sicherzustellen, dass der Client in Zukunft mit dem gleichen Server kommuniziert.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>Bitshostidfallbacktimeout</strong> Datentyp: <strong>DWORD</strong><br/></td>
<td>Die Anzahl der Sekunden, die der BITS-Client versucht, erneut eine Verbindung mit dem <strong>bitshostid-</strong> Servernamen herzustellen, bevor der im Remote Dateinamen des Auftrags angegebene Hostname wieder hergestellt wird. Der Timer beginnt, wenn Bits keine Verbindung mit dem <strong>bitshostid-</strong> Server herstellen kann. Der Zeitgeber wird zurückgesetzt, wenn der Client erfolgreich eine Verbindung mit dem Server herstellt.<br/> Beachten Sie, dass der Wert für keinen Fortschritts Timeout des Auftrags (siehe <a href="/windows/win32/api/bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout"><strong>ibackgroundcopyjob:: setnoprogresstimeout</strong></a>) länger ist als dieser Timeout Wert. Wenn dies nicht der Fall ist, schlägt der Auftrag fehl, bevor der Timeout Wert für das Fall Back<br/> Legen Sie diese Eigenschaft nur fest, wenn Sie die <strong>bitshostid-</strong> Eigenschaft festlegen.<br/> Der Standardwert ist 86.400 (1 Tag).<br/></td>
</tr>
<tr class="even">
<td><strong>Bitsallowoverschreibvorgänge</strong> Datentyp: <strong>Integer</strong><br/></td>
<td>Gibt an, ob eine Uploaddatei eine vorhandene Datei mit demselben Namen überschreiben kann. Die Uploaddatei überschreibt die vorhandene Datei, wenn <strong>bitsallowoverschreib</strong> den Wert 1 hat.<br/> Der Standardwert ist 0.<br/> <strong>IIS 6,0:</strong> Diese Eigenschaft kann nur von einem Skript festgelegt werden. Sie können Sie nicht über die Eigenschaften Seite für BITS-Erweiterungen in der IIS-Benutzeroberfläche festlegen.<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>Bitscleanupuot default</strong> Datentyp: <strong>boolescher</strong> Wert<br/></td>
<td>Gibt an, ob die Bereinigungs Aufgabe die Standard Zeitpläne verwendet. Der Cleanuptask wird standardmäßig alle 12 Stunden ausgeführt.<br/> Legen Sie auf 1 fest, um den Standard Zeitplan zu verwenden. andernfalls 0, um einen Zeitplan anzugeben.<br/> Um einen Zeitplan anzugeben, verwenden Sie die Eigenschaften <strong>bitscleanupcount</strong> und <strong>bitscleanupunits</strong> .<br/> Der Cleanuptask bereinigt das virtuelle Verzeichnis durch Löschen von Aufträgen, die innerhalb des Sitzungs Timeout Zeitraums nicht geändert wurden (siehe <strong>bitssessiontimeout</strong>).<br/> Der Standardwert ist 1. verwenden Sie den Standard Zeitplan.<br/> <strong>IIS 6,0:</strong> Nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><strong>Bitscleanupcount</strong> Datentyp: <strong>Integer</strong><br/></td>
<td>Gibt das Intervall an, das zwischen dem Ausführen der Bereinigungs Aufgabe gewartet werden soll. Welches Intervall Sie angeben können, hängt von den Einheiten ab. Mögliche Intervall Werte finden Sie unter der <strong>bitscleanupunits</strong> -Eigenschaft.<br/> Diese Eigenschaft wird ignoriert, wenn <strong>bitscleanupuot default</strong> den Wert 0 hat.<br/> <strong>IIS 6,0:</strong> Nicht unterstützt.<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>Bitscleanupunits</strong> Datentyp: <strong>Integer</strong><br/></td>
<td>Gibt die Einheiten für das Bereinigungs Intervall an, das in der <strong>bitscleanupcount</strong> -Eigenschaft angegeben ist. Diese Eigenschaft wird ignoriert, wenn <strong>bitscleanupuot default</strong> den Wert 0 hat.<br/> Mögliche Werte sind:<dl> 0: die Einheiten sind Minuten. Mögliche Werte sind 1 bis 60.<br />
1: die Einheiten sind Stunden. Dies ist die Standardoption. Mögliche Werte sind 1 bis 24.<br />
2: die Einheiten sind Tage. Mögliche Werte sind 1 bis 360.<br />
</dl> <br/> <strong>IIS 6,0:</strong> Nicht unterstützt.<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>Bisnumofsessionslimit</strong> Datentyp: <strong>Integer</strong><br/></td>
<td>Schränkt die Anzahl von Uploadsitzungen ein, die für einen Benutzer gleichzeitig vorhanden sein können. Wenn die Anzahl der Sitzungen für einen Benutzer diesen Grenzwert überschreitet, werden beim Ausführen der Bereinigungs Aufgabe die letzten Sitzungen gelöscht, bis die Anzahl der Sitzungen für den Benutzer unterhalb des Limits liegt.<br/> Der Standardwert ist 50 Sitzungen.<br/> <strong>IIS 6,0:</strong> Nicht unterstützt.<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>Bitssessionlimitenable</strong> Datentyp: <strong>boolescher</strong> Wert<br/></td>
<td>Gibt an, ob Bits die Anzahl von Uploadsitzungen pro Benutzer einschränkt. Wenn die Einstellung nicht vorhanden ist oder den Wert 0 hat, ist das Limit deaktiviert.<br/> Um das Limit anzugeben, legen Sie die Eigenschaft <strong>bitnumofsessionslimit</strong> fest.<br/> Der Standardwert ist 1.<br/> <strong>IIS 6,0:</strong> Nicht unterstützt.<br/> <br/></td>
</tr>
</tbody>
</table>



 

Im folgenden Beispiel wird gezeigt, wie die BITS-IIS-Erweiterungs Eigenschaften mithilfe von Windows Script Host festgelegt werden. Wenn das virtuelle Verzeichnis auf eine Remote Freigabe verweist, legen Sie auch die Eigenschaften **UNCUserName** und **UNCPassword** IIS fest.


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



 

