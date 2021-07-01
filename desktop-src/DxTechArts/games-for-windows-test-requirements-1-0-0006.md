---
title: Testfälle für Spiele für Windows; bewährte Methoden für Spiele für Windows XP, Windows Vista, Windows 7 und Windows 8
description: Dieser Artikel enthält Testfälle für Spiele für Windows.
ms.assetid: bbe84d3f-e7ff-f14f-ec25-ae1c980749fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b13a4934c539579e49c9b00c60f3603bd64c711
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120275"
---
# <a name="games-for-windows-test-cases-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a>Spiele für Windows-Testfälle: Bewährte Methoden für Spiele unter Windows XP, Windows Vista, Windows 7 und Windows 8

Dieser Artikel enthält Testfälle für Spiele für Windows.

## <a name="how-to-use-this-article"></a>Zur Verwendung dieses Artikels

Dieser Artikel enthält drei Hauptabschnitte:

<dl> <dt>

<span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Testanforderungen**
</dt> <dd>

Jede Testanforderung in diesem Dokument enthält vier Hauptabschnitte: einen Titel und eine Tabelle mit drei wesentlichen Abschnitten (linke Spalte, rechts oben, rechts unten).

<dl> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Titel
</dt> <dd>

Name des Testfalles.

</dd> <dt>

<span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Feld, spalte ganz links
</dt> <dd>

Namen der Betriebssysteme, für die der Testfall gilt.

</dd> <dt>

<span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, rechts oben
</dt> <dd>

Kurze Zusammenfassung des Testfalles.

</dd> <dt>

<span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, rechts unten
</dt> <dd>

Details zum tatsächlichen Testfall.

</dd> </dl> </dd> <dt>

<span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Beispieltestskript**
</dt> <dd>

Dieser Abschnitt ist ein Beispiel für die Sequenz, der ein typischer Testlauf folgen würde, wenn die Testanforderungen als Leitfaden verwendet werden.

</dd> <dt>

<span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Hinweise zum Testtool**
</dt> <dd>

Dieser Abschnitt enthält ausführliche Hinweise zu den einzelnen Testtools, die zum Überprüfen von Pass- oder Fail-Bedingungen in den Testanforderungen verwendet werden.

</dd> </dl>

## <a name="test-requirements"></a>Testanforderungen

### <a name="1-game-requirements"></a>1. Spielanforderungen

### <a name="11-windows-games-explorer"></a>1.1 Windows Games Explorer



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Das Spiel muss im Spiele-Explorer unter Windows Vista und Windows 7 sichtbar sein. Wenn diese Option ausgewählt ist, muss das Spiel auch die richtigen Metadaten anzeigen. Die Installation darf keine Verknüpfung erstellen, um das Spiel auf dem Desktop, in der Startmenü oder an einem anderen Ort zu starten. Tasks und Verknüpfungen zum Entfernen dürfen nicht erstellt werden.</td>
</tr>
<tr class="even">

<td><ol>
<li>Öffnen Sie nach der Installation des Spiels den Spiele-Explorer.</li>
<li>Vergewissern Sie sich, dass das Spielsymbol im Spiele-Explorer angezeigt wird.</li>
<li>Klicken Sie mit der rechten Maustaste auf das Symbol, und testen Sie jede anwendungsdefinierte Wiedergabe & Supportaufgabe.</li>
<li>Klicken Sie auf das Symbol, und überprüfen Sie, ob die Metadaten (Herausgeber, Entwickler, Genre, Veröffentlichungsdatum, Version) unten angezeigt werden und richtig sind.</li>
<li>Vergewissern Sie sich, dass auf dem Spielsymbol WeI-Informationen (Windows Experience Index) im Spiele-Explorer angezeigt werden.</li>
<li>Vergewissern Sie sich, dass Die Spiellinks für Metadaten im Spiele-Explorer ordnungsgemäß funktionieren. (Wenn Links nicht angezeigt werden, ist dies ein mögliches Zeichen dafür, dass die EXE-Datei nicht signiert ist. Weitere Informationen finden Sie in Abschnitt <a href="#23-sign-files">2.3.)</a></li>
<li>Vergewissern Sie sich, dass das Spiel im Spiele-Explorer eine genaue Bewertung der Jugendkontrolle anzeigt. (Wenn es nicht wert ist, überprüfen Sie, ob es sich um ein nichtratiertes Spiel handelt. Andernfalls ist dies ein Indikator dafür, dass die EXE-Datei nicht signiert ist. Weitere Informationen finden Sie in Abschnitt <a href="#23-sign-files">2.3.)</a></li>
<li>Stellen Sie sicher, dass das Spiel keine Startverknüpfungen auf dem Benutzerdesktop abspielt.</li>
<li>Klicken Sie auf Start -> Alle Programme.</li>
<li>Stellen Sie sicher, dass das Spiel keine Startverknüpfungen im Startmenü abspielt.</li>
<li>Stellen Sie sicher, dass das Spiel keine Deinstallationsverknüpfungen außerhalb des Startmenüs Systemsteuerung.</li>
<li>Wenn das Spiel digital verteilt wird, überprüfen Sie, ob der Dienstanbieter im Windows Games Explorer angezeigt wird.</li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="12-windows-family-safety--parental-controls"></a>1.2 Windows Family Safety/Jugendschutz



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Das Spiel muss im Kontext eines &quot; Standardbenutzers ausgeführt &quot; werden. Die Jugendschutzkontrollen müssen in der Lage sein, das Spiel zu blockieren. Stellen Sie sicher, dass die GDF ÜBER EXE-Namen verfügt.</td>
</tr>
<tr class="even">

<td><ol>
<li>Erstellen Sie in Windows Vista oder Windows 7 ein Standardbenutzerkonto namens Toby. Start -> Systemsteuerung -> Add or Remove User Accounts -> Create New Account</li>
<li>Richten Sie als Jane über das Administratorkonto die Jugendschutzkontrollen für das Spiel ein. Start -> Systemsteuerung -> Einrichten von Jugendschutz für jeden Benutzer – > Toby
<ol>
<li>Vergewissern Sie sich, dass das Spiel über das Symbol "Spiele-Explorer" gestartet wird.</li>
<li>Vergewissern Sie sich, dass das Spiel eine genaue Jugendkontrollbewertung unterhalb des Spieltitels im Jugendkontrollfenster Systemsteuerung.</li>
<li>Vergewissern Sie sich vor dem Anwenden von Jugendschutz, dass das Spiel beim Start nicht zur Eingabe von Administratoranmeldeinformationen aufgefordert wird.</li>
<li>Legen Sie Jugendschutz auf &quot; Ein &quot; fest.</li>
<li>Klicken Sie im Abschnitt Windows-Einstellungen auf Spiele.</li>
<li>Klicken Sie auf OK (die Einstellung sollte jetzt &quot; AO/alle Spiele &quot; sein).</li>
<li>Vergewissern Sie sich, dass das Spiel mit diesen Einstellungen als User Jane ausgeführt wird.</li>
<li>Melden Sie sich als Jane ab, und melden Sie sich als Toby an.</li>
<li>Vergewissern Sie sich, dass das Spiel mit diesen Einstellungen als User Toby ausgeführt wird.</li>
<li>Melden Sie sich als Toby ab, und melden Sie sich als Jane an.</li>
<li>Wechseln Sie zurück zum vorherigen Bildschirm, und wählen &quot; Sie Spielbewertungen festlegen &quot; aus.</li>
<li><p>Wählen Sie eine Bewertung aus, die niedriger als die ESRB-Bewertung des Spiels ist.</p>
<blockquote>
[!Note]<br />
Wenn das Spiel nicht bewertet wird, überspringen Sie diesen Schritt, und fahren Sie mit dem nächsten Teil dieses Tests fort. Es kann erforderlich sein, ein anderes Bewertungssystem zu wählen, um eine Spielbewertung zu finden. Dies hängt vom Sprachdirigenz der zu testenden SKU ab.
</blockquote>
<p><br/></p></li>
<li>Melden Sie sich als Jane ab, und melden Sie sich als Toby an.</li>
<li>Vergewissern Sie sich, dass das Spiel für User Toby nicht gestartet wird, wenn ESRB von User Jane blockiert wird.</li>
<li>Melden Sie sich als Toby ab, und melden Sie sich als Jane an.</li>
<li>Wiederherstellen Sie die ESRB-Einstellungen, wenn Sie dies zuvor geändert haben.</li>
<li>Wenn es keine ESRB-Einstellungen gibt, wählen Sie Blockieren oder Bestimmte Spiele zulassen aus, &quot; und wählen Sie das Spiel nach Namen &quot; aus.</li>
<li>Melden Sie sich als Jane ab, und melden Sie sich als Toby an.</li>
<li>Vergewissern Sie sich, dass das Spiel für User Toby nicht gestartet wird, wenn EXE/Name von User Jane blockiert wird.</li>
<li>Melden Sie sich als Toby ab, und melden Sie sich wieder als Jane an.</li>
<li>Öffnen Sie als Jane benutzersteuerelemente -> Anwendungseinschränkungen.</li>
<li>Klicken Sie auf Toby kann nur die von mir zulässigen Programme verwenden, und klicken Sie auf &quot; &quot; OK (d. h. keine EXE-Dateien zulassen).</li>
<li>Wechseln Sie zu Benutzersteuerelemente | Spiele steuert und lässt das spezifische Spiel mit der ESRB-Bewertung zu.</li>
<li>Melden Sie sich als Jane ab, melden Sie sich als Toby an, und versuchen Sie, das Spiel zu spielen.</li>
<li>Vergewissern Sie sich, dass das Spiel NICHT blockiert ist und dass Toby es spielen kann, wenn &quot; allow no exes &quot; festgelegt ist.</li>
</ol></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="13-windows-vista-rich-saved-games"></a>1.3 Windows Vista Rich Saved Games

