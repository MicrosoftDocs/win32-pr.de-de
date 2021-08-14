---
description: Befehlszeilenoptionen für msiexec.exe für Windows Installer 3.0 und früher. Stellt eine Tabelle mit Optionen, Parametern und Beschreibungen bereit. Beispiele für die Installation von Produkten und anderen Aufgaben.
ms.assetid: a70d8cc8-af47-4472-aabc-97481d97080d
title: Befehlszeilenoptionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287b5711468217105846a13496a23794235bbcfdfcbd0e79278aaba17e7c0341
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380314"
---
# <a name="command-line-options"></a>Befehlszeilenoptionen

Das ausführbare Programm, das Pakete interpretiert und Produkte installiert, ist Msiexec.exe. Beachten Sie, dass Msiexec bei der Rückgabe auch eine Fehlerebene festlegt, die [den Systemfehlercodes](/windows/desktop/Debug/system-error-codes)entspricht. Bei Befehlszeilenoptionen wird die Groß-/Kleinschreibung nicht beachtet.

Die Befehlszeilenoptionen in der folgenden Tabelle sind mit Windows Installer 3.0 und früheren Versionen verfügbar. Die Command-Line Optionen des [Standardinstallationsprogramms](standard-installer-command-line-options.md) sind ab Windows Installer 3.0 verfügbar.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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
<td>Repariert ein Produkt. Diese Option ignoriert alle In der Befehlszeile eingegebenen Eigenschaftswerte. Die Standardargumentliste für diese Option ist "omus". Diese Option teilt die gleiche Argumentliste wie die <a href="reinstallmode.md"><strong>REINSTALLMODE-Eigenschaft.</strong></a><br/> p: Wird nur neu installiert, wenn die Datei fehlt.<br/> o: Wird neu installiert, wenn die Datei fehlt oder eine ältere Version installiert ist.<br/> e: Wird neu installiert, wenn die Datei fehlt oder eine gleiche oder ältere Version installiert ist.<br/> d : Wird neu installiert, wenn die Datei fehlt oder eine andere Version installiert ist.<br/> c: Wird neu installiert, wenn die Datei fehlt oder die gespeicherte Prüfsumme nicht mit dem berechneten Wert übereinstimmt. Repariert nur Dateien mit <strong>msidbFileAttributesChecksum</strong> in der Attributes -Spalte der <a href="file-table.md">Dateitabelle.</a><br/> a: Erzwingt die Neuinstallation aller Dateien.<br/> u: Schreibt alle erforderlichen benutzerspezifischen Registrierungseinträge um.<br/> m: Schreibt alle erforderlichen computerspezifischen Registrierungseinträge um.<br/> s: Überschreibt alle vorhandenen Verknüpfungen.<br/> v: Wird aus der Quelle ausgeführt und speichert das lokale Paket erneut zwischen. Verwenden Sie <strong>nicht</strong> die v-Neuinstallationsoption für die erste Installation einer Anwendung oder eines Features.<br/></td>
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
<td>[u|m] <em>Packageor</em><br/> [u|m] Paket<strong>-/t-Transformationsliste</strong><em></em> <em></em><br/> <em>or</em><br/> [u|m] <em>Package</em><strong>/g</strong><em>LanguageID</em><br/></td>
<td>Kündigt ein Produkt an. Diese Option ignoriert alle In der Befehlszeile eingegebenen Eigenschaftswerte.<br/> u : Kündigt dem aktuellen Benutzer an.<br/> m : Kündigt allen Benutzern des Computers an.<br/> g : Sprachbezeichner.<br/> t: Wendet die Transformation auf angekündigte Pakete an.<br/></td>
</tr>
<tr class="even">
<td><strong>/L</strong></td>
<td>[i|w|e|a|r|u|c|m|o|p|v|x|+|!| *] <em>Protokolldatei</em></td>
<td>Schreibt Protokollierungsinformationen am angegebenen vorhandenen Pfad in eine Protokolldatei. Der Pfad zum Protokolldateispeicherort muss bereits vorhanden sein. Das Installationsprogramm erstellt nicht die Verzeichnisstruktur für die Protokolldatei. Flags geben an, welche Informationen protokolliert werden sollen. Wenn keine Flags angegeben sind, lautet der Standardwert "i csvmo".<br/> i : Statusmeldungen.<br/> w : Nichttale Warnungen.<br/> e : Alle Fehlermeldungen.<br/> a: Starten von Aktionen.<br/> r: Aktionsspezifische Datensätze.<br/> u : Benutzeranforderungen.<br/> c: Anfängliche Benutzeroberflächenparameter.<br/> m: Nicht genügend Arbeitsspeicher oder schwerwiegende Exitinformationen.<br/> o: Nachrichten mit nicht genügend Speicherplatz.<br/> p : Terminaleigenschaften.<br/> v : Ausführliche Ausgabe.<br/> x: Zusätzliche Debuginformationen. <strong>Windows Installer 2.0:</strong> Wird nicht unterstützt. Die Option x ist mit Windows Installer Version 3.0.3790.2180 und höher verfügbar.<br/> <br/> + - An vorhandene Datei anfügen.<br/> ! – Leert jede Zeile in das Protokoll.<br/> &quot;*&quot; – Platzhalter, protokollieren Sie alle Informationen mit Ausnahme der v- und x-Optionen. Um die v- und x-Optionen einzuschließen, geben Sie &quot; /l* vx &quot; an.<br/>
<blockquote>
[!Note]<br />
Weitere Informationen zu allen Methoden, die zum Festlegen des Protokollierungsmodus verfügbar sind, finden Sie unter <a href="normal-logging.md">Normale Protokollierung</a> im Abschnitt <a href="windows-installer-logging.md">Windows Installer-Protokollierung.</a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/m</strong></td>
<td><em>Dateiname</em>
<blockquote>
[!Note]<br />
Der <em>Dateiname</em> darf maximal acht Zeichen lang sein.
</blockquote>
<br/></td>
<td>Generiert eine MIF-Datei mit SMS-Status. Muss mit den Optionen install (-i), remove (-x), administrative installation (-a) oder reinstall (-f) verwendet werden. Die ISMIF32.DLL wird als Teil von SMS installiert und muss sich im Pfad befinden.<br/> Die Felder der Status-MIF-Datei werden mit den folgenden Informationen gefüllt:<br/> Hersteller : <a href="author-summary.md"> <strong>Autor</strong></a><br/> Produkt – <a href="revision-number-summary.md"> <strong>Revisionsnummer</strong></a><br/> Version – <a href="subject-summary.md"> <strong>Betreff</strong></a><br/> Gebietsschema: <a href="template-summary.md"> <strong>Vorlage</strong></a><br/> Seriennummer – nicht festgelegt<br/> Installation– durch ISMIF32.DLL auf &quot; DateTime festgelegt&quot;<br/> InstallStatus – &quot; Erfolg &quot; oder &quot; Fehler&quot;<br/> Beschreibung: Fehlermeldungen in der folgenden Reihenfolge: 1) Vom Installationsprogramm generierte Fehlermeldungen. 2) Ressource aus Msi.dll, wenn die Installation nicht gestartet oder der Benutzer beendet werden konnte. 3) Systemfehlermeldungsdatei. 4) Formatierte Meldung: &quot; Installationsfehler %i &quot; , wobei %i der Fehler ist, der von Msi.dll zurückgegeben wird.<br/></td>
</tr>
<tr class="even">
<td><strong>/p</strong></td>
<td><em>PatchPackage[;p atchPackage2</em> ]</td>
<td>Wendet einen Patch an. Um einen Patch auf ein installiertes Administratorimage anzuwenden, müssen Sie die folgenden Optionen kombinieren:<br/> /p <em> <PatchPackage> [;p atchPackage2 ] </em> /a<em><Package></em><br/></td>
</tr>
<tr class="odd">
<td><strong>/q</strong></td>
<td>n|b|r|f</td>
<td>Legt die <a href="user-interface-levels.md">Benutzeroberflächenebene fest.</a><br/> q , qn – Keine Benutzeroberfläche<br/> qb – <a href="b-gly.md"><em>Einfache Benutzeroberfläche</em></a>. Verwenden Sie qb! , um die Schaltfläche <strong>Abbrechen</strong> auszublenden.<br/> qr: <a href="r-gly.md"><em>Reduzierte Benutzeroberfläche</em></a> ohne modales Dialogfeld, das am Ende der Installation angezeigt wird.<br/> qf: <a href="f-gly.md"><em>Vollständige Benutzeroberfläche</em></a> und alle am Ende der modalen Dialogfelder <a href="fatalerror-dialog.md">"FatalError",</a> <a href="userexit-dialog.md">"UserExit"</a>oder <a href="exit-dialog.md">"Exit"</a> (Beenden).<br/> qn+ – Keine Benutzeroberfläche außer einem modalen Dialogfeld, das am Ende angezeigt wird.<br/> qb+ – <a href="b-gly.md"><em>Einfache Benutzeroberfläche</em></a> mit einem modalen Dialogfeld, das am Ende angezeigt wird. Das modale Feld wird nicht angezeigt, wenn der Benutzer die Installation abbricht. Verwenden Sie qb+! oder qb!+, um die Schaltfläche <strong>Abbrechen</strong> auszublenden.<br/> qb– – <a href="b-gly.md"><em>Einfache Benutzeroberfläche</em></a> ohne modale Dialogfelder. Beachten Sie, dass /qb+- keine unterstützte Benutzeroberflächenebene ist. Verwenden Sie qb-! oder qb!-, um die Schaltfläche <strong>Abbrechen</strong> auszublenden.<br/> Beachten Sie, dass ! -Option ist mit Windows Installer 2.0 verfügbar und funktioniert nur mit der einfachen Benutzeroberfläche. Er ist mit der vollständigen Benutzeroberfläche ungültig.<br/></td>
</tr>
<tr class="even">
<td><strong>/?</strong> oder <strong>/h</strong></td>
<td> </td>
<td>Zeigt Copyrightinformationen für Windows Installer an.<br/></td>
</tr>
<tr class="odd">
<td><strong>/y</strong></td>
<td><em>Modul</em></td>
<td>Ruft die Systemfunktion <strong>DllRegisterServer auf,</strong> um module selbst zu registrieren, die in der Befehlszeile übergeben werden. Geben Sie den vollständigen Pfad zur DLL an. Beispielsweise können Sie MY_FILE.DLL im aktuellen Ordner verwenden:<br/> <strong>msiexec /y .\MY_FILE.DLL</strong><br/> Diese Option wird nur für Registrierungsinformationen verwendet, die nicht mithilfe der Registrierungstabellen der .msi werden können.<br/></td>
</tr>
<tr class="even">
<td><strong>/z</strong></td>
<td><em>Modul</em></td>
<td>Ruft die Systemfunktion <strong>DllUnRegisterServer auf,</strong> um die Registrierung von Modulen zu aufheben, die in der Befehlszeile übergeben werden. Geben Sie den vollständigen Pfad zur DLL an. Beispielsweise können Sie MY_FILE.DLL im aktuellen Ordner verwenden: <br/> <strong>msiexec /z .\MY_FILE.DLL</strong><br/> Diese Option wird nur für Registrierungsinformationen verwendet, die nicht mithilfe der Registrierungstabellen der .msi werden können.<br/></td>
</tr>
<tr class="odd">
<td><strong>/c</strong></td>

