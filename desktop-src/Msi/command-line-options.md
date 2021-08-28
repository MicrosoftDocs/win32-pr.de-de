---
description: Befehlszeilenoptionen für msiexec.exe für Windows Installer 3.0 und früher. Stellt eine Tabelle mit Optionen, Parametern und Beschreibungen zur Verfügung. Beispiele, die zeigen, wie Produkte und andere Aufgaben installiert werden.
ms.assetid: a70d8cc8-af47-4472-aabc-97481d97080d
title: Befehlszeilenoptionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a45d59922a6c2c1d6cd0b5f8cd61b393944e23
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880628"
---
# <a name="command-line-options"></a>Befehlszeilenoptionen

Das ausführbare Programm, das Pakete interpretiert und Produkte installiert, wird Msiexec.exe. Beachten Sie, dass Msiexec auch eine Fehlerebene bei der Rückgabe legt, die den [Systemfehlercodes entspricht.](/windows/desktop/Debug/system-error-codes) Bei Befehlszeilenoptionen wird die Groß-/Kleinschreibung nicht beachtet.

Die Befehlszeilenoptionen in der folgenden Tabelle sind mit Windows Installer 3.0 und früheren Versionen verfügbar. Die [Optionen für Command-Line Standardinstallationsprogramm](standard-installer-command-line-options.md) sind ab Windows Installer 3.0 ebenfalls verfügbar.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Parameter</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>/I</strong></td>
<td><em>Paket| Productcode</em></td>
<td>Installiert oder konfiguriert ein Produkt.<br/></td>
</tr>
<tr class="even">
<td><strong>/f</strong></td>
<td>[p|o|e|d|c|a|u|m|s|v] <em>Paket</em> | <em>ProductCode</em></td>
<td>Repariert ein Produkt. Diese Option ignoriert alle Eigenschaftswerte, die in der Befehlszeile eingegeben werden. Die Standardargumentliste für diese Option ist "omus". Diese Option verwendet dieselbe Argumentliste wie die <a href="reinstallmode.md"><strong>REINSTALLMODE-Eigenschaft.</strong></a><br/> p : Wird nur dann neu installiert, wenn die Datei fehlt.<br/> o : Wird neu installiert, wenn die Datei fehlt oder eine ältere Version installiert ist.<br/> e: Wird neu installiert, wenn die Datei fehlt oder eine gleich oder eine ältere Version installiert ist.<br/> d : Wird neu installiert, wenn die Datei fehlt oder eine andere Version installiert ist.<br/> c : Wird neu installiert, wenn die Datei fehlt oder die gespeicherte Prüfsumme nicht mit dem berechneten Wert übereinstimmen. Repariert nur Dateien mit <strong>msidbFileAttributesChecksum</strong> in der Spalte Attribute der <a href="file-table.md">Tabelle Datei.</a><br/> a: Erzwingt, dass alle Dateien neu installiert werden.<br/> u: Schreibt alle erforderlichen benutzerspezifischen Registrierungseinträge neu.<br/> m: Schreibt alle erforderlichen computerspezifischen Registrierungseinträge neu.<br/> s: Überschreibt alle vorhandenen Tastenkombinationen.<br/> v: Wird von der Quelle aus ausgeführt und speichert das lokale Paket erneut zwischen. Verwenden Sie die <strong>Option v</strong> reinstall nicht für die erste Installation einer Anwendung oder eines Features.<br/></td>
</tr>
<tr class="odd">
<td><strong>/a</strong></td>
<td><em>Paket</em></td>
<td><a href="administrative-installation.md">Administratorinstallationsoption.</a> Installiert ein Produkt im Netzwerk.<br/></td>
</tr>
<tr class="even">
<td><strong>/x</strong></td>
<td><em>Paket| Productcode</em></td>
<td>Deinstalliert ein Produkt.</td>
</tr>
<tr class="odd">
<td><strong>/j</strong></td>
<td>[u|m] <em>Packageor</em><br/> [u|m] <em>Paket</em><strong>/t</strong><em>Transformationsliste</em><br/> <em>or</em><br/> [u|m] <em>Package</em><strong>/g</strong><em>LanguageID</em><br/></td>
<td>Gibt ein Produkt an. Diese Option ignoriert alle Eigenschaftswerte, die in der Befehlszeile eingegeben werden.<br/> u: Gibt für den aktuellen Benutzer an.<br/> m: Wird allen Benutzern des Computers angekündigt.<br/> g : Sprachbezeichner.<br/> t: Wendet die Transformation auf das angekündigte Paket an.<br/></td>
</tr>
<tr class="even">
<td><strong>/L</strong></td>
<td>[i|w|e|a|r|u|c|m|o|p|v|x|+|!| *] <em>Protokolldatei</em></td>
<td>Schreibt Protokollierungsinformationen unter dem angegebenen vorhandenen Pfad in eine Protokolldatei. Der Pfad zum Speicherort der Protokolldatei muss bereits vorhanden sein. Das Installationsprogramm erstellt nicht die Verzeichnisstruktur für die Protokolldatei. Flags geben an, welche Informationen protokolliert werden. Wenn keine Flags angegeben werden, ist der Standardwert "iojmo".<br/> i : Statusmeldungen.<br/> w : Nichtfatale Warnungen.<br/> e: Alle Fehlermeldungen.<br/> a: Starten von Aktionen.<br/> r: Aktionsspezifische Datensätze.<br/> u : Benutzeranforderungen.<br/> c : Anfängliche Benutzeroberflächenparameter.<br/> m: Nicht genügend Arbeitsspeicher oder schwerwiegende Exitinformationen.<br/> o: Nachrichten, die nicht auf dem Datenträger verfügbar sind.<br/> p : Terminaleigenschaften.<br/> v : Ausführliche Ausgabe.<br/> x: Zusätzliche Debuginformationen. <strong>Windows Installer 2.0:</strong> Nicht unterstützt. Die x-Option ist mit Windows Installer-Version 3.0.3790.2180 und höher verfügbar.<br/> <br/> + - An vorhandene Datei anfügen.<br/> ! – Leeren Sie jede Zeile in das Protokoll.<br/> &quot;*&quot; – Platzhalter, alle Informationen mit Ausnahme der Optionen v und x protokollieren. Geben Sie &quot; /l vx an,* um die v- und x-Optionen ein include &quot; zu erhalten.<br/>
<blockquote>
[!Note]<br />
Weitere Informationen zu allen Methoden, die zum Festlegen des Protokollierungsmodus verfügbar sind, finden Sie unter <a href="normal-logging.md">Normale</a> Protokollierung im Abschnitt Windows <a href="windows-installer-logging.md">Installer-Protokollierung.</a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/m</strong></td>
<td><em>Dateiname</em>
<blockquote>
[!Note]<br />
Die Länge des <em>Dateinamens</em> darf nicht mehr als acht Zeichen umfassen.
</blockquote>
<br/></td>
<td>Generiert eine MIF-Datei mit dem SMS-Status. Muss entweder mit den Optionen install (-i), remove (-x), administrative installation (-a) oder reinstall (-f) verwendet werden. Der ISMIF32.DLL wird als Teil von SMS installiert und muss sich im Pfad befindet.<br/> Die Felder der Mif-Statusdatei werden mit den folgenden Informationen gefüllt:<br/> Hersteller – <a href="author-summary.md"> <strong>Autor</strong></a><br/> Produkt – <a href="revision-number-summary.md"> <strong>Revisionsnummer</strong></a><br/> Version – <a href="subject-summary.md"> <strong>Betreff</strong></a><br/> Locale : <a href="template-summary.md"> <strong>Vorlage</strong></a><br/> Seriennummer – nicht festgelegt<br/> Installation: Legen Sie diese ISMIF32.DLL &quot; auf DateTime fest.&quot;<br/> InstallStatus – &quot; Erfolg &quot; oder &quot; Fehler&quot;<br/> Beschreibung: Fehlermeldungen in der folgenden Reihenfolge: 1) Vom Installationsprogramm generierte Fehlermeldungen. 2) Ressource aus Msi.dll, wenn die Installation nicht beginnen oder der Benutzer beendet werden konnte. 3) Systemfehlermeldungsdatei. 4) Formatierte Meldung: &quot; Installationsprogrammfehler %i , wobei %i ein Fehler ist, der von der &quot; Msi.dll.<br/></td>
</tr>
<tr class="even">
<td><strong>/p</strong></td>
<td><em>PatchPackage[;p atchPackage2</em> ]</td>
<td>Wendet einen Patch an. Um einen Patch auf ein installiertes administratives Image anzuwenden, müssen Sie die folgenden Optionen kombinieren:<br/> /p <em> &lt; PatchPackage &gt; [;p atchPackage2 ]</em> /a<em><Package></em><br/></td>
</tr>
<tr class="odd">
<td><strong>/q</strong></td>
<td>n|b|r|f</td>
<td>Legt <a href="user-interface-levels.md">die Benutzeroberflächesebene fest.</a><br/> q , qn – Keine Benutzeroberfläche<br/> qb: <a href="b-gly.md"><em>Grundlegende Benutzeroberfläche.</em></a> Verwenden Sie qb! , um die Schaltfläche <strong>Abbrechen</strong> auszublenden.<br/> qr: <a href="r-gly.md"><em>Reduzierte Benutzeroberfläche</em></a> ohne modales Dialogfeld, das am Ende der Installation angezeigt wird.<br/> modal: <a href="f-gly.md"><em>Vollständige Benutzeroberfläche</em></a> und alle erstellten modalen Dialogfelder <a href="fatalerror-dialog.md">"FatalError",</a> <a href="userexit-dialog.md">"UserExit"</a>oder <a href="exit-dialog.md">"Exit"</a> am Ende.<br/> qn+: Keine Benutzeroberfläche außer einem modalen Dialogfeld, das am Ende angezeigt wird.<br/> qb+: <a href="b-gly.md"><em>Einfache Benutzeroberfläche</em></a> mit einem modalen Dialogfeld, das am Ende angezeigt wird. Das modale Feld wird nicht angezeigt, wenn der Benutzer die Installation abbricht. Verwenden Sie qb+! oder qb!+, um die Schaltfläche <strong>Abbrechen</strong> auszublenden.<br/> qb: <a href="b-gly.md"><em>Einfache Benutzeroberfläche</em></a> ohne modale Dialogfelder. Beachten Sie, dass /qb+- keine unterstützte Benutzeroberflächenebene ist. Verwenden Sie qb-! oder qb!- , um die Schaltfläche <strong>Abbrechen</strong> auszublenden.<br/> Beachten Sie, dass die ! -Option ist mit Windows Installer 2.0 verfügbar und funktioniert nur mit der einfachen Benutzeroberfläche. Sie ist mit der vollständigen Benutzeroberfläche ungültig.<br/></td>
</tr>
<tr class="even">
<td><strong>/?</strong> oder <strong>/h</strong></td>
<td> </td>
<td>Zeigt Copyrightinformationen für Windows Installer an.<br/></td>
</tr>
<tr class="odd">
<td><strong>/y</strong></td>
<td><em>Modul</em></td>
<td>Ruft die Systemfunktion <strong>DllRegisterServer</strong> auf, um module, die über die Befehlszeile übergeben werden, selbst zu registrieren. Geben Sie den vollständigen Pfad zur DLL an. Für MY_FILE.DLL im aktuellen Ordner können Sie beispielsweise Folgendes verwenden:<br/> <strong>msiexec /y .\MY_FILE.DLL</strong><br/> Diese Option wird nur für Registrierungsinformationen verwendet, die nicht mithilfe der Registrierungstabellen der .msi-Datei hinzugefügt werden können.<br/></td>
</tr>
<tr class="even">
<td><strong>/z</strong></td>
<td><em>Modul</em></td>
<td>Ruft die Systemfunktion <strong>DllUnRegisterServer</strong> auf, um die Registrierung der in der Befehlszeile übergebenen Module aufzuheben. Geben Sie den vollständigen Pfad zur DLL an. Für MY_FILE.DLL im aktuellen Ordner können Sie beispielsweise Folgendes verwenden: <br/> <strong>msiexec /z .\MY_FILE.DLL</strong><br/> Diese Option wird nur für Registrierungsinformationen verwendet, die nicht mithilfe der Registrierungstabellen der .msi-Datei entfernt werden können.<br/></td>
</tr>
<tr class="odd">
<td><strong>/c</strong></td>

