---
description: Befehlszeilenoptionen für msiexec.exe für Windows Installer 3,0 und früher. Stellt eine Tabelle mit Optionen, Parametern und Beschreibungen bereit. In den Beispielen wird gezeigt, wie Sie Produkte und andere Tasks installieren.
ms.assetid: a70d8cc8-af47-4472-aabc-97481d97080d
title: Befehlszeilenoptionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46fe56026c21e4120963c86b4de08decc85b2a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373196"
---
# <a name="command-line-options"></a>Befehlszeilenoptionen

Das ausführbare Programm, das Pakete interpretiert und Produkte installiert, ist Msiexec.exe. Beachten Sie, dass msiexec bei der Rückgabe auch eine Fehlerstufe festlegt, die [Systemfehler Codes](/windows/desktop/Debug/system-error-codes)entspricht. Bei Befehlszeilenoptionen wird die Groß-/Kleinschreibung nicht beachtet.

Die Befehlszeilenoptionen in der folgenden Tabelle sind in Windows Installer 3,0 und früheren Versionen verfügbar. Die [Command-Line Optionen für Standard-Installer](standard-installer-command-line-options.md) sind auch ab Windows Installer 3,0 verfügbar.



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
<td><em>Paket | ProductCode</em></td>
<td>Installiert oder konfiguriert ein Produkt.<br/></td>
</tr>
<tr class="even">
<td><strong>/f</strong></td>
<td>[p | o | e | d | c | a | u | m | s | v] <em>Paket</em> | <em>ProductCode</em></td>
<td>Repariert ein Produkt. Diese Option ignoriert alle Eigenschaftswerte, die in der Befehlszeile eingegeben werden. Die Standardargument Liste für diese Option ist "omus". Diese Option hat dieselbe Argumentliste wie die <a href="reinstallmode.md"><strong>REINSTALLMODE</strong></a> -Eigenschaft.<br/> p-wird nur neu installiert, wenn die Datei fehlt.<br/> o-neu installiert, wenn die Datei fehlt oder eine ältere Version installiert ist.<br/> e-neu installieren, wenn die Datei fehlt oder eine gleichmäßige oder eine ältere Version installiert ist.<br/> d: wird neu installiert, wenn die Datei fehlt oder eine andere Version installiert ist.<br/> c: wird neu installiert, wenn die Datei fehlt oder die gespeicherte Prüfsumme nicht mit dem berechneten Wert identisch ist. Repariert nur Dateien mit <strong>msidbFileAttributesChecksum</strong> in der Spalte Attribute der <a href="file-table.md">Datei</a> Tabelle.<br/> a: erzwingt, dass alle Dateien neu installiert werden.<br/> u: schreibt alle erforderlichen benutzerspezifischen Registrierungseinträge neu.<br/> m-schreibt alle erforderlichen computerspezifischen Registrierungseinträge neu.<br/> s-überschreibt alle vorhandenen Verknüpfungen.<br/> v: führt die Ausführung von der Quelle aus und speichert das lokale Paket erneut. Verwenden Sie die Option " <strong>v</strong> installieren Sie" nicht für die erste Installation einer Anwendung oder eines Features.<br/></td>
</tr>
<tr class="odd">
<td><strong>/a</strong></td>
<td><em>Paket</em></td>
<td><a href="administrative-installation.md">Administrative Installations</a> Option. Hiermit wird ein Produkt im Netzwerk installiert.<br/></td>
</tr>
<tr class="even">
<td><strong>/x</strong></td>
<td><em>Paket | ProductCode</em></td>
<td>Deinstalliert ein Produkt.</td>
</tr>
<tr class="odd">
<td><strong>/j</strong></td>
<td>[u | m] <em>Packageor</em><br/> [u | m] <em>Paket</em><strong>/t</strong><em>Transformations Liste</em><br/> <em>or</em><br/> [u | m] <em>Paket</em><strong>/g</strong><em>LanguageID</em><br/></td>
<td>Gibt ein Produkt an. Diese Option ignoriert alle Eigenschaftswerte, die in der Befehlszeile eingegeben werden.<br/> u: gibt dem aktuellen Benutzer eine Werbung.<br/> m: gibt allen Benutzern des Computers eine Werbung.<br/> Bezeichner der g-Sprache.<br/> t-wendet die Transformation auf das angekündigte Paket an.<br/></td>
</tr>
<tr class="even">
<td><strong>/L</strong></td>
<td>[i | w | e | a | r | u | c | m | o | p | v | x | + |! | *] <em>Protokolldatei</em></td>
<td>Schreibt Protokollierungs Informationen in eine Protokolldatei unter dem angegebenen vorhandenen Pfad. Der Pfad zum Speicherort der Protokolldatei muss bereits vorhanden sein. Das Installationsprogramm erstellt nicht die Verzeichnisstruktur für die Protokolldatei. Flags geben an, welche Informationen protokolliert werden sollen. Wenn keine Flags angegeben sind, lautet der Standardwert "iwearmo.".<br/> i-Status Meldungen.<br/> w-nicht schwerwiegende Warnungen.<br/> e-alle Fehlermeldungen.<br/> a: Starten von Aktionen.<br/> r-Aktions spezifische Datensätze.<br/> u-User-Anforderungen.<br/> c-anfängliche UI-Parameter.<br/> m-nicht genügend Arbeitsspeicher oder schwerwiegende Exit-Informationen.<br/> nicht genügend Speicherplatz Nachrichten.<br/> p-Terminal Eigenschaften.<br/> v-ausführliche Ausgabe.<br/> x-zusätzliche Debuginformationen. <strong>Windows Installer 2,0:</strong> Nicht unterstützt. Die Option x ist in Windows Installer Version 3.0.3790.2180 und höher verfügbar.<br/> <br/> + - An vorhandene Datei anfügen.<br/> ! : Leert jede Zeile in das Protokoll.<br/> &quot;-Platzhalter *&quot; , alle Informationen werden mit Ausnahme der Optionen v und x protokolliert. Um die Optionen v und x einzuschließen, geben Sie &quot; /l* VX an &quot; .<br/>
<blockquote>
[!Note]<br />
Weitere Informationen zu allen Methoden, die zum Festlegen des Protokollierungs Modus verfügbar sind, finden Sie unter <a href="normal-logging.md">normale Protokollierung</a> im Abschnitt <a href="windows-installer-logging.md">Windows Installer Protokollierung</a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/m</strong></td>
<td><em>Einfügen</em>
<blockquote>
[!Note]<br />
Die Länge des <em>Datei namens</em> darf nicht mehr als acht Zeichen umfassen.
</blockquote>
<br/></td>
<td>Generiert eine SMS-Status-MIF-Datei. Muss entweder mit den Optionen install (-i), Remove (-x), administrative Installation (-a) oder installieren Sie (-f) verwendet werden. Der ISMIF32.DLL wird als Teil von SMS installiert und muss sich im Pfad befinden.<br/> Die Felder der MIF-Statusdatei sind mit den folgenden Informationen gefüllt:<br/> Hersteller- <a href="author-summary.md"> <strong>Autor</strong></a><br/> Produkt- <a href="revision-number-summary.md"> <strong>Revisionsnummer</strong></a><br/> Version- <a href="subject-summary.md"> <strong>Subject</strong></a><br/> Locale- <a href="template-summary.md"> <strong>Template</strong></a><br/> Seriennummer-nicht festgelegt<br/> Installation: ISMIF32.DLL auf &quot; DateTime festgelegt.&quot;<br/> InstallStatus- &quot; Erfolg &quot; oder &quot; Fehler&quot;<br/> Beschreibung: Fehlermeldungen in der folgenden Reihenfolge: 1) vom Installationsprogramm generierte Fehlermeldungen. 2) Ressource aus Msi.dll, wenn die Installation nicht starten oder Benutzer beenden konnte. 3) systemfehlermeldungs-Datei. 4) formatierte Nachricht: &quot; Installationsfehler% i &quot; , wobei% i Fehler von Msi.dll zurückgegeben wird.<br/></td>
</tr>
<tr class="even">
<td><strong>/p</strong></td>
<td><em>Patchpaket [;p atchpackage2</em> ]</td>
<td>Wendet einen Patch an. Zum Anwenden eines Patches auf ein installiertes administratives Image müssen Sie die folgenden Optionen kombinieren:<br/> /p <em> <PatchPackage> [;p atchpackage2] </em> /a<em><Package></em><br/></td>
</tr>
<tr class="odd">
<td><strong>/q</strong></td>
<td>n | b | r | f</td>
<td>Legt die <a href="user-interface-levels.md">Benutzeroberflächen Ebene</a>fest.<br/> q, Qn-keine Benutzeroberfläche<br/> QB- <a href="b-gly.md"><em>grundlegende Benutzeroberfläche</em></a>. Verwenden Sie qb! , um die Schaltfläche <strong>Abbrechen</strong> auszublenden.<br/> QR: <a href="r-gly.md"><em>reduzierte Benutzeroberfläche</em></a> ohne modales Dialogfeld wird am Ende der Installation angezeigt.<br/> QR: <a href="f-gly.md"><em>vollständige Benutzeroberfläche</em></a> und alle erstellten <a href="fatalerror-dialog.md">modalerror</a>-, <a href="userexit-dialog.md">Userexit</a>-oder <a href="exit-dialog.md">Exit</a> -modalen Dialogfelder am Ende.<br/> Qn +-keine Benutzeroberfläche außer einem modalen Dialogfeld, das am Ende angezeigt wird.<br/> QB +- <a href="b-gly.md"><em>grundlegende Benutzeroberfläche</em></a> mit einem modalen Dialogfeld, das am Ende angezeigt wird. Das modale Feld wird nicht angezeigt, wenn der Benutzer die Installation abbricht. Verwenden Sie qb +! oder QB! +, um die Schaltfläche " <strong>Abbrechen</strong> " auszublenden.<br/> qb: <a href="b-gly.md"><em>grundlegende Benutzeroberfläche</em></a> ohne modale Dialogfelder. Beachten Sie, dass/QB +-keine unterstützte UI-Ebene ist. Verwenden Sie qb-! oder qb!-um die Schaltfläche " <strong>Abbrechen</strong> " auszublenden.<br/> Beachten Sie, dass! die Option ist in Windows Installer 2,0 verfügbar und funktioniert nur mit der grundlegenden Benutzeroberfläche. Dies ist mit der vollständigen Benutzeroberfläche nicht zulässig.<br/></td>
</tr>
<tr class="even">
<td><strong>/?</strong> oder <strong>/h</strong></td>
<td> </td>
<td>Zeigt die Copyright Informationen für Windows Installer an.<br/></td>
</tr>
<tr class="odd">
<td><strong>/y</strong></td>
<td><em>Mond</em></td>
<td>Ruft die Systemfunktion <strong>DllRegisterServer</strong> für selbst registrierte Module auf, die in der Befehlszeile weitergegeben werden. Geben Sie den vollständigen Pfad zur DLL an. Beispielsweise können Sie für MY_FILE.DLL im aktuellen Ordner Folgendes verwenden:<br/> <strong>msiexec/y .\MY_FILE.DLL</strong><br/> Diese Option wird nur für Registrierungsinformationen verwendet, die nicht mithilfe der Registrierungs Tabellen der MSI-Datei hinzugefügt werden können.<br/></td>
</tr>
<tr class="even">
<td><strong>"/z</strong></td>
<td><em>Mond</em></td>
<td>Ruft die Systemfunktion <strong>DllUnregisterServer</strong> auf, um die Registrierung der in der Befehlszeile weiter gegebenen Module aufzuheben. Geben Sie den vollständigen Pfad zur DLL an. Beispielsweise können Sie für MY_FILE.DLL im aktuellen Ordner Folgendes verwenden: <br/> <strong>msiexec "/z .\MY_FILE.DLL</strong><br/> Diese Option wird nur für Registrierungsinformationen verwendet, die nicht mithilfe der Registrierungs Tabellen der MSI-Datei entfernt werden können.<br/></td>
</tr>
<tr class="odd">
<td><strong>/c</strong></td>