<td>Gibt eine neue Instanz des Produkts an. Muss in Verbindung mit /t verwendet werden. Verfügbar ab der Windows Installer-Version, die mit Windows Server 2003 und Windows XP mit Service Pack 1 (SP1) ausgeliefert wird.<br/></td>
</tr>
<tr class="even">
<td><strong>/n</strong></td>
<td><em>ProductCode</em></td>
<td>Gibt eine bestimmte Instanz des Produkts an. Wird verwendet, um eine Instanz zu identifizieren, die mithilfe der Unterstützung mehrerer Instanzen installiert wurde, indem transformationen durch einen Produktcode geändert werden. Verfügbar ab der Windows Installer-Version, die im Lieferumfang von Windows Server 2003 und Windows XP mit SP1 enthalten ist. <br/></td>
</tr>
</tbody>
</table>



 

Die Optionen /i, /x, /f \[ p o e d c a u m s \| v , \| \| \| \| \| \| \| \| \] /j u m , \[ \| \] /a, /p, /y und /z sollten nicht zusammen verwendet werden. Die einzige Ausnahme dieser Regel ist, dass für das Patchen einer [Administratorinstallation](administrative-installation.md) sowohl /p als auch /a verwendet werden müssen. Die Optionen /t, /c und /g sollten nur mit /j verwendet werden. Die Optionen /l und /q können mit /i, /x, /f \[ p o e d c a u m \| s \| \| \| \| \| \| \| \| \] v, /j \[ u \| \] m, /a und /p verwendet werden. Die Option /n kann mit /i, /f, /x und /p verwendet werden.