Diese Anforderung wurde nicht mehr erfüllt.

### <a name="14-xbox-360-common-controller-for-windows-conditional-requirement"></a>1.4 Xbox 360 Common Controller für bedingte \[ Windows-Anforderungen\]



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Spiele, die Gamepad-Controller unterstützen, müssen den Xbox 360 Controller für Windows mithilfe der XInput-API unterstützen. Alle Verweise auf allgemeine Controllertrigger und Schaltflächen müssen die Xbox 360 verwenden.</td>
</tr>
<tr class="even">

<td><ol>
<li>Starten Sie das Spiel.</li>
<li>Wechseln Sie zu den Controlleroptionen. **</li>
<li>Stellen Sie sicher, dass das Spiel Xbox 360 Controller für Windows als Eingabegerät erkennt.</li>
<li>Spielen Sie das Spiel, und überprüfen Sie, ob das Spiel- und Menüsystem mit dem Xbox 360 Controller für Windows steuerbar ist.</li>
<li>Vergewissern Sie sich Xbox 360 dass sich der Xbox 360-Controller für Windows gemäß den akzeptierten Standards verhält. (B für "Zurück", "A" für "Akzeptieren", "Starten" für im Spielmenü/Anhalten oder Akzeptieren usw.)</li>
<li>Stellen Sie sicher, dass das Spiel auf die Controllerschaltflächen und Trigger verweist, Xbox 360 verwenden.</li>
</ol>
<br/>
<blockquote>
[!Note]<br />
Wenn das Spiel keinen Gamecontroller unterstützt und/oder nur Tastatur/Maus unterstützt, überspringen Sie diesen Testfall.
</blockquote>
<br/> ** Einstellungen für den Controller befinden sich möglicherweise außerhalb des Spiels. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="15-multiple-aspect-ratios-and-resolutions"></a>1.5 Mehrere Seitenverhältnisse und Auflösungen



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Das Spiel muss mindestens die folgenden Seitenverhältnisse und die zugehörigen Bildschirmauflösungen unterstützen: <br/>
<ul>
<li>4:3 &quot; normal &quot; (800 600 oder 1024 768)</li>
<li>16:9 &quot; Widescreen &quot; (1280 720)</li>
<li>16:10 &quot; Widescreen &quot; (1152 720, 1680 1050 oder 800 480)</li>
</ul></td>
</tr>
<tr class="even">

<td>Suchen Sie nach den Videooptionen für das Spiel (dies kann in unserem Out-of-Game sein).<br/>
<blockquote>
[!Note]<br />
Die folgenden Tests müssen auf einem Widescreen-Monitor durchgeführt werden.
</blockquote>
<br/>
<ol>
<li>Wählen Sie im Abschnitt Videoauflösung die Option 800 600 oder 1024 768 aus.</li>
<li>Überprüfen Sie, ob das Spiel mit einer Auflösung von 4:3 Seitenverhältnis ausgeführt wird.</li>
<li>Wählen Sie im Abschnitt video resolution (Videoauflösung) die Option 1280 720 aus.</li>
<li>Vergewissern Sie sich, dass das Spiel mit einer Auflösung von 16:9 Seitenverhältnis ausgeführt wird.</li>
<li>Wählen Sie im Abschnitt Videoauflösung die Option 1680 1050, 800 480 oder 1152 720 aus.</li>
<li>Stellen Sie sicher, dass das Spiel mit einer Auflösung von 16:10 Seitenverhältnis ausgeführt wird.</li>
<li>Stellen Sie sicher, dass das Spiel das Bild nicht streckt und wiederum einen breiteren Ansichtsbereich zeigt.</li>
<li>Stellen Sie sicher, dass der Benutzer vom Spiel aufgefordert wird, wenn eine Änderung an der Lösung vorgenommen wird.</li>
<li>Wenn der Benutzer nicht innerhalb von 15 Sekunden akzeptiert, stellen Sie sicher, dass die Anzeige auf die vorherige Einstellung zurückverwendet wird.</li>
<li>Stellen Sie sicher, dass das Spiel links und rechts vom Spielbereich keine schwarzen Balken hinzufüge. (In diesem Fall wird der Spielbereich in der Mitte des Bildschirms noch im Verhältnis 4:3 angezeigt.)</li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="16-windows-media-center"></a>1.6 Windows Media Center

Diese Anforderung wurde nicht mehr erfüllt.

### <a name="17-direct3d-conditional-requirement"></a>1.7 Bedingte \[ Direct3D-Anforderung\]



| Betriebssystem                                                                    | Anforderung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows 7<br/> Windows Vista<br/> Windows XP<br/> | Wenn das Spiel Direct3D verwendet, muss die unterstützte Mindestversion Direct3D 9 und Direct3D der Standard für jede Anzeigekonfigurationsoption sein.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|     <dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuell</dt> <dd> Starten Sie das Spiel. Überprüfen Sie in den Videooptionen, ob Renderoptionen wie D3D und/oder OpenGL verfügbar sind. Wenn dies der Standard ist, überprüfen Sie, ob die Renderoptionen für das Spiel direct3D sind. Wenn Sie nicht überprüfen können, ob D3D9 die verwendete DirectX-Version ist, fahren Sie mit Automatisierter Test fort. <br/> </dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automatisierter Test</dt> <dd> Tool verwenden: Depends.exe <br/> </dd> </dl> |



 

### <a name="18-enable-high-dpi-aware"></a>1.8 Aktivieren von "High-DPI Aware" (Hohe DPI-Leistung)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Spiele und ihre Installationsprogramme müssen ohne visuelle Probleme ordnungsgemäß ausgeführt werden, wenn die DPI-Skalierung aktiviert ist.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuell</dt> <dd>
<ol>
<li>Legen Sie das System auf DPI 150 % fest: <br/> Windows Vista: Systemsteuerung: Personalisierung, Anpassen des Schriftgrads (DPI), BenutzerdefinierteR DPI. Legen Sie auf 150 % fest.<br/> Windows 7: Systemsteuerung: Display, Set to Larger - 150%.<br/></li>
<li>Führen Sie den Installationsvorgang und das Spiel aus, um sicherzustellen, dass keine Probleme mit abgeschnittenen Bildschirmen oder Dialogfeldern auftreten.</li>
</ol>
</dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automatisierter Test</dt> <dd> Stellen Sie sicher, <dpiAware>dass das Element true</dpiAware> im eingebetteten Manifest enthalten ist.<br/> Tool verwenden: Mt.exe <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="2-security-and-compatibility"></a>2. Sicherheit und Kompatibilität

### <a name="21-follow-user-account-control-guidelines"></a>2.1 Befolgen Sie die Richtlinien für die Benutzerkontensteuerung.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Jede ausführbare Datei (.EXE Erweiterung), die in einer Anwendung enthalten ist, muss über ein eingebettetes Manifest verfügen, das die Ausführungsebene definiert:
<pre class="syntax" data-space="preserve"><code><requestedExecutionLevel level=&quot;asInvoker|highestAvailable|requireAdministrator&quot; 
              uiAccess=&quot;true|false&quot;/></code></pre>
<br/>
<blockquote>
[!Note]<br />
Bei Spielen und Spieleinstallern sollte uiAccess immer auf FALSE festgelegt &quot; &quot; werden.
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><ol>
<li>Überprüfen Sie, ob ausführbare Dateien des Spiels Manifeste enthalten.</li>
<li>Vergewissern Sie sich, dass das ausführbare Dateimanifest des Spiels requestedExecutionLevel &quot; auf AsInvokerfestlegt &quot; ist.</li>
</ol>
Tool verwenden: Mt.exe <br/></td>
</tr>
</tbody>
</table>



 