<td>Kündigt eine neue Instanz des Produkts an. Muss in Verbindung mit /t verwendet werden. Verfügbar ab der Windows Installer-Version, die mit Windows Server 2003 und Windows XP mit Service Pack 1 (SP1) ausgeliefert wird.<br/></td>
</tr>
<tr class="even">
<td><strong>/n</strong></td>
<td><em>ProductCode</em></td>
<td>Gibt eine bestimmte Instanz des Produkts an. Wird verwendet, um eine Instanz zu identifizieren, die mithilfe der Unterstützung mehrerer Instanzen über einen Produktcode installiert wurde, der Transformationen ändert. Verfügbar ab der Windows Installer-Version, die mit Windows Server 2003 und Windows XP mit SP1 ausgeliefert wird. <br/></td>
</tr>
</tbody>
</table>



 

Die Optionen /i, /x, /f \[ p o e d c a u m s \| v \| , \| \| \| \| \| \| \| \] /j u m , \[ \| \] /a, /p, /y und /z sollten nicht zusammen verwendet werden. Eine Ausnahme von dieser Regel ist, dass zum Patchen einer [Administratorinstallation](administrative-installation.md) sowohl /p als auch /a verwendet werden muss. Die Optionen /t, /c und /g sollten nur mit /j verwendet werden. Die Optionen /l und /q können mit /i, /x, /f \[ p o e d c a u m \| s v \| , \| \| \| \| \| \| \| \] /j u m , \[ \| \] /a und /p verwendet werden. Die Option /n kann mit /i, /f, /x und /p verwendet werden.

