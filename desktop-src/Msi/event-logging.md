---
description: Windows-Ereignisse bieten eine standardmäßige, zentralisierte Methode für Anwendungen (und das Betriebssystem), um wichtige Software-und Hardware Ereignisse aufzuzeichnen.
ms.assetid: 1f28cbce-b759-4293-8af2-15f86f23228c
title: Ereignisprotokollierung (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7fdaf29ec0c638d3c85b82c74cca2bbede63c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755632"
---
# <a name="event-logging-windows-installer"></a>Ereignisprotokollierung (Windows Installer)

[Windows-Ereignisse](../events/windows-events.md) bieten eine standardmäßige, zentralisierte Methode für Anwendungen (und das Betriebssystem), um wichtige Software-und Hardware Ereignisse aufzuzeichnen. Der Ereignis Protokollierungs Dienst speichert Ereignisse aus verschiedenen Quellen in einer einzelnen Sammlung, die als *Ereignisprotokoll* bezeichnet wird. Vor Windows Vista verwenden Sie entweder die Ereignis Ablauf [Verfolgung für Windows (Event Tracing for Windows](../etw/event-tracing-portal.md) , etw) oder die [Ereignisprotokollierung](../eventlog/event-logging.md) zum Protokollieren von Ereignissen. In Windows Vista wurde ein neues Ereignis Modell eingeführt, das sowohl die etw-als auch die [Windows-Ereignisprotokoll](../wes/windows-event-log.md) -API vereinheitlicht.

Das Installationsprogramm schreibt auch Einträge in das Ereignisprotokoll. Folgende Ereignisse werden aufgezeichnet:

-   Erfolg oder Fehler bei der Installation. Entfernen oder Reparieren eines Produkts.
-   Fehler, die während der Produktkonfiguration auftreten.
-   Erkennung von beschädigten Konfigurationsdaten.

Wenn eine große Menge an Informationen geschrieben wird, kann die Ereignisprotokoll Datei voll sein, und das Installationsprogramm zeigt die Meldung an, dass die Anwendungsprotokoll Datei voll ist.

Der Installer kann die folgenden Einträge im Ereignisprotokoll schreiben. Alle Ereignisprotokoll Meldungen weisen eine eindeutige Ereignis-ID auf. Alle allgemeinen Fehler, die in der [Fehler Tabelle](error-table.md) erstellt wurden, die für eine fehlgeschlagene Installation zurückgegeben werden, werden im Anwendungs Ereignisprotokoll mit einer Nachrichten-ID, die dem Fehler + 10.000 entspricht, protokolliert. Beispielsweise ist die Fehlernummer in der Fehler Tabelle für eine Installation erfolgreich abgeschlossen. 1707. Die erfolgreiche Installation wird im Anwendungs Ereignisprotokoll mit der Nachrichten-ID 11707 (1707 + 10.000) protokolliert.

Informationen dazu, wie Sie die ausführliche Protokollierung auf dem Computer eines Benutzers bei der Problembehandlung von bereit Stellungen aktivieren, finden Sie unter [Windows Installer bewährten Methoden](windows-installer-best-practices.md).



<table>
<thead>
<tr class="header">
<th>Ereignis-ID</th>
<th>`Message`</th>
<th>Bemerkungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1001</td>
<td>Fehler bei der Erkennung von Produkt "%1", Funktion "%2" während der Anforderung für die Komponente "%3".</td>
<td>Eine Warnmeldung. Weitere Informationen finden Sie unter <a href="searching-for-a-broken-feature-or-component.md">Suchen nach einer unterbrochenen Funktion oder Komponente</a>.</td>
</tr>
<tr class="even">
<td>1002</td>
<td>Unerwarteter oder fehlender Wert (Name: ' %1 ', Wert: ' %2 ') im Schlüssel ' %3 '.</td>
<td>Fehlermeldung, dass ein unerwarteter oder fehlender Wert vorhanden war.</td>
</tr>
<tr class="odd">
<td>1003</td>
<td>Unerwarteter oder fehlender Unterschlüssel "%1" im Schlüssel "%2".</td>
<td>Fehlermeldung, dass ein unerwarteter oder fehlender Unterschlüssel vorhanden war.</td>
</tr>
<tr class="even">
<td>1004</td>
<td>Fehler bei der Erkennung von Produkt "%1", Funktion "%2", Komponente "%3" <strong>:</strong> ab Windows Installer Version 2,0 lautet diese Meldung: Erkennung von Produkt "%1", Funktion "%2", Komponente "%3". Die Ressource "%4" ist nicht vorhanden.<br/></td>
<td>Eine Warnmeldung. Siehe auch <a href="searching-for-a-broken-feature-or-component.md">Suchen nach einer unterbrochenen Funktion oder Komponente</a>.</td>
</tr>
<tr class="odd">
<td>1005</td>
<td>Der Installationsvorgang hat einen Neustart initiiert.</td>
<td>Informations Meldung, dass bei der Installation ein Neustart des Systems initiiert wurde.</td>
</tr>
<tr class="even">
<td>1006</td>
<td>Die Überprüfung der digitalen Signatur für die CAB-"%1" kann nicht ausgeführt werden. WinVerifyTrust ist auf dem Computer nicht verfügbar.</td>
<td>Warnmeldung. In der <a href="msidigitalsignature-table.md">Tabelle "msidigitalsignature</a> " wurde eine CAB-Datei erstellt, um eine <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust"><strong>WinVerifyTrust</strong></a> -Prüfung durchzuführen. Diese Aktion konnte nicht ausgeführt werden, da auf dem Computer nicht die richtigen kryptografiedlls installiert sind.</td>
</tr>
<tr class="odd">
<td>1007</td>
<td>Die Installation von "%1" ist durch die Software Einschränkungs Richtlinie nicht zulässig. Der Windows Installer ermöglicht nur die Ausführung uneingeschränkter Elemente. Die von der Software Einschränkungs Richtlinie zurückgegebene Autorisierungs Ebene war %2.</td>
<td>Eine Fehlermeldung, die angibt, dass der Administrator die Software Einschränkungs Richtlinie so konfiguriert hat, dass diese Installation nicht zugelassen wird</td>
</tr>
<tr class="even">
<td>1008</td>
<td>Die Installation von %1 ist aufgrund eines Fehlers bei der Verarbeitung der Software Einschränkungs Richtlinie nicht zulässig. Das Objekt kann nicht als vertrauenswürdig eingestuft werden.</td>
<td>Eine Fehlermeldung, die angibt, dass beim Versuch, das Paket gemäß der Software Einschränkungs Richtlinie zu überprüfen, Probleme aufgetreten sind.</td>
</tr>
<tr class="odd">
<td>1012</td>
<td>Diese Windows-Version unterstützt die Bereitstellung von 64-Bit-Paketen nicht. Das Skript "%1" ist für ein 64-Bit-Paket vorgesehen.</td>
<td>Eine Fehlermeldung, die angibt, dass Skripts für 64-Bit-Pakete nur auf einem 64-Bit-Computer ausgeführt werden können.</td>
</tr>
<tr class="even">
<td>1013</td>
<td>{Nicht behandelter Ausnahme Bericht}</td>
<td>Fehlermeldung für eine nicht behandelte Ausnahme, dies ist der Bericht.</td>
</tr>
<tr class="odd">
<td>1014</td>
<td>Windows Installer Proxy Informationen sind nicht ordnungsgemäß registriert.</td>
<td>Fehlermeldung, dass die Proxy Informationen nicht ordnungsgemäß registriert wurden.</td>
</tr>
<tr class="even">
<td>1015</td>
<td>Fehler beim Herstellen einer Verbindung mit dem Server. Fehler:% d</td>
<td>Informations Meldung, dass bei der Installation keine Verbindung mit dem Server hergestellt werden konnte.</td>
</tr>
<tr class="odd">
<td>1016</td>
<td>Die Erkennung von Produkt "%1", Funktion "%2", Komponente "%3" ist fehlgeschlagen. Die Ressource "%4" in einer Komponente aus der Quell Komponente konnte nicht gefunden werden, da keine gültige und barrierefreie Quelle gefunden werden konnte.</td>
<td>Warnmeldung. Weitere Informationen finden Sie unter <a href="searching-for-a-broken-feature-or-component.md">Suchen nach einer unterbrochenen Funktion oder Komponente</a>.</td>
</tr>
<tr class="even">
<td>1017</td>
<td>Die Benutzer-SID wurde von "%1" in "%2" geändert, aber die verwaltete APP und die Benutzerdaten Schlüssel können nicht aktualisiert werden. Fehler = ' %3 '.</td>
<td>Eine Fehlermeldung, die angibt, dass beim Versuch, die Registrierung des Benutzers zu aktualisieren, nach dem Ändern der SID des Benutzers ein Fehler aufgetreten ist.</td>
</tr>
<tr class="odd">
<td>1018</td>
<td>Die Anwendung "%1" kann nicht installiert werden, da Sie mit dieser Windows-Version nicht kompatibel ist.</td>
<td>Eine Fehlermeldung, die angibt, dass die Installation nicht mit der aktuell ausgeführt Version von Windows kompatibel ist. Wenden Sie sich an den Hersteller der Software, die für ein Update installiert wird.</td>
</tr>
<tr class="even">
<td>1019</td>
<td>Produkt: %1-das Update "%2" wurde erfolgreich entfernt.</td>
<td>Informations Meldung, dass das Update vom Installationsprogramm entfernt wurde. <strong>Windows Installer 2,0:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1020</td>
<td>Produkt: %1-das Update "%2" konnte nicht entfernt werden. Fehlercode %3. Weitere Informationen finden Sie in der Protokolldatei "%4".</td>
<td>Eine Fehlermeldung, die angibt, dass das Installationsprogramm das Update nicht entfernen konnte. Weitere Informationen finden Sie in der Protokolldatei. <strong>Windows Installer 2,0:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>1021</td>
<td>Produkt: %1-das Update "%2" konnte nicht entfernt werden. Fehlercode %3.</td>
<td>Eine Fehlermeldung, die angibt, dass das Installationsprogramm das Update nicht entfernen konnte. Informationen zum Aktivieren der Protokollierung finden Sie unter Aktivieren der ausführlichen <a href="windows-installer-best-practices.md">Protokollierung auf dem Computer des Benutzers bei der Problembehandlung für die Bereitstellung.</a> <strong>Windows Installer 2,0:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1022</td>
<td>Produkt: %1-das Update "%2" wurde erfolgreich installiert.</td>
<td>Informations Meldung, dass das Update vom Installationsprogramm erfolgreich installiert wurde. <strong>Windows Installer 2,0:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>1023</td>
<td>Produkt: %1-das Update "%2" konnte nicht installiert werden. Fehlercode %3. Weitere Informationen finden Sie in der Protokolldatei "%4".</td>
<td>Eine Fehlermeldung, die angibt, dass das Installationsprogramm das Update nicht installieren konnte. Weitere Informationen finden Sie in der Protokolldatei. <strong>Windows Installer 2,0:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1024</td>
<td>Produkt: %1-das Update "%2" konnte nicht installiert werden. Fehlercode %3.</td>
<td>Eine Fehlermeldung, die angibt, dass das Installationsprogramm das Update nicht installieren konnte. Informationen zum Aktivieren der Protokollierung finden Sie unter Aktivieren der ausführlichen <a href="windows-installer-best-practices.md">Protokollierung auf dem Computer des Benutzers bei der Problembehandlung für die Bereitstellung.</a> <strong>Windows Installer 2,0:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>1025</td>
<td>Produkt: %1. Die Datei "%2" wird von folgendem Prozess verwendet: Name: %3, ID: %4.</td>
<td><strong>Windows Installer 2,0:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1026</td>
<td>Windows Installer hat festgestellt, dass der Registrierungsschlüssel für die Konfigurationsdaten nicht ordnungsgemäß gesichert wurde. Der Besitzer des Schlüssels muss entweder "Lokales System" oder "VORDEFINIERT\Administratoren" sein. Der vorhandene Schlüssel wird gelöscht und mit den entsprechenden Sicherheitseinstellungen neu erstellt.</td>
<td>Warnmeldung. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 und früher</a>:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>1027</td>
<td>Windows Installer hat festgestellt, dass der Registrierungs Unterschlüssel %1 innerhalb der Konfigurationsdaten nicht ordnungsgemäß gesichert wurde. Der Besitzer des Schlüssels muss entweder "Lokales System" oder "VORDEFINIERT\Administratoren" sein. Der vorhandene Unterschlüssel und sein Inhalt werden gelöscht.</td>
<td>Warnmeldung. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 und früher</a>:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1028</td>
<td>Windows Installer hat festgestellt, dass der Konfigurationsdaten Cache Ordner nicht ordnungsgemäß gesichert wurde. Der Besitzer des Schlüssels muss entweder "Lokales System" oder "VORDEFINIERT\Administratoren" sein. Der vorhandene Ordner wird gelöscht und mit den entsprechenden Sicherheitseinstellungen neu erstellt.</td>
<td>Warnmeldung<strong><a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 und früher</a>:</strong> nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>1029</td>
<td>Produkt: %1. Neustart erforderlich.</td>
<td>Warnmeldung mit dem Hinweis, dass ein Neustart des Systems erforderlich ist, um die Installation abzuschließen, und der Neustart wurde zu einem späteren Zeitpunkt verzögert. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 und früher</a>:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1030</td>
<td>Produkt: %1. Die Anwendung hat versucht, eine neuere Version der geschützten Windows-Datei "%2" zu installieren. Möglicherweise müssen Sie Ihr Betriebssystem aktualisieren, damit diese Anwendung ordnungsgemäß funktioniert. (Paket Version: %3, vom Betriebs System geschützte Version: %4).</td>
<td>Eine Warnmeldung, die angibt, dass bei der Installation eine durch <a href="windows-resource-protection-on-windows-vista.md">Windows-Ressourcenschutz</a>geschützte kritische Datei ersetzt werden konnte. Zur Verwendung dieser Anwendung ist möglicherweise ein Update des Betriebssystems erforderlich. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 und früher</a>:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>1031</td>
<td>Produkt: %1. Die Assembly "%2" für die Komponente "%3" wird verwendet.</td>
<td>Warnmeldung, die angibt, dass bei der Installation versucht wurde, eine zurzeit verwendete Assembly zu aktualisieren. Das System muss neu gestartet werden, um das Update dieser Assembly abzuschließen. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 und früher</a>:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1032</td>
<td>Fehler beim Aktualisieren von Umgebungsvariablen, die während der Installation von "%1" aktualisiert wurden.</td>
<td>Eine Warnmeldung, die angibt, dass einige Benutzer, die am Computer angemeldet sind, sich möglicherweise ab-und wieder anmelden müssen, um das Update der Umgebungsvariablen abzuschließen. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 und früher</a>:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>1033</td>
<td>Produkt: %1. Version: %2. Sprache: %3. Die Installation wurde mit dem Status "%4" abgeschlossen. Hersteller: %5.</td>
<td>Feld 1- <a href="productname.md"><strong>ProductName</strong></a> Field 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Feld 3- <a href="productlanguage.md"> <strong>productlanguage</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 und früher</a>:</strong> Nicht verfügbar.<br/> Feld 5- <a href="manufacturer.md"> <strong>Hersteller</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 und früher</a>:</strong> Field 5 ist nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1034</td>
<td>Produkt: %1. Version: %2. Sprache: %3. Das Entfernen wurde mit dem Status "%4" abgeschlossen. Hersteller: %5.</td>
<td>Feld 1- <a href="productname.md"><strong>ProductName</strong></a> Field 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Feld 3- <a href="productlanguage.md"> <strong>productlanguage</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 und früher</a>:</strong> Nicht verfügbar.<br/> Feld 5- <a href="manufacturer.md"> <strong>Hersteller</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 und früher</a>:</strong> Field 5 ist nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>1035</td>
<td>Produkt: %1. Version: %2. Sprache: %3. Die Konfigurationsänderung wurde mit dem Status "%4" abgeschlossen. Hersteller: %5.</td>
<td>Feld 1- <a href="productname.md"><strong>ProductName</strong></a> Field 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Feld 3- <a href="productlanguage.md"> <strong>productlanguage</strong></a><br/> Feld 5- <a href="manufacturer.md"> <strong>Hersteller</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 und früher</a>:</strong> Field 5 ist nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1036</td>
<td>Produkt: %1. Version: %2. Sprache: %3. Update: %4. Die Update Installation wurde mit dem Status "%5" abgeschlossen. Hersteller: %6.</td>
<td>Feld 1- <a href="productname.md"><strong>ProductName</strong></a> Field 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Feld 3- <a href="productlanguage.md"> <strong>productlanguage</strong></a><br/> Feld 4: Dies ist der benutzerfreundliche Name, wenn die <a href="msipatchmetadata-table.md">MsiPatchMetadata-Tabelle</a> im Patchpaket vorhanden ist. Andernfalls ist dies die Patchcode-GUID des Patches.<br/> Feld 5: Status der Update Installation.<br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 und früher</a>:</strong> Nicht verfügbar.<br/> Feld 6- <a href="manufacturer.md"> <strong>Hersteller</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 und früher</a>:</strong> Feld 6 ist nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>1037</td>
<td>Produkt: %1. Version: %2. Sprache: %3. Update: %4. Das Entfernen des Updates wurde mit dem Status "%5" abgeschlossen. Hersteller: %6.</td>
<td>Feld 1- <a href="productname.md"><strong>ProductName</strong></a> Field 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Feld 3- <a href="productlanguage.md"> <strong>productlanguage</strong></a><br/> Feld 4: Dies ist der benutzerfreundliche Name, wenn die <a href="msipatchmetadata-table.md">MsiPatchMetadata-Tabelle</a> im Patchpaket vorhanden ist. Andernfalls ist dies die Patchcode-GUID des Patches.<br/> Feld 5: Status der Update Entfernung.<br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 und früher</a>:</strong> Nicht verfügbar.<br/> Feld 6- <a href="manufacturer.md"> <strong>Hersteller</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 und früher</a>:</strong> Feld 6 ist nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1038</td>
<td>Produkt: %1. Version: %2. Sprache: %3. Es ist ein Neustart erforderlich. Neustarttyp: %4. Grund für Neustart: %5. Hersteller: %6.</td>
<td>Feld 1- <a href="productname.md"><strong>ProductName</strong></a> Field 2- <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Feld 3- <a href="productlanguage.md"> <strong>productlanguage</strong></a><br/> <dl> Feld 4: eine-Konstante, die den Typ des Neustarts angibt: <br/> <dl> <strong>msirbrebootimvermittler</strong> (1): der Computer wurde sofort neu gestartet.<br />
<strong>msirbrebootverzögertes</strong> (2): ein Benutzer oder Administrator hat einen erforderlichen Neustart des Computers mithilfe der Benutzeroberfläche oder <a href="reboot.md"><strong>Neustart</strong></a>= "reallyunterdrückung" zurückgestellt.<br />
</dl> </dd> Field 5 - A constant indicating the reason for the restart:<br/> <dl> <strong>msirbrebootundeterminedreason</strong> (0): der Neustart ist aus einem nicht angegebenen Grund erforderlich.<br />
<strong>msirbrebootinusefilesreason</strong> (1): ein Neustart war erforderlich, um verwendete Dateien zu ersetzen.<br />
<strong>msirbrebootschedulerebooket</strong> (2): das Paket enthält eine <a href="schedulereboot-action.md">schedulereboot</a> -Aktion.<br />
<strong>msirbrebootforcerebooverrat</strong> (3): das Paket enthält eine <a href="forcereboot-action.md">ForceReboot</a> -Aktion.<br />
<strong>msirbrebootcustomaction Reason</strong> (4): eine benutzerdefinierte Aktion, die als <a href="/windows/desktop/api/Msiquery/nf-msiquery-msisetmode"><strong>msisetmode</strong></a> -Funktion bezeichnet wird.<br />
</dl> </dd> </dl> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3,1 und früher</a>:</strong> Nicht verfügbar.<br/> Feld 6- <a href="manufacturer.md"> <strong>Hersteller</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4,5 und früher</a>:</strong> Feld 6 ist nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>10005</td>
<td>Unerwarteter Fehler beim Installieren des Pakets. Dies weist auf ein Problem mit diesem Paket hin. Der Fehlercode ist [1]. {{Argumente: [2], [3], [4]}}</td>
<td>Fehlermeldung, die angibt, dass ein interner Fehler aufgetreten ist Der Text dieser Meldung basiert auf dem Text, der in der Fehler Tabelle für Fehler 5 erstellt wurde.</td>
</tr>
<tr class="odd">
<td>11707</td>
<td>Produkt [2] – der Installationsvorgang wurde erfolgreich abgeschlossen.</td>
<td>Informations Meldung, dass die Installation des Produkts erfolgreich war.</td>
</tr>
<tr class="even">
<td>11708</td>
<td>Produkt [2] – Installationsvorgang fehlgeschlagen</td>
<td>Fehlermeldung, dass bei der Installation des Produkts ein Fehler aufgetreten ist.</td>
</tr>
<tr class="odd">
<td>11728</td>
<td>Produkt [2]--die Konfiguration wurde erfolgreich abgeschlossen.</td>
<td>Informations Meldung, dass die Konfiguration des Produkts erfolgreich war.</td>
</tr>
</tbody>
</table>



 

Sie können mit Msidb.exe oder [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)lokalisierte Fehler Zeichenfolgen für Ereignisse in die-Datenbank importieren. Das SDK schließt lokalisierte Ressourcen Zeichenfolgen für jede der Sprachen ein, die im Abschnitt [lokalisieren der Fehler-und Aktions Text Tabellen](localizing-the-error-and-actiontext-tables.md) aufgeführt sind. Wenn die Fehler Zeichenfolgen, die den Ereignissen entsprechen, nicht aufgefüllt werden, lädt das Installationsprogramm lokalisierte Zeichen folgen für die durch die [**productlanguage**](productlanguage.md) -Eigenschaft angegebene Sprache.

 

 