### <a name="22-support-x64-versions-of-windows"></a>2.2 Unterstützung von x64-Versionen von Windows



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>So gewährleisten Sie die Kompatibilität mit x64-Versionen von Windows: <br/>
<ul>
<li>Titel- und Titelinstallationsprogramme dürfen keinen 16-Bit-Code enthalten oder 16-Bit-Komponenten verwenden.</li>
<li>Wenn das Spiel für den Betrieb von Kernelmodustreibern abhängig ist, müssen x64-Versionen dieser Treiber verfügbar sein. Das Spielsetup muss die richtigen Treiber und Komponenten für 64-Bit-Editionen von Windows erkennen und installieren.</li>
</ul>
<blockquote>
[!Note]<br />
Die Unterstützung für die 64-Bit-Edition von Windows XP Professional ist optional.
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td>Manueller Test<br/>
<ol>
<li>Führen Sie das Spiel auf 64-Bit-Editionen von Windows aus. Stellen Sie sicher, dass der Spielinstallationsprozess normal auf 64-Bit-Editionen von Windows Vista oder Windows 7 ausgeführt wird.</li>
<li>Stellen Sie sicher, dass für das Spiel kein Fehler als Ergebnis von ausführbaren 16-Bit-Dateien in 64-Bit-Editionen von Windows Vista oder Windows 7 auftritt. Der Fehler erwähnt die 16-Bit-Anwendung im Fehlerfenster.</li>
<li>Wenn das Spiel über eine native ausführbare 64-Bit-Datei verfügt, verwenden Sie diese auch.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="23-sign-files"></a>2.3 Signieren von Dateien



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Alle ausführbaren Codedateien (z. B. .exe erweiterungen .dll) müssen mit einem Authenticode-Zertifikat signiert sein. <br/> Wenn Sie Windows Installer, müssen die Paketdateien (.msi Dateien) des Installationsprogramms signiert sein. <br/></td>
</tr>
<tr class="even">

<td>Manueller Test<br/>
<ol>
<li>Navigieren Sie zum Spielverzeichnis.</li>
<li>Suchen Sie nach allen .exe und .dll Dateien.</li>
<li>Klicken Sie für jede Datei mit der rechten Maustaste auf Eigenschaften.</li>
<li>Überprüfen Sie, ob die ausführbaren Dateien des Spiels eine digitale Signatur enthalten.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="24-sign-drivers"></a>2.4 Signieren von Treibern



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Jeder Kernelmodustreiber, der vom Spiel installiert wird, muss mit einem öffentlich gültigen Authenticode-Zertifikat signiert werden. <br/> Jeder Hardwaregerätetreiber im Kernelmodus, der vom Spiel installiert wird, muss über eine Microsoft-Signatur verfügen, die über das Windows Hardware Quality Labs-Programm (WHQL) oder drS-Programm (Driver Reliability Signature) erworben wurde. <br/></td>
</tr>
<tr class="even">

<td>Manueller Test<br/>
<ol>
<li>Installieren Sie das Spiel.</li>
<li>Vergewissern Sie sich, dass bei der Installation des Spiels keine Dialogfelder mit nicht signierten Treibern angezeigt werden.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="25-perform-version-checking-properly"></a>2.5 Ordnungsgemäßes Durchführen der Versionsüberprüfung



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Spiele dürfen nicht auf zukünftigen Betriebssystemen ausgeführt werden, wie durch Änderungen an der Windows-Versionsnummer angegeben, es sei denn, der Endbenutzer-Lizenzvertrag untersagt die Verwendung auf zukünftigen Betriebssystemen. Wenn das Spiel fehlschlagen soll, muss es dies ordnungsgemäß tun, indem dem Benutzer eine Meldung angezeigt wird.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuell</dt> <dd>
<ol>
<li>Installieren Sie das Spiel unter Windows XP, auf 32-Bit-Editionen von Windows Vista und Windows 7 sowie auf 64-Bit-Editionen von Windows Vista und Windows 7.</li>
<li>Stellen Sie sicher, dass bei der Spieleinstallation kein Fehler in Bezug auf die Betriebssystemversion auftritt.</li>
</ol>
</dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automatisierter Test</dt> <dd> Tool verwenden: Application Verifier<br/>
<ol>
<li>Starten Application Verifier.</li>
<li>Aktivieren Sie den Test Compatibility:HighVersionLie, nachdem Sie die INSTALL.EXE.</li>
<li>Installieren Sie das Spiel, und stellen Sie sicher, dass die Installation nicht basierend auf der Betriebssystemversion blockiert wird.</li>
<li>Aktivieren Sie den Test Compatibility:HighVersionLie, nachdem Sie die GAME.EXE.</li>
<li>Führen Sie das Spiel aus, und stellen Sie sicher, dass die Ausführung nicht basierend auf der Betriebssystemversion blockiert wird.</li>
</ol>
</dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="26-support-concurrent-user-sessions"></a>2.6 Unterstützung gleichzeitiger Benutzersitzungen



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Spiele müssen Standardmäßige Windows-Multitaskingszenarien unterstützen.</td>
</tr>
<tr class="even">

<td>Erstellen Sie in Windows Vista oder Windows 7 ein Standardbenutzerkonto namens Toby. Start -> Systemsteuerung -> Add or Remove User Accounts -> Create New Account <br/>
<ol>
<li>Starten Sie das Spiel als User Jane.</li>
<li>ALT+TAB zurück zum Desktop.</li>
<li>Vergewissern Sie sich, dass das Spiel ordnungsgemäß ALT+TABs auf dem Windows-Desktop installiert.</li>
<li>Klicken Sie auf Start -> [Pfeil rechts neben Sperren] -> Benutzer wechseln.</li>
<li>Melden Sie sich als User Toby an.</li>
<li>Vergewissern Sie sich, dass das Spiel als User Toby gestartet wird, während es weiterhin als User Jane ausgeführt wird.</li>
<li>Stellen Sie sicher, dass im Spiel während des Benutzerwechselvorgangs keine Fehler für User Toby oder User Jane auftreten.</li>
<li>Wenn Sie eine weitere Spielsitzung starten können, vergewissern Sie sich, dass Sie keine Audiodaten aus der ursprünglichen Spielsitzung hören können.</li>
<li>Schließen Sie das Spiel, und wechseln Sie zurück zum ursprünglichen Benutzer und Spiel.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="27-support-long-names"></a>2.7 Unterstützung für lange Namen



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Wenn ein Spiel das Speichern von Dateien unterstützt, muss es in der Lage sein, Dateien mit langen Namen und Pfaden zu speichern. Das Spiel muss spezielle Dateisystemzeichen ordnungsgemäß verarbeiten, z. B. \ / : * ? &quot; < oder > in allen Benutzereingabefeldern, die zum Erstellen von Dateinamen oder Pfaden verwendet werden.</td>
</tr>
<tr class="even">

<td><ol>
<li>Starten Sie das Spiel.</li>
<li>Starten Sie ein neues Spiel.</li>
<li>Speichern Sie das Spiel. Vergewissern Sie sich während des Speichervorgangs, dass das Spiel mit dem Speichernamen "My First Save Game" (Mein erstes Spiel speichern) speichert.</li>
<li>Beenden Sie zurück zum Hauptmenü.</li>
<li>Versuchen Sie, das neu gespeicherte Spiel zu laden.</li>
<li>Stellen Sie sicher, dass beim Behandeln von nicht unterstützten Dateisystemzeichen keine Fehler auftreten, z. B. \ / : * ? &quot; < oder > Wenn das Spiel Es zulässt, benennen Sie das gespeicherte Spiel.</li>
<li>Wenn der Benutzer sein Profil benennen und/oder Zeichen verwenden oder Spiele speichern darf, stellen Sie sicher, dass beim Spiel auch hier keine Fehler auftreten, wenn lange Dateinamen verwendet werden.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="3-installation"></a>3. Installation

### <a name="31-easy-install"></a>3.1 Einfache Installation



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Spiele mit einer herkömmlichen Installation müssen einen vereinfachten Pfad in ihrer Setup-Benutzeroberfläche bereitstellen.</td>
</tr>
<tr class="even">