Um ein Produkt aus A: \\Example.msi zu installieren, installieren Sie das Produkt wie folgt:

**msiexec /i A: \\Example.msi**

Nur [öffentliche Eigenschaften](public-properties.md) können über die Befehlszeile geändert werden. Alle Eigenschaftsnamen in der Befehlszeile werden als Großbuchstaben interpretiert, aber der Wert behält die Groß-/Kleinschreibung bei. Wenn Sie **MyProperty** in einer Befehlszeile eingeben, überschreibt das Installationsprogramm den Wert von MYPROPERTY und nicht den Wert von **MyProperty** in der Property-Tabelle. Weitere Informationen finden Sie unter [Informationen zu Eigenschaften.](about-properties.md)

Verwenden Sie die folgende Syntax in der Befehlszeile, um ein Produkt zu installieren, für das PROPERTY auf VALUE festgelegt ist. Sie können die Eigenschaft an einer beliebigen Stelle außer zwischen einer Option und ihrem Argument setzen.

Richtige Syntax:

**msiexec /i A: \\Example.msi PROPERTY=VALUE**

Falsche Syntax:

**msiexec /i PROPERTY=VALUE A: \\Example.msi**

Eigenschaftswerte, die Literalzeichenfolgen sind, müssen in Anführungszeichen eingeschlossen werden. Schließen Sie alle Leerzeichen in die Zeichenfolge zwischen den Markierungen ein.