<td>Gibt eine neue Instanz des Produkts an. Muss zusammen mit/t. verwendet werden. Verfügbar ab der Windows Installer Version, die in Windows Server 2003 und Windows XP mit Service Pack 1 (SP1) enthalten ist.<br/></td>
</tr>
<tr class="even">
<td><strong>/n</strong></td>
<td><em>ProductCode</em></td>
<td>Gibt eine bestimmte Instanz des Produkts an. Wird verwendet, um eine Instanz zu identifizieren, die mithilfe der Unterstützung mehrerer Instanzen über einen Produktcode zum Ändern von Transformationen installiert Verfügbar ab der Windows Installer Version, die mit Windows Server 2003 und Windows XP mit SP1 ausgeliefert wird. <br/></td>
</tr>
</tbody>
</table>



 

Die Optionen/i,/x,/f \[ p \| o \| e \| d \| c \| a \| u \| m \| s \| v \] ,/j \[ u \| m \] ,/a,/p,/y und "/z sollten nicht gleichzeitig verwendet werden. Die einzige Ausnahme von dieser Regel besteht darin, dass für das Patchen einer [administrativen Installation](administrative-installation.md) sowohl/p als auch/a verwendet werden müssen. Die Optionen/t,/c und/g sollten nur mit/j. verwendet werden. Die Optionen/l und/q können mit/i,/x,/f \[ p \| o \| e \| d \| c \| a \| u \| m \| s \| v \] ,/j \[ u \| m \] ,/a und/p verwenden. verwendet werden. Die Option/n kann mit/i,/f,/x und/p verwenden. verwendet werden.