<td><ol>
<li>Fügen Sie den Spiel-Datenträger ein.</li>
<li>Vergewissern Sie sich, dass im Spiel nicht mehr als ein lizenzvertrag End-User angezeigt wird.</li>
<li>Wenn das Spiel eine benutzerdefinierte oder erweiterte Installationsoption unterstützt, überprüfen Sie, ob während des Installationsvorgangs auf diese Option zugegriffen werden kann.</li>
<li>Stellen Sie sicher, dass die Option Standardinstallation alle Benutzereingabeauswahlen für den Installationsvorgang umgeht (Auswahl des Installationsordners, Auswahl von Komponenten und so weiter).</li>
<li>Stellen Sie sicher, dass bei der Spieleinstallation keine Aufforderung zur Einrichtung von Betriebssystemkomponenten angezeigt wird (DirectX-Setup, Visual C-Runtimes und so weiter).</li>
<li>Stellen Sie sicher, dass bei der Spieleinstallation keine Aufforderung zur Firewallinteraktion angezeigt wird.</li>
<li>Vergewissern Sie sich, dass das Spiel automatisch ausgeführt wird oder dass am Ende des Installationsprozesses ein Startmenü vorhanden ist.</li>
<li>Stellen Sie sicher, dass beim Deinstallationsprozess des Spiels alle installierten, nicht neu verteilten Betriebssystemkomponentendateien entfernt und alle Einstellungen entfernt werden. Das Bereinigen aller Einstellungen und Daten pro Benutzer (z. B. gespeicherte Spiele) ist nicht erforderlich.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="32-support-user-account-control-for-installation"></a>3.2 Unterstützung der Benutzerkontensteuerung für die Installation



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Der Spieleinstaller darf nicht davon ausgehen, dass er im gleichen Kontext wie der Benutzer ausgeführt wird. Spiele müssen daher aufgaben pro Benutzer bei der ersten Ausführung getrennt von der Installation ausführen.</td>
</tr>
<tr class="even">

<td><ol>
<li>Vergewissern Sie sich, dass Sie das Spiel als User Jane installieren können. (Dies erfordert erhöhte Rechte während des Setup-/Installationsprozesses.)</li>
<li>Vergewissern Sie sich, dass benutzerin Jane während der Spieleinstallation aufgefordert wird, die Rechte mit Administratoranmeldeinformationen zu erhöhen. (Die Aufforderung zum Erhöhen der Rechte wird angezeigt, wenn der Benutzer versucht, die Installation zu versuchen.)</li>
<li>Entscheiden Sie sich dafür, das Spiel am Ende der Installation automatisch zu erstellen, falls dies noch nicht der Dere ist, oder starten Sie es über das angezeigte Menü.</li>
<li>Erstellen Sie nach dem Spiel ein neues Profil, spielen Sie ein Spiel, und speichern Sie es.</li>
<li>Beenden Sie das Spiel.</li>
<li>Starten Sie das Spiel neu, und überprüfen Sie, ob das User Jane-Konto auf Benutzerprofile und gespeicherte Spiele zugreifen kann.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="33-install-to-correct-folders"></a>3.3 Installieren in korrekten Ordnern



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Spiele müssen standardmäßig im Ordner "Programme" installiert werden. Benutzerdaten müssen bei der ersten Ausführung und nicht während der Installation geschrieben werden.</td>
</tr>
<tr class="even">

<td><ol>
<li>Installieren Sie das Spiel mithilfe des Standard-Installationstyps.</li>
<li>Vergewissern Sie sich, dass das Spiel unter Programme installiert wurde.</li>
</ol>
<blockquote>
[!Note]<br />
Wenn dieser Test fehlschlägt, überprüfen Sie, ob das Spiel für alle Benutzer installiert werden soll. Wenn dies der Fall ist, ist dies ein Fehler.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="34-install-windows-resources-properly"></a>3.4 Ordnungsgemäßes Installieren von Windows-Ressourcen



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Anwendungen dürfen nicht versuchen, Dateien oder Registrierungsschlüssel zu installieren, die durch Windows-Ressourcenschutz (WRP) geschützt sind.</td>
</tr>
<tr class="even">

<td><ul>
<li>Stellen Sie sicher, Windows-Ressourcenschutz WRP-Dialogfelder während des Installationsprozesses nicht angezeigt werden.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="35-avoid-reboots-during-installation"></a>3.5 Vermeiden von Neustarts während der Installation



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Das Spieleinstallationsprogramm sollte nicht davon ausgehen, dass die Installation von Windows-Komponenten aus Weiterverteilungspaketen einen Neustart erfordert, es sei denn, der Neustart wird durch ein Rückgabeergebnis oder in der Microsoft-Dokumentation angegeben.</td>
</tr>
<tr class="even">

<td><ol>
<li>Installieren Sie das Spiel.</li>
<li>Stellen Sie sicher, dass das System nach der Installation nicht neu gestartet werden muss.</li>
</ol>
<blockquote>
[!Note]<br />
Wenn ein Microsoft-Systemupdate REDIST einen Neustart erfordert, führen Sie folgende Schritte aus: Schließen Sie die Spieleinstallation ab, deinstallieren Sie das Spiel, und installieren Sie das Spiel ein zweites Mal neu. Der Spielinstallationsprozess sollte bei dieser zweiten Installation keinen Neustart erfordern.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="36-use-file-versioning-correctly"></a>3.6 Verwenden sie die Dateiversionsierung ordnungsgemäß.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Das Spielinstallationsprogramm muss ordnungsgemäß überprüfen, um sicherzustellen, dass die neuesten Dateiversionen installiert sind. Die Installation eines Spiels darf niemals Dateien zurückdrennen, die Sie nicht erzeugen oder die von Anwendungen freigegeben werden, die Sie nicht erstellen.</td>
</tr>
<tr class="even">

<td><ol>
<li>Erstellen Sie vor der Installation des Spiels eine Vorabmomentaufnahme von System32.<br/>
<ol>
<li>Erstellen Sie ein Verzeichnis mit dem Namen G4Wtest.</li>
<li>Öffnen Sie ein Befehlsfenster (Start -> Run -> cmd).</li>
<li>Navigieren Sie zu c:\windows\system32.</li>
<li>Geben Sie dir /o:-g /o:-d >> c:\G4Wtest\pregame.txt ein.</li>
</ol></li>
<li>Erstellen Sie eine Momentaufnahme von System32 nach der Installation. <br/>
<ol>
<li>Öffnen Sie ein Befehlsfenster (Start -> Run -> cmd).</li>
<li>Navigieren Sie zu c:\windows\system32.</li>
<li>Geben Sie dir /o:-g /o:-d >> c:\G4Wtest\postgame.txt ein.</li>
<li>Stellen Sie sicher, dass das Spiel keine Dateiversionen von Dateien zurückzieht, die das Spiel nicht erzeugt hat (... der in den beiden Dokumenten aufgeführten Dateien, indem pregame.txt mit postgame.txt) verglichen werden.</li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="37-support-autorun-conditional-requirement"></a>3.7 Unterstützung von bedingten \[ Autorun-Anforderungen\]



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Bei Spielen, die auf CD, DVD oder anderen Wechselmedien verteilt werden, die Autorun unterstützen, muss die Anwendung automatisch ausgeführt werden oder den Benutzer auffordern, das Spiel zu installieren, wenn der Datenträger zum ersten Mal eingefügt wird. <br/>
<blockquote>
[!Note]<br />
Autorun-Programme, die für die Verwendung in Windows-Versionen vor Windows Vista geschrieben wurden, sollten nicht die .NET-Runtime verwenden, da diese Technologie nicht in Windows XP oder älteren Versionen von Windows enthalten ist.
</blockquote>
<br/> Weitere Informationen finden Sie unter <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Games for Windows Technical Requirements</a> 3.7, Support Autorun. <br/></td>
</tr>
<tr class="even">

<td><ol>
<li>Fügen Sie die Spieldatenträger oder -medien ein.</li>
<li>Vergewissern Sie sich, dass das Dialogfeld "Installieren/Ausführen" automatisch angezeigt wird.</li>
<li>Windows Vista oder Windows 7: Vergewissern Sie sich, dass das Autorun-Programm für das Spiel selbst Benutzer Jane nicht auffordert, die Rechte über Administratoranmeldeinformationen zu erhöhen.</li>
<li>Vergewissern Sie sich, dass die ausführbare Datei Autorun keine vordefinierten REDIST-Komponenten wie .NET 3.5, C Run-Time Bibliotheken usw. benötigt.</li>
<li>Stellen Sie sicher, dass das erneute Einfügen des Datenträgers auf dem Laufwerk nach der Installation nicht dazu führt, dass die Installation automatisch erneut gestartet wird.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="4-reliability"></a>4. Zuverlässigkeit

### <a name="41-eliminate-unnecessary-reboots"></a>4.1 Vermeiden unnötiger Neustarts



