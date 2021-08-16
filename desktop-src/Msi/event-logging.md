---
description: Windows Ereignisse bieten eine standardisierte, zentralisierte Möglichkeit für Anwendungen (und das Betriebssystem), wichtige Software- und Hardwareereignisse aufzuzeichnen.
ms.assetid: 1f28cbce-b759-4293-8af2-15f86f23228c
title: Ereignisprotokollierung (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c1aa4808727a220ec104cb3e7bfdff2741dcb2366ca1468288a082baab813b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636924"
---
# <a name="event-logging-windows-installer"></a>Ereignisprotokollierung (Windows Installer)

[Windows Events](../events/windows-events.md) bietet eine standardisierte, zentralisierte Möglichkeit für Anwendungen (und das Betriebssystem), wichtige Software- und Hardwareereignisse aufzuzeichnen. Der Ereignisprotokollierungsdienst speichert Ereignisse aus verschiedenen Quellen in einer einzelnen Sammlung, die als Ereignisprotokoll bezeichnet *wird.* Vor Windows Vista verwendeten Sie entweder [die Ereignisablaufverfolgung für Windows](../etw/event-tracing-portal.md) (ETW) oder die [Ereignisprotokollierung,](../eventlog/event-logging.md) um Ereignisse zu protokollieren. Windows Vista hat ein neues Ereignismodell eingeführt, das sowohl ETW als auch die [Windows Ereignisprotokoll-API](../wes/windows-event-log.md) vereinheitlicht.

Das Installationsprogramm schreibt auch Einträge in das Ereignisprotokoll. Diese zeichnen Ereignisse wie die folgenden auf:

-   Erfolg oder Fehler der Installation; Entfernen oder Reparieren eines Produkts.
-   Fehler, die während der Produktkonfiguration auftreten.
-   Erkennung beschädigter Konfigurationsdaten.

Wenn eine große Menge an Informationen geschrieben wird, kann die Ereignisprotokolldatei voll werden, und das Installationsprogramm zeigt die Meldung "Die Anwendungsprotokolldatei ist voll" an.

Das Installationsprogramm kann die folgenden Einträge in das Ereignisprotokoll schreiben. Alle Ereignisprotokollmeldungen verfügen über eine eindeutige Ereignis-ID. Alle allgemeinen Fehler, die in der [Fehlertabelle](error-table.md) erstellt wurden und für eine installation zurückgegeben werden, bei der ein Fehler auftritt, werden im Anwendungsereignisprotokoll mit einer Meldungs-ID protokolliert, die dem Fehler + 10.000 entspricht. Die Fehlernummer in der Tabelle Fehler für eine erfolgreiche Installation lautet beispielsweise 1707. Die erfolgreiche Installation wird im Anwendungsereignisprotokoll mit der Meldungs-ID 11707 (1707 + 10.000) protokolliert.

Informationen zum Aktivieren der ausführlichen Protokollierung auf dem Computer eines Benutzers bei der Problembehandlung bei der Bereitstellung finden Sie unter [Windows Installer Best Practices](windows-installer-best-practices.md).



<table>
<thead>
<tr class="header">
<th>Ereignis-ID</th>
<th>`Message`</th>
<th>Hinweise</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1001</td>
<td>Fehler bei der Erkennung des Produkts "%1", Feature "%2" während der Anforderung der Komponente "%3"</td>
<td>Eine Warnmeldung. Weitere Informationen finden Sie unter <a href="searching-for-a-broken-feature-or-component.md">Suchen nach einer fehlerhaften Funktion oder Komponente.</a></td>
</tr>
<tr class="even">
<td>1002</td>
<td>Unerwarteter oder fehlender Wert (Name: '%1', Wert: '%2') im Schlüssel '%3'</td>
<td>Fehlermeldung, dass ein unerwarteter oder fehlender Wert aufgetreten ist.</td>
</tr>
<tr class="odd">
<td>1003</td>
<td>Unerwarteter oder fehlender Unterschlüssel '%1' in Schlüssel '%2'</td>
<td>Fehlermeldung, dass ein unerwarteter oder fehlender Unterschlüssel vorhanden war.</td>
</tr>
<tr class="even">
<td>1004</td>
<td>Erkennung des Produkts "%1", Feature "%2", Komponente "%3" fehlgeschlagen <strong>Hinweis:</strong> Ab Windows Installer Version 2.0 lautet diese Meldung: Fehler bei der Erkennung des Produkts "%1", Feature "%2", Komponente "%3". Die Ressource '%4' ist nicht vorhanden.<br/></td>
<td>Eine Warnmeldung. Siehe auch <a href="searching-for-a-broken-feature-or-component.md">Suchen nach einer fehlerhaften Funktion oder Komponente.</a></td>
</tr>
<tr class="odd">
<td>1005</td>
<td>Installationsvorgang initiiert einen Neustart</td>
<td>Informationsmeldung, dass die Installation einen Neustart des Systems initiiert hat.</td>
</tr>
<tr class="even">
<td>1006</td>
<td>Die Überprüfung der digitalen Signatur für das "%1"-Gehäuse kann nicht durchgeführt werden. WinVerifyTrust ist auf dem Computer nicht verfügbar.</td>
<td>Warnmeldung. In der <a href="msidigitalsignature-table.md">Tabelle MsiDigitalSignature</a> wurde ein Schränk erstellt, um eine <a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust"><strong>WinVerifyTrust-Überprüfung</strong></a> durchzuführen. Diese Aktion konnte nicht ausgeführt werden, da auf dem Computer nicht die richtigen Kryptografie-DLLs installiert sind.</td>
</tr>
<tr class="odd">
<td>1007</td>
<td>Die Installation von %1 ist durch die Softwareeinschränkungsrichtlinie nicht zulässig. Der Windows Installer lässt nur die Ausführung uneingeschränkter Elemente zu. Die von der Softwareeinschränkungsrichtlinie zurückgegebene Autorisierungsebene war %2.</td>
<td>Eine Fehlermeldung, die angibt, dass der Administrator die Softwareeinschränkungsrichtlinie konfiguriert hat, um diese Installation zu verhindern.</td>
</tr>
<tr class="even">
<td>1008</td>
<td>Die Installation von %1 ist aufgrund eines Fehlers bei der Verarbeitung von Softwareeinschränkungsrichtlinien nicht zulässig. Das Objekt kann nicht als vertrauenswürdig eingestuft werden.</td>
<td>Eine Fehlermeldung, die angibt, dass beim Versuch, das Paket gemäß der Softwareeinschränkungsrichtlinie zu überprüfen, Probleme aufgetreten sind.</td>
</tr>
<tr class="odd">
<td>1012</td>
<td>Diese Version von Windows unterstützt nicht die Bereitstellung von 64-Bit-Paketen. Das Skript '%1' ist für ein 64-Bit-Paket vorgesehen.</td>
<td>Fehlermeldung, die angibt, dass Skripts für 64-Bit-Pakete nur auf einem 64-Bit-Computer ausgeführt werden können.</td>
</tr>
<tr class="even">
<td>1013</td>
<td>{Nicht behandelter Ausnahmebericht}</td>
<td>Fehlermeldung für eine nicht behandelte Ausnahme. Dies ist der Bericht.</td>
</tr>
<tr class="odd">
<td>1014</td>
<td>Windows Proxyinformationen des Installationsprogramms nicht ordnungsgemäß registriert</td>
<td>Fehlermeldung, dass Proxyinformationen nicht ordnungsgemäß registriert wurden.</td>
</tr>
<tr class="even">
<td>1015</td>
<td>Fehler beim Herstellen einer Verbindung mit dem Server. Fehler: %d</td>
<td>Informationsmeldung, dass bei der Installation keine Verbindung mit dem Server hergestellt werden konnte.</td>
</tr>
<tr class="odd">
<td>1016</td>
<td>Fehler bei der Erkennung des Produkts "%1", Feature "%2", Komponente "%3". Die Ressource '%4' in einer Run-from-Source-Komponente konnte nicht gefunden werden, da keine gültige und zugängliche Quelle gefunden wurde.</td>
<td>Warnmeldung. Weitere Informationen finden Sie unter <a href="searching-for-a-broken-feature-or-component.md">Suchen nach einem fehlerhaften Feature oder einer komponente</a>.</td>
</tr>
<tr class="even">
<td>1017</td>
<td>Die Benutzer-SID wurde von "%1" in "%2" geändert, aber die verwaltete App und die Benutzerdatenschlüssel können nicht aktualisiert werden. Fehler = '%3'.</td>
<td>Fehlermeldung, die angibt, dass beim Versuch, die Registrierung des Benutzers zu aktualisieren, ein Fehler aufgetreten ist, nachdem die SID des Benutzers geändert wurde.</td>
</tr>
<tr class="odd">
<td>1018</td>
<td>Die '%1'-Anwendung kann nicht installiert werden, da sie nicht mit dieser Version von Windows kompatibel ist.</td>
<td>Fehlermeldung, die angibt, dass die Installation nicht mit der derzeit ausgeführten Version von Windows kompatibel ist. Wenden Sie sich an den Hersteller der Software, die für ein Update installiert wird.</td>
</tr>
<tr class="even">
<td>1019</td>
<td>Produkt: %1 – Update '%2' wurde erfolgreich entfernt.</td>
<td>Informationsmeldung, dass das Update vom Installationsprogramm entfernt wurde. <strong>Windows Installer 2.0:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1020</td>
<td>Produkt: %1 – Update '%2' konnte nicht entfernt werden. Fehlercode %3. Zusätzliche Informationen sind in der Protokolldatei %4 verfügbar.</td>
<td>Fehlermeldung, die angibt, dass das Update vom Installationsprogramm nicht entfernt werden konnte. Zusätzliche Informationen sind in der Protokolldatei verfügbar. <strong>Windows Installer 2.0:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>1021</td>
<td>Produkt: %1 – Update '%2' konnte nicht entfernt werden. Fehlercode %3.</td>
<td>Fehlermeldung, die angibt, dass das Update vom Installationsprogramm nicht entfernt werden konnte. Informationen zum Aktivieren der Protokollierung finden Sie unter Aktivieren der <a href="windows-installer-best-practices.md">ausführlichen Protokollierung auf dem Computer des Benutzers bei der Problembehandlung bei der Bereitstellung.</a> <strong>Windows Installer 2.0:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1022</td>
<td>Produkt: %1 – Update '%2' erfolgreich installiert.</td>
<td>Informationsmeldung, dass das Update vom Installationsprogramm erfolgreich installiert wurde. <strong>Windows Installer 2.0:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>1023</td>
<td>Produkt: %1 – Update '%2' konnte nicht installiert werden. Fehlercode %3. Weitere Informationen finden Sie in der Protokolldatei %4.</td>
<td>Fehlermeldung, die angibt, dass das Installationsprogramm das Update nicht installieren konnte. Weitere Informationen finden Sie in der Protokolldatei. <strong>Windows Installer 2.0:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1024</td>
<td>Produkt: %1 – Update '%2' konnte nicht installiert werden. Fehlercode %3.</td>
<td>Fehlermeldung, die angibt, dass das Installationsprogramm das Update nicht installieren konnte. Informationen zum Aktivieren der Protokollierung finden Sie unter Aktivieren der ausführlichen Protokollierung auf dem Computer des Benutzers <a href="windows-installer-best-practices.md">bei der Problembehandlung bei der Bereitstellung.</a> <strong>Windows Installer 2.0:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>1025</td>
<td>Produkt: %1. Die Datei %2 wird von folgendem Prozess verwendet: Name: %3, Id %4.</td>
<td><strong>Windows Installer 2.0:</strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1026</td>
<td>Windows Das Installationsprogramm hat festgestellt, dass sein Registrierungsschlüssel für Konfigurationsdaten nicht ordnungsgemäß gesichert wurde. Der Besitzer des Schlüssels muss entweder Lokales System oder Builtin\Administrators sein. Der vorhandene Schlüssel wird gelöscht und mit den entsprechenden Sicherheitseinstellungen neu erstellt.</td>
<td>Warnmeldung. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 und früher:</a></strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>1027</td>
<td>Windows Das Installationsprogramm hat festgestellt, dass ein Registrierungsunterschlüssel %1 innerhalb seiner Konfigurationsdaten nicht ordnungsgemäß gesichert wurde. Der Besitzer des Schlüssels muss entweder Lokales System oder Builtin\Administrators sein. Der vorhandene Unterschlüssel und sein sämtlicher Inhalt werden gelöscht.</td>
<td>Warnmeldung. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 und früher:</a></strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1028</td>
<td>Windows Das Installationsprogramm hat festgestellt, dass der Konfigurationsdatencacheordner nicht ordnungsgemäß gesichert wurde. Der Besitzer des Schlüssels muss entweder Lokales System oder Builtin\Administrators sein. Der vorhandene Ordner wird gelöscht und mit den entsprechenden Sicherheitseinstellungen neu erstellt.</td>
<td>Warnmeldung Windows<strong><a href="not-supported-in-windows-installer-version-3-1.md">Installer 3.1 und früher:</a></strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>1029</td>
<td>Produkt: %1. Neustart erforderlich.</td>
<td>Warnmeldung, die angibt, dass ein Systemneustart erforderlich ist, um die Installation abzuschließen, und der Neustart zu einem späteren Zeitpunkt verzögert wurde. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 und früher:</a></strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1030</td>
<td>Produkt: %1. Die Anwendung hat versucht, eine neuere Version der geschützten Datei Windows %2 zu installieren. Möglicherweise müssen Sie Ihr Betriebssystem aktualisieren, damit diese Anwendung ordnungsgemäß funktioniert. (Paketversion: %3, Durch das Betriebssystem geschützte Version: %4).</td>
<td>Warnmeldung, die angibt, dass bei der Installation versucht wurde, eine kritische Datei zu ersetzen, die durch Windows <a href="windows-resource-protection-on-windows-vista.md">Resource Protection geschützt ist.</a> Für die Verwendung dieser Anwendung ist möglicherweise ein Update des Betriebssystems erforderlich. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 und früher:</a></strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>1031</td>
<td>Produkt: %1. Die Assembly '%2' für die Komponente '%3' wird verwendet.</td>
<td>Warnmeldung, die angibt, dass bei der Installation versucht wurde, eine aktuell verwendete Assembly zu aktualisieren. Das System muss neu gestartet werden, um das Update dieser Assembly abschließen zu können. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 und früher:</a></strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1032</td>
<td>Fehler beim Aktualisieren von Umgebungsvariablen, die während der Installation von '%1' aktualisiert wurden.</td>
<td>Warnmeldung, die angibt, dass einige Benutzer, die am Computer angemeldet sind, sich möglicherweise ab- und wieder anmelden müssen, um das Update der Umgebungsvariablen abschließen zu können. <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 und früher:</a></strong> Nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>1033</td>
<td>Produkt: %1. Version: %2. Sprache: %3. Die Installation wurde mit dem Status %4 abgeschlossen. Hersteller: %5.</td>
<td>Feld 1 – <a href="productname.md"><strong>ProductName-Feld</strong></a> 2 – <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Feld 3 : <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 und früher:</a></strong> Nicht verfügbar.<br/> Feld 5 – <a href="manufacturer.md"> <strong>Hersteller</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 und früher:</a></strong> Feld 5 nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1034</td>
<td>Produkt: %1. Version: %2. Sprache: %3. Die Entfernung wurde mit dem Status %4 abgeschlossen. Hersteller: %5.</td>
<td>Feld 1 – <a href="productname.md"><strong>ProductName-Feld</strong></a> 2 – <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Feld 3 : <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 und früher:</a></strong> Nicht verfügbar.<br/> Feld 5 – <a href="manufacturer.md"> <strong>Hersteller</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 und früher:</a></strong> Feld 5 nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>1035</td>
<td>Produkt: %1. Version: %2. Sprache: %3. Die Konfigurationsänderung wurde mit dem Status %4 abgeschlossen. Hersteller: %5.</td>
<td>Feld 1 – <a href="productname.md"><strong>ProductName-Feld</strong></a> 2 – <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Feld 3 : <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Feld 5 – <a href="manufacturer.md"> <strong>Hersteller</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 und früher:</a></strong> Feld 5 nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1036</td>
<td>Produkt: %1. Version: %2. Sprache: %3. Update: %4. Die Updateinstallation wurde mit dem Status %5 abgeschlossen. Hersteller: %6.</td>
<td>Feld 1 – <a href="productname.md"><strong>ProductName-Feld</strong></a> 2 – <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Feld 3 : <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Feld 4: Dies ist der benutzerfreundliche Name, wenn die <a href="msipatchmetadata-table.md">MsiPatchMetadata-Tabelle</a> im Patchpaket vorhanden ist. Andernfalls ist dies die Patchcode-GUID des Patches.<br/> Feld 5: Status der Updateinstallation.<br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 und früher:</a></strong> Nicht verfügbar.<br/> Feld 6 – <a href="manufacturer.md"> <strong>Hersteller</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 und früher:</a></strong> Feld 6 nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>1037</td>
<td>Produkt: %1. Version: %2. Sprache: %3. Update: %4. Das Entfernen des Updates wurde mit dem Status %5 abgeschlossen. Hersteller: %6.</td>
<td>Feld 1 – <a href="productname.md"><strong>ProductName-Feld</strong></a> 2 – <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Feld 3 : <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> Feld 4: Dies ist der benutzerfreundliche Name, wenn die <a href="msipatchmetadata-table.md">MsiPatchMetadata-Tabelle</a> im Patchpaket vorhanden ist. Andernfalls ist dies die Patchcode-GUID des Patches.<br/> Feld 5: Status der Updateentfernung.<br/> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 und früher:</a></strong> Nicht verfügbar.<br/> Feld 6 – <a href="manufacturer.md"> <strong>Hersteller</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 und früher:</a></strong> Feld 6 nicht verfügbar.<br/></td>
</tr>
<tr class="odd">
<td>1038</td>
<td>Produkt: %1. Version: %2. Sprache: %3. Es ist ein Neustart erforderlich. Neustarttyp: %4. Neustartgrund: %5. Hersteller: %6.</td>
<td>Feld 1 – <a href="productname.md"><strong>ProductName-Feld</strong></a> 2 – <a href="productversion.md"><strong>ProductVersion</strong></a><br/> Feld 3 : <a href="productlanguage.md"> <strong>ProductLanguage</strong></a><br/> <dl> Feld 4: Eine Konstante, die den Typ des Neustarts angibt: <br/> <dl> <strong>msirbRebootImmediate</strong> (1): Der Computer wurde sofort neu gestartet.<br />
<strong>msirbRebootDeferred</strong> (2): Ein Benutzer oder Administrator hat einen erforderlichen Neustart des Computers über die Benutzeroberfläche oder <a href="reboot.md"><strong>REBOOT</strong></a>=ReallySuppress verzögert.<br />
</dl> </dd> Field 5 - A constant indicating the reason for the restart:<br/> <dl> <strong>msirbRebootUndeterminedReason</strong> (0): Neustart aus einem nicht angegebenen Grund erforderlich.<br />
<strong>msirbRebootInUseFilesReason</strong> (1): Ein Neustart war erforderlich, um die verwendeten Dateien zu ersetzen.<br />
<strong>msirbRebootScheduleRebootReason</strong> (2): Das Paket enthält eine <a href="schedulereboot-action.md">ScheduleReboot-Aktion.</a><br />
<strong>msirbRebootForceRebootReason</strong> (3): Das Paket enthält eine <a href="forcereboot-action.md">ForceReboot-Aktion.</a><br />
<strong>msirbRebootCustomActionReason</strong> (4): Eine benutzerdefinierte Aktion namens <a href="/windows/desktop/api/Msiquery/nf-msiquery-msisetmode"><strong>MsiSetMode-Funktion.</strong></a><br />
</dl> </dd> </dl> <strong> <a href="not-supported-in-windows-installer-version-3-1.md">Windows Installer 3.1 und früher:</a></strong> Nicht verfügbar.<br/> Feld 6 – <a href="manufacturer.md"> <strong>Hersteller</strong></a><br/> <strong> <a href="not-supported-in-windows-installer-4-5.md">Windows Installer 4.5 und früher:</a></strong> Feld 6 nicht verfügbar.<br/></td>
</tr>
<tr class="even">
<td>10005</td>
<td>Beim Installationsprogramm ist ein unerwarteter Fehler beim Installieren dieses Pakets aufgetreten. Dies weist auf ein Problem mit diesem Paket hin. Der Fehlercode ist [1]. {{Die Argumente sind: [2], [3], [4]}}</td>
<td>Fehlermeldung, die angibt, dass ein interner Fehler aufgetreten ist. Der Text dieser Meldung basiert auf dem Text, der für Fehler 5 in der Tabelle Error (Fehler) verfasst wurde.</td>
</tr>
<tr class="odd">
<td>11707</td>
<td>Produkt [2] – Installationsvorgang erfolgreich abgeschlossen</td>
<td>Informationsmeldung, dass die Installation des Produkts erfolgreich war.</td>
</tr>
<tr class="even">
<td>11708</td>
<td>Produkt [2] – Fehler beim Installationsvorgang</td>
<td>Fehlermeldung, dass bei der Installation des Produkts ein Fehler aufgetreten ist.</td>
</tr>
<tr class="odd">
<td>11728</td>
<td>Produkt [2] – Die Konfiguration wurde erfolgreich abgeschlossen.</td>
<td>Eine Informationsmeldung, dass die Konfiguration des Produkts erfolgreich war.</td>
</tr>
</tbody>
</table>



 

Sie können lokalisierte Fehlerzeichenfolgen für Ereignisse in Ihre Datenbank importieren, indem Sie Msidb.exe [**oder MsiDatabaseImport verwenden.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) Das SDK enthält lokalisierte Ressourcenzeichenfolgen für jede der Sprachen, die im Abschnitt [Lokalisieren der Fehler- und Aktionstexttabellen aufgeführt](localizing-the-error-and-actiontext-tables.md) sind. Wenn die Fehlerzeichenfolgen für Ereignisse nicht aufgefüllt werden, lädt das Installationsprogramm lokalisierte Zeichenfolgen für die Sprache, die von der [**ProductLanguage-Eigenschaft angegeben**](productlanguage.md) wird.

 

 