Installieren Sie zum Installieren eines Produkts von a: \\Example.msi das Produkt wie folgt:

**msiexec/i A: \\Example.msi**

Nur [öffentliche Eigenschaften](public-properties.md) können mithilfe der Befehlszeile geändert werden. Alle Eigenschaftsnamen in der Befehlszeile werden als Großbuchstaben interpretiert, aber der Wert behält die Groß-/Kleinschreibung bei. Wenn Sie " **MyProperty** " in einer Befehlszeile eingeben, überschreibt das Installationsprogramm den Wert von "MyProperty" und nicht den Wert von " **MyProperty** " in der Eigenschaften Tabelle. Weitere Informationen finden Sie unter Informationen [zu Eigenschaften](about-properties.md).

Verwenden Sie die folgende Syntax in der Befehlszeile, um ein Produkt zu installieren, wobei die Eigenschaft auf Wert festgelegt ist. Sie können die Eigenschaft an eine beliebige Stelle mit Ausnahme einer Option und ihres Arguments platzieren.

Richtige Syntax:

**msiexec/i A: \\Example.msi Eigenschaft = Wert**

Falsche Syntax:

**msiexec/i Property = Wert A: \\Example.msi**

Eigenschaftswerte, die Literalzeichenfolgen sind, müssen in Anführungszeichen eingeschlossen werden. Schließen Sie alle Leerzeichen in der Zeichenfolge zwischen den Markierungen ein.