Um ein Produkt von A: \\Example.msi installieren Sie das Produkt wie folgt:

**msiexec /i A: \\Example.msi**

Nur [öffentliche Eigenschaften](public-properties.md) können über die Befehlszeile geändert werden. Alle Eigenschaftsnamen in der Befehlszeile werden als Großbuchstaben interpretiert, aber der Wert behält die Groß-/Kleinschreibung bei. Wenn Sie **MyProperty** in einer Befehlszeile eingeben, überschreibt das Installationsprogramm den Wert von MYPROPERTY und nicht den Wert von **MyProperty** in der Property-Tabelle. Weitere Informationen finden Sie unter [Informationen zu Eigenschaften.](about-properties.md)

Verwenden Sie die folgende Syntax in der Befehlszeile, um ein Produkt zu installieren, bei dem PROPERTY auf VALUE festgelegt ist. Sie können die Eigenschaft an einer beliebigen Stelle außer zwischen einer Option und ihrem Argument setzen.

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

**msiexec /i testdb.msi INSTALLLEVEL=3 /l \* msi.log COMPANYNAME="Acme ""Widgets"" und ""Mos.""**

Im folgenden Beispiel werden Ankündigungsoptionen gezeigt. Beachten Sie, dass bei Schaltern nicht zwischen Schreibung und Schreibung zu beachten ist.