**msiexec /i A: \\Example.msi PROPERTY="Embedded White Space"**

Um eine öffentliche Eigenschaft über die Befehlszeile zu löschen, legen Sie ihren Wert auf eine leere Zeichenfolge fest.

**msiexec /i A: \\Example.msi PROPERTY=""**

Schließen Sie für Textabschnitte, die durch literale Anführungszeichen getrennt sind, den Abschnitt in ein zweites Anführungszeichenpaar ein.

**msiexec /i A: \\Example.msi PROPERTY="Embedded ""Quotes"" White Space"**

Das folgende Beispiel zeigt eine komplizierte Befehlszeile.

**msiexec /i testdb.msi INSTALLLEVEL=3 /l \* msi.log COMPANYNAME="Acme ""Widgets"" und ""Widgetmos.""**

Das folgende Beispiel zeigt Ankündigungsoptionen. Beachten Sie, dass bei Schaltern die Groß-/Kleinschreibung nicht beachtet wird.

**msiexec /JM msisample.msi /T transform.mst /LIME logfile.txt**

Im folgenden Beispiel wird gezeigt, wie Sie eine neue Instanz eines Produkts installieren, das angekündigt werden soll. Dieses Produkt wurde zur Unterstützung mehrerer Instanztransformationen erstellt.

**msiexec /JM msisample.msi /T :instance1.mst;customization.mst /c /LIME logfile.txt**

Das folgende Beispiel zeigt, wie Sie eine Instanz eines Produkts patchen, das mithilfe von Transformationen für mehrere Instanzen installiert wird.

**msiexec /p msipatch.msp;msipatch2.msp /n {00000001-0002-0000-0000-624474736554} /qb**

Wenn Sie Patches auf ein bestimmtes Produkt anwenden, können die Optionen /i und /p nicht zusammen in einer Befehlszeile angegeben werden. In diesem Fall können Sie Patches wie folgt auf ein Produkt anwenden.

**msiexec /i A: \\Example.msi PATCH=msipatch.msp;msipatch2.msp /qb**

Die [**PATCH-Eigenschaft**](patch.md) kann nicht in einer Befehlszeile festgelegt werden, wenn die Option /p verwendet wird. Wenn die **PATCH-Eigenschaft** festgelegt wird, wenn die Option /p verwendet wird, wird der Wert der **PATCH-Eigenschaft** ignoriert und überschrieben.

 