| Betriebssystem                                              | Anforderung                                                                                                                                                                   |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows 7<br/> Windows Vista<br/> | Alle Anwendungsinstallationsprogramme müssen die Neustart-Manager-APIs nutzen, um Systemneustarts zu vermeiden (siehe [Anforderung 3.5).](#35-avoid-reboots-during-installation) |



 

### <a name="42-eliminate-application-verifier-failures"></a>4.2 Beseitigen von Application Verifier Fehlern



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Das Spiel darf in den folgenden Tests keine Fehler generieren, die unter Microsoft Application Verifier (AppVerifier), Version 4.0 oder höher, ausgeführt werden: <br/>
<ul>
<li>Grundlagen: Handles, Heaps, Sperren, Arbeitsspeicher, TLS</li>
<li>Sonstiges: DangerousAPIs, DirtyStacks</li>
</ul></td>
</tr>
<tr class="even">

<td>Tool verwenden: AppVerifier 4.0 (oder höher)<br/>
<ol>
<li>Installieren Sie AppVerifier.</li>
<li>Starten Sie AppVerifier, und wählen Sie Datei -> Anwendung hinzufügen aus.</li>
<li>Suchen Sie die ausführbare Spieldatei, wählen Sie sie aus, und klicken Sie auf die &quot; &quot; Schaltfläche Öffnen.</li>
<li>Wählen Sie im &quot; Abschnitt Anwendungen die ausführbare &quot; Spieldatei aus.</li>
<li>Wählen Sie im &quot; Abschnitt Tests unter den Kategorien Grundlagen und &quot; Sonstiges die oben aufgeführten Tests aus &quot; &quot; &quot; &quot; (deaktivieren Sie ThreadPool und TimeRollOver), und stellen Sie sicher, dass nicht alle anderen Tests ausgewählt sind.</li>
<li>Starten Sie das Spiel.</li>
<li>Vergewissern Sie sich, dass das Spiel keine Fehler generiert, wenn es unter Application Verifier ausgeführt wird.</li>
</ol>
<blockquote>
[!Note]<br />
Einige Tests erfordern, dass ein Debugger vollständig ausgeführt wird. Dies kann eine ungeschützte Releaseversion der ausführbaren Spieldatei erfordern, da die Antispickzettel-/Anti-Anti- antivirus-Technologie AppVerifer beeinträchtigen kann.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="43-support-windows-error-reporting"></a>4.3 Unterstützung Windows-Fehlerberichterstattung



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Spiele dürfen nur Ausnahmen behandeln, die bekannt und erwartet sind, und Windows-Fehlerberichterstattung dürfen nicht deaktiviert werden. Wenn ein Fehler (z. B. eine Zugriffsverletzung) in ein Spiel eingefügt wird, muss es Windows-Fehlerberichterstattung ermöglichen, den Absturz zu melden.</td>
</tr>
<tr class="even">

<td>Verwenden des Tools: Thread Auserzählen <br/>
<ul>
<li>Wenn die Anwendung beim Testen abstürzt, überprüfen Sie, ob das Spiel Windows-Fehlerberichterstattung ordnungsgemäß anzeigt und Absturzdaten sammelt.</li>
</ul></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Alle ausführbaren Dateien (z. B. .exe- oder .dll dateien) müssen einen genauen Produktnamen, Einen Firmennamen und eine Dateiversion enthalten.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Manueller Test:</dt> <dd>
<ol>
<li>Klicken Sie mit der rechten Maustaste auf die ausführbaren Dateien des Spiels sowohl auf dem Installationsmedium als auch auf den auf der Computerfestplatte installierten Dateien.</li>
<li>Wählen Sie „Eigenschaften“.</li>
<li>Windows XP: Klicken Sie auf die Registerkarte <strong>Version.</strong> Stellen Sie sicher, dass die Felder Produktname, Unternehmensname und Dateiversion ordnungsgemäß ausgefüllt sind.</li>
<li>Windows Vista oder Windows 7: Klicken Sie auf die Registerkarte <strong>Details.</strong> Vergewissern Sie sich, dass die Felder Produktname und Dateiversion ordnungsgemäß ausgefüllt sind. Der Unternehmensname ist auf der Eigenschaftenseite von Windows Vista oder Windows 7 nicht sichtbar.</li>
</ol>
</dd> <dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Automatisierter Test:</dt> <dd>
<ul>
<li>Verwenden sie das Microsoft Games for Windows Test Tool. siehe <a href="#64-microsoft-games-for-windows-test-tool">Abschnitt 6.4.</a></li>
</ul>
</dd> </dl></td>
</tr>
</tbody>
</table>



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Das normale Beenden des Spiels darf nicht zu einem unbekannten Ausnahmefehler führen.</td>
</tr>
<tr class="even">

<td><ul>
<li>Überprüfen Sie nach dem Spielen für eine normale Spielsitzung, ob das Spiel beim Beenden keine Fehler generiert.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="5-sample-test-script"></a>5. Beispieltestskript

Dies ist ein Beispiel für einen typischen Testdurchlauf, der die oben genannten Testanforderungen als Leitfaden verwendet.

### <a name="51-tools"></a>5.1 Tools

-   32-Bit-Edition von Windows Vista SP1 und/oder Windows 7 auf einer AMD-CPU
-   32-Bit-Edition von Windows Vista SP1 und/oder Windows 7 auf einer Intel-CPU
-   64-Bit-Edition von Windows Vista SP1 und/oder Windows 7 auf einer AMD-CPU
-   64-Bit-Edition von Windows Vista SP1 und/oder Windows 7 auf einer Intel-CPU
-   32-Bit-Edition Windows XP SP2 auf einer AMD-CPU
-   32-Bit-Edition Windows XP SP2 auf einer Intel-CPU
-   Breitbildschirmmonitor, der 1680 1050 unterstützt
-   Xbox 360 Controller für Windows

### <a name="52-pre-install"></a>5.2 Vorinstallation

1.  Windows Vista und Windows 7: Erstellen von zwei Standardbenutzern: Jane und Toby
2.  Windows Vista und Windows 7: Sicherstellen, dass die Benutzerkontensteuerung aktiviert ist
3.  Erstellen einer Vorinstallationsmomentaufnahme von System32

    1.  Erstellen eines Verzeichnisses mit dem Namen G4Wtest
    2.  Aufrufen eines Befehlsfensters (Start -> Run -> cmd)
    3.  Navigieren Sie zu c: \\ windows \\ system32.
    4.  Geben Sie dir /o:-g /o:-d >> c: \\ G4Wtest \\pregame.txt

4.  Windows Vista und Windows 7: Auf 150 % DPI \[ 1.8 festgelegt\]
5.  Fahren Sie mit [der Installation](#3-installation) fort.

### <a name="53-install"></a>5.3 Installieren

1.  Melden Sie sich als Benutzerin Jane an.
2.  Fügen Sie die Spieldatenträger in das CD/DVD-Laufwerk ein, und vergewissern Sie sich, dass das Dialogfeld "Installieren/Ausführen" automatisch \[ 3.7 angezeigt wird.\]
3.  Vergewissern Sie sich, dass der Spielinstallationsvorgang Benutzer Jane auffordert, die Administratoranmeldeinformationen \[ 3.2 zu erhöhen.\]
4.  Vergewissern Sie sich, dass das Autorun-Programm für das Spiel selbst Benutzer Jane nicht dazu auffordert, die Rechte über Administratoranmeldeinformationen \[ 3.7 zu erhöhen.\]
5.  Vergewissern Sie sich, dass im Spiel nicht mehr als ein End-User Lizenzvertrag (EULA) \[ 3.1 angezeigt wird.\]
6.  Vergewissern Sie sich, dass das Spiel die Installationsoptionen Standard/Einfach und Benutzerdefiniert/Erweitert \[ 3.1 anzeigt.\]
7.  Stellen Sie sicher, dass die Option Standardinstallation/Einfache Installation alle Benutzereingabeauswahlen für den Installationsvorgang umgeht (Auswahl des Installationsordners, Komponentenauswahl usw.). \[ 3.1\]
8.  Vergewissern Sie sich, dass der Spielinstallationsvorgang nicht zur Einrichtung von Betriebssystemkomponenten auffordert (DirectX-Setup, C Run-Time Bibliotheken usw.). \[ 3.1\]
9.  Vergewissern Sie sich, dass der Spielinstallationsvorgang nicht zur Eingabe der Firewallinteraktion \[ 3.1 auffordert.\]
10. Vergewissern Sie sich, dass bei der Spieleinstallation kein Fehler in Bezug auf Betriebssystemversion \[ 2.5 \] \[ 4.2 auftritt.\]
11. Vergewissern Sie sich, dass bei der Spieleinstallation keine Dialogfelder für nicht signierte Treiber \[ 2.4 angezeigt werden.\]
12. Vergewissern Sie sich, dass während des Installationsvorgangs 3.4 keine WRP-Dialoge (Windows-Ressourcenschutz) angezeigt werden. \[\]
13. Vergewissern Sie sich, dass das erneute Einfügen des Datenträgers auf dem Laufwerk nach der Installation nicht dazu führt, dass die Installation automatisch erneut gestartet wird.
14. Vergewissern Sie sich, dass das System nach Installation von 3.5 nicht neu gestartet werden muss. \[\]
15. Vergewissern Sie sich, dass Sie das Spiel als Benutzerin Jane \[ 3.2 installieren können.\]
16. Stellen Sie sicher, dass das Spiel automatisch ausgeführt wird oder dass am Ende des Installationsvorgangs 3.1 ein Startmenü vorhanden ist. \[\]
17. Wenn das Spiel nach der Installation automatisch ausgeführt wird, fahren Sie mit [Runtime](#55-runtime)
18. Wenn das Spiel ein Startmenü verlassen hat oder nicht deinstalliert werden konnte, finden Sie weitere Informationen im Abschnitt [Nach der Installation.](#54-post-install)

### <a name="54-post-install"></a>5.4 Nach der Installation

1.  Vergewissern Sie sich, dass das Spiel keine Startverknüpfungen auf benutzerdesktop \[ 1.1 eingibt.\]
2.  Vergewissern Sie sich, dass das Spiel keine Startverknüpfungen im Startmenü \[ 1.1 einsortiert.\]
3.  Überprüfen Sie, ob das Spielsymbol in Windows Games Explorer \[ 1.1 angezeigt wird.\]
4.  Überprüfen Sie, ob die Metadaten (Herausgeber, Entwickler, Genre, Veröffentlichungsdatum, Version) unten angezeigt werden und richtig \[ 1.1 sind.\]
5.  Überprüfen Sie, ob das Spielsymbol WeI-Informationen (Windows Experience Index) in Windows Games Explorer \[ 1.1 anzeigt.\]
6.  Überprüfen, ob Gamelinks für Metadaten in Windows Games Explorer \[ 1.1 ordnungsgemäß funktionieren\]
7.  Überprüfen Sie, ob das Spiel in Windows Games Explorer 1.1 eine genaue Bewertung der Jugendschutzsteuerung anzeigt. \[\]
8.  Erstellen einer Momentaufnahme von System32 nach der Installation

    1.  Aufrufen eines Befehlsfensters (Start -> Run -> cmd)
    2.  Navigieren Sie zu c: \\ windows \\ system32.
    3.  Geben Sie dir /o:-g /o:-d >> c: \\ G4Wtest \\postgame.txt
    4.  Stellen Sie sicher, dass das Spiel keine Dateiversionen der in den beiden Dokumenten aufgeführten Dateien zurückzieht, indem Sie pregame.txt mit postgame.txt \[ 3.6 vergleichen.\]

9.  Fahren Sie mit [runtime fort.](#55-runtime)

### <a name="55-runtime"></a>5.5 Runtime

1.  RUNTIME 1: Wenn das Startmenü vorhanden ist, starten Sie das Spiel von dort aus. Wenn das Spiel nach der Installation automatisch ausgeführt oder nach der Installation über das Menü des Spielstarts gestartet wurde, führen Sie Folgendes aus: Falls nicht, fahren Sie mit RUNTIME 2:

    1.  Erstellen eines Profils (wenn das Spiel dies zulässt)
    2.  Starten eines neuen Spiels
    3.  Speichern des Spiels
    4.  Beenden des Spiels
    5.  Starten des Spiels im Spiele-Explorer
    6.  Überprüfen Sie, ob das Spiel über das Symbol "Spiele-Explorer \[ 1.2" gestartet wird.\]
    7.  Vergewissern Sie sich, dass das Spiel beim Start 1.2 nicht zur Eingabe von Administratoranmeldeinformationen auffordert. \[\]
    8.  Vergewissern Sie sich, dass auf Benutzerprofile und Spiele speichern über das Benutzer-Jane-Konto 3.2 zugegriffen werden kann. \[\]
    9.  Fahren Sie mit RUNTIME 3 fort.

2.  RUNTIME 2: Wenn das Spiel nicht automatisch ausgeführt wurde oder einen Start über das Startmenü des Spiels anzeigte, ist dies ein Fehler von \[ 3.1. Die \] Tests können jedoch normal fortgesetzt werden:

    1.  Starten des Spiels im Spiele-Explorer
    2.  Überprüfen Sie, ob das Spiel über das Symbol "Spiele-Explorer \[ 1.2" gestartet wird.\]
    3.  Vergewissern Sie sich, dass das Spiel beim Start 1.2 nicht zur Eingabe von Administratoranmeldeinformationen auffordert. \[\]
    4.  Fahren Sie mit RUNTIME 3 fort.

3.  RUNTIME 3: Wenn das Spiel ein Spielpad unterstützt, überprüfen Sie, ob das Spiel Xbox 360 Controller für Windows als Eingabegerät \[ erkennt 1.4\]

    1.  Aktivieren Sie bei Bedarf den Controller über das Menü "Optionen".
    2.  Überprüfen Sie, ob das Spiel auf die Controllerschaltflächen und Trigger verweist, indem Sie Xbox 360 Namen verwenden.
    3.  Überprüfen Sie, ob spiel- und menüsystem mit dem Xbox 360 Controller für Windows steuerbar sind.
    4.  Überprüfen Sie, ob sich der Xbox 360 Controller für Windows gemäß den akzeptierten Standards verhält.

4.  Legen Sie das Video auf \[ 1.5 \] fest:

    1.  Überprüfen Sie, ob das Spiel mit einer Seitenverhältnisauflösung von 4:3 (800 600 oder 1024 768) ausgeführt wird.
    2.  Überprüfen Sie, ob das Spiel mit einer Seitenverhältnisauflösung von 16:9 (1280 720) ausgeführt wird.
    3.  Überprüfen Sie, ob das Spiel mit einer Seitenverhältnisauflösung von 16:10 (1680 1050, 800 480 oder 1152 720) ausgeführt wird.
    4.  Vergewissern Sie sich, dass das Spiel den Benutzer auffordert, wenn eine Änderung an der Auflösung vorgenommen wird.
    5.  Stellen Sie sicher, dass die Anzeige auf die vorherige Einstellung zurückgesetzt wird, wenn Sie nicht innerhalb von 15 Sekunden akzeptieren.
    6.  Stellen Sie sicher, dass das Spiel das Bild nicht gestreckt und wiederum einen breiteren Ansichtsbereich darstellt.
    7.  Vergewissern Sie sich, dass das Spiel links und rechts vom Spielbereich keine schwarzen Balken hinzufüge.

5.  Falls in den Videoeinstellungen verfügbar, überprüfen Sie, ob die Spielrenderoptionen standardmäßig Direct3D \[ 1.7 \] verwenden. Fahren Sie andernfalls mit [automatisierten Tests](#58-automated-tests) fort.
6.  Wenn Sie dazu aufgefordert werden oder die Option verfügbar ist, erstellen Sie ein Benutzerprofil. Vergewissern Sie sich, dass beim Spiel keine Fehler auftreten, wenn lange Dateinamen \[ 2.7 verwendet werden.\]
7.  Starten Sie ein neues Spiel, erstellen Sie ein Spiel, und überprüfen Sie, ob beim Behandeln von nicht unterstützten Dateisystemzeichen 2.7 keine Fehler auftreten. \[\]
8.  Vergewissern Sie sich, dass das Spiel ordnungsgemäß ALT+TABs für Windows Desktop \[ 2.6 verwendet.\]

    1.  Wechseln Sie die Benutzer mit dem ausgeführten Spiel, indem Sie auf Start -> Switch User (Benutzer wechseln) klicken.
    2.  Anmelden als Toby
    3.  Vergewissern Sie sich, dass das Spiel als User Toby gestartet wird, während es weiterhin als Benutzerin Jane \[ 2.6 ausgeführt wird.\]
    4.  Vergewissern Sie sich, dass beim Benutzerwechselprozess 2.6 keine Fehler für "User Toby" oder "User Jane" \[ auftreten.\]
    5.  Vergewissern Sie sich, dass Sie keine Audiodaten aus der ursprünglichen Spielsitzung \[ 2.6 hören können.\]
    6.  Beenden des Spiels
    7.  Abmelden von Toby
    8.  Wechseln Sie zurück zum ursprünglichen Benutzer, auf dem das Spiel ausgeführt wird.
    9.  ALT+TAB zurück ins Spiel

9.  Beenden des Spiels
10. Fahren Sie mit [Post-Runtime](#56-post-runtime) fort.

### <a name="56-post-runtime"></a>5.6 Nach der Laufzeit

1.  Vergewissern Sie sich, dass das Spiel keine Fehler beim Beenden \[ von 4.3 generiert.\]
2.  Überprüfen Sie, ob das Spiel in Program Files \[ 3.3 installiert ist.\]
3.  Fahren Sie mit [Jugendschutz fort.](/windows)

### <a name="57-parental-controls"></a>5.7 Jugendschutz

1.  Öffnen der Jugendschutzfunktionen in Systemsteuerung
2.  Vergewissern Sie sich, dass das Spiel unter dem Spieltitel in Der Jugendschutz Systemsteuerung 1.2 eine genaue Bewertung der Jugendschutzprüfung anzeigt. \[\]
3.  Die folgenden Tests finden Sie unter Testfall \[ 1.2: \]

    1.  Nachdem Sie Die Jugendschutz auf "Ein" festgelegt haben, überprüfen Sie, ob das Spiel mit diesen Einstellungen als Benutzerin Jane \[ 1.2 ausgeführt wird.\]
    2.  Melden Sie sich ab, und melden Sie sich als Toby an.
    3.  Überprüfen Sie, ob das Spiel mit diesen Einstellungen als User Toby \[ 1.2 ausgeführt wird.\]
    4.  Melden Sie sich ab, und melden Sie sich als Jane an.
    5.  Blockieren Sie im Abschnitt Jugendschutz, dass Benutzer Toby keine Spiele mehr oder höher als das soeben installierte Spiel mit einer ESRB-Ebene sehen kann.

        Beispiel: Wenn das Spiel mit E bewertet wird, legen Sie es so fest, dass Toby nur Spiele mit der Bewertung "C" spielen kann.

    6.  Vergewissern Sie sich, dass das Spiel mit diesen Einstellungen als Benutzerin Jane \[ 1.2 ausgeführt wird.\]
    7.  Melden Sie sich ab, und melden Sie sich als Benutzer toby an.
    8.  Vergewissern Sie sich, dass das Spiel nicht auf User Toby gestartet wird, wenn ESRB von Benutzerin Jane \[ 1.2 blockiert wird.\]
    9.  Melden Sie sich als Benutzer Toby an, und melden Sie sich wieder als Benutzerin Jane an.
    10. Wenn sie zuvor geändert wurden, stellen Sie die ESRB-Einstellungen wieder her.
    11. Wenn keine ESRB-Einstellungen vorhanden sind, wählen Sie "Bestimmte Spiele blockieren oder zulassen" aus, und wählen Sie das Spiel anhand des Namens aus.
    12. Melden Sie sich als Jane und als Toby an.
    13. Vergewissern Sie sich, dass das Spiel nicht auf User Toby gestartet wird, wenn EXE/Name von Benutzerin Jane \[ 1.2 blockiert wird.\]
    14. Melden Sie sich als Toby und wieder als Jane an.
    15. Öffnen Sie als Jane Benutzersteuerelemente -> Anwendungseinschränkungen.
    16. Klicken Sie auf "Toby kann nur die Programme verwenden, die ich zulässt", und klicken Sie dann auf OK (d.h. keine Exe-Dateien zulassen).
    17. Klicken Sie auf das Kontrollkästchen Alle deaktivieren und dann auf OK.
    18. Wechseln Sie zu Benutzersteuerelemente \| Spielesteuerelemente, und lassen Sie das jeweilige Spiel mit der ESRB-Bewertung zu.
    19. Melden Sie sich als Jane an, melden Sie sich als Toby an, und versuchen Sie, das Spiel zu spielen.
    20. Stellen Sie sicher, dass das Spiel NICHT blockiert ist und dass Toby es spielen kann, wenn "Keine Exes zulassen" \[ auf 1.2 festgelegt ist.\]
    21. Melden Sie sich als Benutzer Toby an, und melden Sie sich wieder als Benutzerin Jane an.
    22. Wechseln Sie in Systemsteuerung zu Jugendschutz, und entfernen Sie die Einschränkungen.
    23. Vergewissern Sie sich, dass beide Benutzer jetzt das Spiel spielen können.

4.  Fahren Sie mit [automatisierten Tests](#58-automated-tests) fort.

### <a name="58-automated-tests"></a>5.8 Automatisierte Tests

1.  Überprüfen Sie, ob das Spiel keine Fehler generiert, wenn es unter Application Verifier ausgeführt wird. Weitere Informationen finden Sie in der Dokumentation zum Brandingtesttool \[ 4.2.\]
2.  Überprüfen Sie, ob die ausführbaren Dateien des Spiels Manifeste enthalten. Weitere Informationen finden Sie unter Branding Test Tool Documentation 2.1 (Dokumentation zum Brandingtesttool \[ 2.1).\]
3.  Vergewissern Sie sich, dass das ausführbare Dateimanifest für das Spiel "RequestedExecutionLevel" "AsInvoker" lautet. Weitere Informationen finden Sie in der Dokumentation zum Brandingtesttool \[ 2.1.\]
4.  Fahren Sie mit [anderen Tests](#59-other-tests) fort.

### <a name="59-other-tests"></a>5.9 Weitere Tests

1.  Überprüfen Sie, ob die ausführbaren Dateien des Spiels eine digitale Signatur \[ 2.3 enthalten.\]
2.  Überprüfen Sie, ob der Spielinstallationsvorgang normal in 64-Bit-Editionen von Windows Vista und/oder Windows 7 \[ 2.3 ausgeführt wird.\]
3.  Vergewissern Sie sich, dass beim Spiel kein Fehler aufgrund von ausführbaren 16-Bit-Dateien in 64-Bit-Editionen von Windows Vista und/oder Windows 7 \[ 2.3 auftritt.\]
4.  Erzwingen des Absturzes der Anwendung beim Testen, überprüfen Sie, ob das Spiel Windows-Fehlerberichterstattung ordnungsgemäß anzeigt und Absturzdaten \[ 4.3 sammelt.\]
5.  Sicherstellen der richtigen Dateizusammenfassungen \[ 4.3\]

    1.  Klicken Sie auf Start -> Computer.
    2.  Navigieren Sie zum Spielverzeichnis.
    3.  Geben Sie im Suchfenster \*.dll
    4.  Für jede Datei: Klicken Sie mit der rechten Maustaste auf die Datei, und klicken Sie auf Eigenschaften.

        -   In Windows XP: Klicken Sie auf die Registerkarte Version. Stellen Sie sicher, dass die Felder Produktname, Unternehmensname und Dateiversion ordnungsgemäß aufgefüllt sind. \[4.3\]
        -   Unter Windows Vista und Windows 7: Klicken Sie auf die Registerkarte Details. Vergewissern Sie sich, dass die Felder Produktname und Dateiversion ordnungsgemäß ausgefüllt sind. Der Unternehmensname ist auf der Eigenschaftenseite 4.3 von Windows Vista oder Windows 7 nicht sichtbar. \[\]

    5.  Wiederholen Sie diese Überprüfung für .exe Dateien.

6.  Starten Sie das Spiel.

    1.  Drücken Sie STRG+ALT+ENTF.
    2.  Klicken Sie auf den Pfeil "Optionen zum Herunterfahren".
    3.  Klicken Sie auf Neu starten.
    4.  Vergewissern Sie sich, dass das Herunterfahren 3.1 durch das Spiel nicht blockiert \[ wird.\]

7.  Fahren Sie mit [der Deinstallation fort.](#510-uninstall)

### <a name="510-uninstall"></a>5.10 Deinstallieren

-   Stellen Sie sicher, dass beim Deinstallationsprozess des Spiels alle installierten, nicht neu verteilten Betriebssystemkomponentendateien entfernt werden und alle Einstellungen \[ 3.1 gelöscht werden.\]

    -   Vergewissern Sie sich in Windows Vista oder Windows 7, dass Systemsteuerung die einzige Möglichkeit ist, das Programm \[ 1.1 zu entfernen.\]

## <a name="test-tool-notes"></a>Testtoolhinweise

Dies sind Hinweise für jedes der Testtools, die in den obigen Testanforderungen aufgeführt sind.

### <a name="61-appverifier-40-or-higher"></a>6.1 Appverifier 4.0 (oder höher)

**Testfall: 2.5, 4.2**

> [!Note]  
> Einige Anwendungen können aufgrund des Kopierschutzes nicht mit AppVerifier ausgeführt werden. Dies kann durch Ausführen einer nicht geschützten Releaseversion der ausführbaren Spieldatei behoben werden.

 

1.  Installieren von AppVerifier 4.0 (oder höher) auf einem Computer mit Windows XP
2.  Starten Sie AppVerifier, und klicken Sie auf Datei -> Anwendung hinzufügen.
3.  Suchen Sie die ausführbare Spieldatei, wählen Sie sie aus, und klicken Sie auf Öffnen.
4.  Wählen Sie im Abschnitt "Anwendungen" die ausführbare Spieldatei aus.
5.  Wählen Sie im Abschnitt "Grundlagen" die folgenden Tests aus:

    -   Ziehpunkte
    -   Heaps
    -   Locks
    -   Arbeitsspeicher
    -   TLS

6.  Wählen Sie im Abschnitt "Sonstiges" die folgenden Tests aus:

    -   DangerousAPIs
    -   DirtyStacks

7.  Sicherstellen, dass nicht alle anderen Tests ausgewählt sind
8.  Starten des Spiels
9.  Spielen Sie das Spiel.
10. Schließen des Spiels
11. Wählen Sie in AppVerifier die Option -> Protokolle anzeigen aus.
12. Wählen Sie im Abschnitt "Anwendungen" die App-.exe datei aus.
13. Wählen Sie im Abschnitt "Protokolle" die Protokolldatei aus, und beobachten Sie die Fehleranzahl. Wenn keine Fehler auftreten, beenden Sie AppVerifier-Tests. Wenn Fehler auftreten, klicken Sie auf die Schaltfläche Ansicht.
14. Durchsuchen Sie das Dokument (STRG+F) nach Severity="Error
15. Erstellen von Fehlern basierend auf dem LayerName=-Teil des Fehlers

### <a name="62-manifest-test---mtexe"></a>6.2 Manifesttest – mt.exe

**Testfall: 1.8, 2.1**

Dieses Tool wird über eine Eingabeaufforderung ausgeführt, in der sich MT.exe befindet.

Beispiel:

``` syntax
mt.exe -inputresource:"c:\yourdir\YourGame.exe";#1 -out:yourgame.manifest
```

1.  Klicken Sie auf Start -> Run -> geben Sie cmd ein, und klicken Sie auf die Schaltfläche OK.
2.  Führen Sie das mt.exe Tool aus, um eine MANIFEST-Datei für jede .exe-Datei zu generieren, die mit dem Spiel installiert wird.
3.  Öffnen der generierten MANIFEST-Datei
4.  Stellen Sie sicher, dass jede .exe Datei Folgendes enthält (angefordert:

    ``` syntax
    <description>Example Game Name</description>
    <trustInfo xmlns="urn:schemas-microsoft-com:asm.v2">
      <security>
        <requestedPrivileges>
          <requestedExecutionLevel level="asInvoker"></requestedExecutionLevel>
        </requestedPrivileges>
      </security>
    </trustInfo>
      <asmv3:windowsSettings xmlns=http://schemas.microsoft.com/SMI/2005/WindowsSettings>
        <dpiAware>true<dpiAware>
      </asmv3:windowsSettings>
    </asmv3:application>
    ```

> [!Note]  
> Die angeforderte Ausführungsebene sollte für jede Datei vorhanden sein, und dpiAware sollte mindestens für die ausführbare Datei des Spiels vorhanden sein.

 

### <a name="63-thread-hijacker---threadhijackerexe"></a>6.3 Thread- und threadhijacker.exe

Dieses Tool wird über eine Eingabeaufforderung ausgeführt, in der sich threadhijacker.exe befindet.

Beispiel:

``` syntax
threadhijacker.exe /process:str
```

Dabei ist str der Name \_ der \_program.exe

1.  Öffnen Sie Task-Manager, klicken Sie auf die Registerkarte Prozesse, und suchen Sie den Namen der ausführbaren Spieldatei.
2.  Öffnen einer Eingabeaufforderung im Administratormodus
3.  Navigieren Sie zu dem Verzeichnis, in dem sich threadhijacker.exe befindet.
4.  Typ: **threadhijacker.exe /process:** str, wobei str der Name der ausführbaren Datei ist, die Sie erreichen möchten.

### <a name="64-microsoft-games-for-windows-test-tool"></a>6.4 Microsoft Games for Windows Test Tool

Dieses Tool befindet sich im DirectX SDK. Sobald das SDK auf einem Computer installiert ist, kann das Installationsprogramm für das Games for Windows Test Tool auf dem Testcomputer platziert und installiert werden.

Suchen Sie den Installer für das Microsoft Games for Windows Test Tool auf dem Entwicklungscomputer, auf dem das DirectX SDK installiert ist. Standardmäßig wird sie an folgendem Speicherort platziert:

``` syntax
%SystemDrive%\Program Files (x86)\Microsoft DirectX SDK (Date)\Utilities\bin\x86\Microsoft Games for Windows Test Tools\
```

1.  Kopieren Sie das Installationsprogramm (MicrosoftGFWTestTool.msi/setup.exe) auf den Testcomputer.
2.  Führen Sie das Installationsprogramm aus.
3.  Starten Sie das Testtool Microsoft Games for Windows.
4.  Ersetzen Sie im Feld **Projektliste** das Feld **Neues Projekt erstellen** durch Ihren Titelnamen, und klicken Sie auf Neu **erstellen.**

    Warten Sie, bis die Baseline abgeschlossen ist.

5.  Geben Sie alle Informationen ein, die Sie möglicherweise im Abschnitt **Spielinformationen** haben, und klicken Sie auf **Spielinformationen aktualisieren.**
6.  Klicken Sie auf die Registerkarte **Testfälle.**
7.  Beginnen Sie oben mit den Testfällen, und klicken Sie je nach Bedarf auf **Erfolgreich** oder **Fehler.**

    Weitere Informationen zum Einschließen eines Fehlers in den Bericht finden Sie weiter unten in diesem Abschnitt unter "Schreiben eines Fehlers".

8.  Kehren Sie zur Registerkarte **Projekte** zurück, nachdem Sie den Bericht überprüft haben (durch Überprüfen der Registerkarten **Bericht** und **Fehlerbearbeitung).**
9.  Klicken Sie auf **Bericht kompilieren.**

    Wenn die Kompilierung des Berichts abgeschlossen ist, wird ein Fenster geöffnet. Hier finden Sie einen .ZIP Dateinamen *ProjectName* \_report.zip. Diese Datei enthält alle Protokolle und Ergebnisse, die während des Testdurchlaufs gesammelt wurden.

### <a name="writing-a-bug"></a>Schreiben eines Fehlers

Es gibt zwei Möglichkeiten, einen Fehlerbericht zu schreiben: Sie können die Testfälle durchlaufen und auf **Fehler** klicken, wenn der Titel bei einem Testfall fehlschlägt, oder Sie können auf die Registerkarte **Fehlerbearbeitung** klicken und manuell einen Fehlerbericht hinzufügen.

### <a name="clicking-fail-on-a-test-case"></a>Klicken auf Fehler bei einem Testfall

1.  Wenn Sie bei einem Testfall auf **Fehler** klicken, wird die Dropdownliste **Problemtyp** automatisch auf den Testfalltyp festgelegt.
2.  Fügen Sie dem Feld **Titel** eine kurze Beschreibung hinzu, in der das Problem kurz beschrieben wird.
3.  Fügen Sie dem Feld **Beobachtetes Verhalten** eine ausführliche Beschreibung des Problems hinzu.
4.  Fügen Sie ggf. das erwartete Verhalten (im Gegensatz zu einer Beschreibung des Problems) zum Feld **Erwartetes Verhalten** hinzu.
5.  Fügen Sie dem Feld **Reproduktionsschritte** eine ausführliche Beschreibung der Reproduktion des Problems hinzu.
6.  Klicken Sie anschließend auf die Schaltfläche **Speichern.**

### <a name="manually-adding-a-bug"></a>Manuelles Hinzufügen eines Fehlers

Dieser Vorgang entspricht dem Klicken auf **Fehler**, mit Ausnahme der automatisch aufgefüllten Dropdownliste. Wählen Sie in diesem Fall entweder den entsprechenden TCR-Fehlertyp aus, oder wählen Sie **\* \* Nicht-TR-Problem \* \*** für Fehler aus, die außerhalb des TR-Bereichs liegen, aber trotzdem gemeldet werden sollten.

## <a name="resources"></a>Ressourcen

<dl> <dt>

<span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Spiele für Windows: Technische Anforderungen
</dt> <dd>

[Technische Anforderungen für Spiele für Windows: Bewährte Methoden für Spiele unter Windows XP, Windows Vista und Windows 7](./games-for-windows-technical-requirements-1-1-0006.md)

</dd> <dt>

<span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK
</dt> <dd>

[Windows SDKs](https://msdn.microsoft.com/bb980924.aspx)

</dd> <dt>

<span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>Richtlinien für die Benutzerkontensteuerung
</dt> <dd>

[Anforderungen an die Windows Vista-Anwendungsentwicklung für die Kompatibilität der Benutzerkontensteuerung](/previous-versions/dotnet/articles/bb530410(v=msdn.10))

</dd> <dt>

<span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Installer Informationen
</dt> <dd>

[Windows Installer](../msi/windows-installer-portal.md)

</dd> <dt>

<span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual Entwicklerportal 
</dt> <dd>

[Windows Quality Online Services (Winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

</dd> <dt>

<span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX Entwicklerportal
</dt> <dd>

[DirectX Developer Center](/previous-versions/windows/apps/hh452744(v=win.10))

</dd> <dt>

<span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Games for Windows and DirectX SDK Blog
</dt> <dd>

[Spiele für Windows und das DirectX SDK](https://walbourn.github.io/)

</dd> <dt>

<span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Zusätzliche DirectX-Artikel
</dt> <dd>

[Technische Artikel zu DirectX](./dx9-technical-articles.md)

</dd> </dl>

 