**msiexec /JM msisample.msi /T transform.mst /LIME logfile.txt**

Im folgenden Beispiel wird gezeigt, wie Sie eine neue Instanz eines Produkts installieren, das angekündigt werden soll. Dieses Produkt wurde für die Unterstützung mehrerer Instanztransformationen verfasst.

**msiexec /JM msisample.msi /T :instance1.mst;customization.mst /c /LIME logfile.txt**

Das folgende Beispiel zeigt, wie eine Instanz eines Produkts gepatcht wird, das mithilfe mehrerer Instanztransformationen installiert wird.

**msiexec /p msipatch.msp;msipatch2.msp /n {00000001-0002-0000-0000-624474736554} /qb**

Wenn Sie Patches auf ein bestimmtes Produkt anwenden, können die Optionen /i und /p nicht zusammen in einer Befehlszeile angegeben werden. In diesem Fall können Sie Patches wie folgt auf ein Produkt anwenden.

**msiexec /i A: \\Example.msi PATCH=msipatch.msp;msipatch2.msp /qb**

Die [**PATCH-Eigenschaft**](patch.md) kann nicht in einer Befehlszeile festgelegt werden, wenn die Option /p verwendet wird. Wenn die **PATCH-Eigenschaft** festgelegt wird, wenn die Option /p verwendet wird, wird der Wert der **PATCH-Eigenschaft** ignoriert und überschrieben.

 