**msiexec/i A: \\Example.msi Property = "eingebetteter Leerraum"**

Wenn Sie eine öffentliche Eigenschaft über die Befehlszeile löschen möchten, legen Sie Ihren Wert auf eine leere Zeichenfolge fest.

**msiexec/i A: \\Example.msi-Eigenschaft = ""**

Schließen Sie den Abschnitt mit einem zweiten paar von Anführungszeichen in Textabschnitte ein, die durch literalanführungs Zeichen festgelegt wurden.

**msiexec/i A: \\Example.msi Property = "Embedded" "Anführungszeichen" "Leerzeichen"**

Das folgende Beispiel zeigt eine komplizierte Befehlszeile.

**msiexec/i testdb.msi INSTALLLEVEL = 3/l \* MSI. log CompanyName = "Acme" "Widgets" "und" "Gizmos." "**

Im folgenden Beispiel werden Ankündigungs Optionen gezeigt. Beachten Sie, dass bei Switches keine Groß-/Kleinschreibung beachtet wird

**msiexec/JM msisample.msi/T Transform. MST/Lime logfile.txt**

Im folgenden Beispiel wird gezeigt, wie Sie eine neue Instanz eines Produkts installieren, das angekündigt wird. Dieses Produkt wird erstellt, um mehrere instanztransformationen zu unterstützen.

**msiexec/JM msisample.msi/T: instance1. MST; Anpassung. MST/c/Lime logfile.txt**

Im folgenden Beispiel wird gezeigt, wie eine Instanz eines Produkts, das mithilfe mehrerer instanztransformationen installiert wird, gepatcht wird.

**msiexec/p msipatch. msp; msipatch2. msp/n {00000001-0002-0000-0000-624474736554} /qb**

Wenn Sie Patches auf ein bestimmtes Produkt anwenden, können die Optionen/i und/p nicht gleichzeitig in einer Befehlszeile angegeben werden. In diesem Fall können Sie Patches wie folgt auf ein Produkt anwenden.

**msiexec/i A: \\Example.msi Patch = msipatch. msp; msipatch2. msp/QB**

Die [**Patch**](patch.md) -Eigenschaft kann nicht in einer Befehlszeile festgelegt werden, wenn die/p-Option verwendet wird. Wenn die **Patch** -Eigenschaft festgelegt wird, wenn die/p-Option verwendet wird, wird der Wert der **Patch** -Eigenschaft ignoriert und überschrieben.

 

