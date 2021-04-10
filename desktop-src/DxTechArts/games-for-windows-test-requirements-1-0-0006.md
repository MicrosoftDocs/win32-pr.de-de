---
title: Testfälle für Spiele für Windows; bewährte Methoden für Spiele für Windows XP, Windows Vista, Windows 7 und Windows 8
description: Dieser Artikel enthält Testfälle für Spiele für Windows.
ms.assetid: bbe84d3f-e7ff-f14f-ec25-ae1c980749fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae26274f199f070ce605227fa19796716df9fbaf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039314"
---
# <a name="games-for-windows-test-cases-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a>Spiele für Windows-Testfälle: bewährte Methoden für Spiele unter Windows XP, Windows Vista, Windows 7 und Windows 8

Dieser Artikel enthält Testfälle für Spiele für Windows.

## <a name="how-to-use-this-article"></a>Zur Verwendung dieses Artikels

Es gibt drei Hauptabschnitte zu diesem Artikel:

<dl> <dt>

<span id="Test_Requirements"></span><span id="test_requirements"></span><span id="TEST_REQUIREMENTS"></span>**Test Anforderungen**
</dt> <dd>

Jede Test Anforderung in diesem Dokument umfasst vier Hauptabschnitte: einen Titel und eine Tabelle mit drei wichtigen Abschnitten (linke Spalte, rechts oben, rechts unten).

<dl> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Tel
</dt> <dd>

Der Name des Testfalls.

</dd> <dt>

<span id="Box__far_left_column"></span><span id="box__far_left_column"></span><span id="BOX__FAR_LEFT_COLUMN"></span>Box, Spalte ganz links
</dt> <dd>

Die Namen der Betriebssysteme, auf die der Testfall angewendet wird.

</dd> <dt>

<span id="Box__right_top"></span><span id="box__right_top"></span><span id="BOX__RIGHT_TOP"></span>Box, rechts oben
</dt> <dd>

Kurze Zusammenfassung des Testfalls.

</dd> <dt>

<span id="Box__right_bottom"></span><span id="box__right_bottom"></span><span id="BOX__RIGHT_BOTTOM"></span>Box, rechts unten
</dt> <dd>

Details zum eigentlichen Testfall.

</dd> </dl> </dd> <dt>

<span id="Sample_Test_Script"></span><span id="sample_test_script"></span><span id="SAMPLE_TEST_SCRIPT"></span>**Beispiel für ein Test Skript**
</dt> <dd>

Dieser Abschnitt ist ein Beispiel für die Sequenz, die bei der Verwendung der Testanforderungen als Leitfaden für einen typischen Test Durchlauf befolgt wird.

</dd> <dt>

<span id="Test_Tool_Notes"></span><span id="test_tool_notes"></span><span id="TEST_TOOL_NOTES"></span>**Anmerkungen zum Testtool**
</dt> <dd>

Dieser Abschnitt enthält ausführliche Hinweise zu den einzelnen Test Tools, die zur Überprüfung der Erfolgs-oder Fehlerbedingungen in den Testanforderungen verwendet werden.

</dd> </dl>

## <a name="test-requirements"></a>Test Anforderungen

### <a name="1-game-requirements"></a>1. Spiel Anforderungen

### <a name="11-windows-games-explorer"></a>1,1 Windows Games Explorer



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Das Spiel muss im Spiele-Explorer unter Windows Vista und Windows 7 sichtbar sein. Wenn diese Option ausgewählt ist, muss das Spiel auch korrekte Metadaten anzeigen. Bei der Installation darf keine Verknüpfung erstellt werden, um das Spiel auf dem Desktop, im Startmenü oder an einem anderen Speicherort zu starten. Aufgaben und Verknüpfungen zum Entfernen dürfen nicht erstellt werden.</td>
</tr>
<tr class="even">

<td><ol>
<li>Nachdem Sie das Spiel installiert haben, öffnen Sie Games Explorer.</li>
<li>Stellen Sie sicher, dass das Symbol "Spiel" in Games Explorer angezeigt wird</li>
<li>Klicken Sie mit der rechten Maustaste auf das Symbol, und testen Sie jede Anwendungs definierte Wiedergabe & Unterstützungs Aufgabe.</li>
<li>Klicken Sie auf das Symbol, und überprüfen Sie, ob die Metadaten (Verleger, Entwickler, Genre, Veröffentlichungsdatum, Version) unten angezeigt werden und korrekt sind.</li>
<li>Stellen Sie sicher, dass das Symbol "Spiel" Informationen zu Windows-Erfahrungs Index (Wei) in Games Explorer anzeigt.</li>
<li>Überprüfen Sie, ob die Spiel Hyperlinks für Metadaten im Spiele-Explorer ordnungsgemäß funktionieren. (Wenn Hyperlinks nicht angezeigt werden, ist dies ein mögliches Vorzeichen, dass die exe-Seite nicht signiert ist. Weitere Informationen finden Sie im <a href="#23-sign-files">Abschnitt 2,3</a>.)</li>
<li>Stellen Sie sicher, dass das Spiel in Games Explorer eine genaue Bewertung der Jugend Teuerung anzeigt. (Wenn er als nicht bewertet eingestuft wird, überprüfen Sie, ob es sich um ein nicht bewertetes Spiel handelt; andernfalls handelt es sich hierbei um einen Indikator, dass die exe-Datei nicht signiert ist. siehe <a href="#23-sign-files">Abschnitt 2,3</a></li>
<li>Vergewissern Sie sich, dass das Spiel keine Start Verknüpfungen auf dem Benutzer Desktop platziert.</li>
<li>Klicken Sie auf Start-> alle Programme.</li>
<li>Vergewissern Sie sich, dass das Spiel keine Start Verknüpfungen im Startmenü platziert.</li>
<li>Vergewissern Sie sich, dass das Spiel keine Deinstallations Verknüpfungen im Startmenü außerhalb der Systemsteuerung platziert.</li>
<li>Wenn das Spiel Digital verteilt ist, überprüfen Sie, ob der Dienstanbieter in Windows Games Explorer angezeigt wird.</li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="12-windows-family-safety--parental-controls"></a>1,2 Windows-Familien Sicherheit/Eltern Steuerelemente



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Das Spiel muss im Kontext eines &quot; Standard Benutzers ausgeführt werden &quot; . Eltern Steuerelemente müssen in der Lage sein, das Spiel zu blockieren. Vergewissern Sie sich, dass die GDF über exe-Namen verfügt.</td>
</tr>
<tr class="even">

<td><ol>
<li>Erstellen Sie ein Standard Benutzerkonto in Windows Vista oder Windows 7 namens Toby. Start->-Systemsteuerung-> Benutzerkonten hinzufügen oder entfernen-> neues Konto erstellen</li>
<li>Als Andrea haben Sie aus dem Administrator Konto Eltern Steuerelemente für das Spiel eingerichtet. Start->-Systemsteuerung-> richten Sie die Jugendschutz Steuerelemente für alle Benutzer >
<ol>
<li>Überprüfen Sie, ob das Spiel über das Symbol für Spiele-Explorer gestartet wird</li>
<li>Vergewissern Sie sich, dass das Spiel unter dem Spieltitel in der Systemsteuerung für Eltern Steuerelemente eine genaue Bewertung des Eltern Steuer Elements anzeigt.</li>
<li>Vergewissern Sie sich vor dem Anwenden der Jugend Steuerungsmechanismen, dass das Spiel beim Start keine Administrator Anmelde Informationen auffordert.</li>
<li>Legen Sie Eltern Steuerelemente auf ein fest &quot; &quot; .</li>
<li>Klicken Sie im Abschnitt Windows-Einstellungen auf Games.</li>
<li>Klicken Sie auf OK (die Einstellung sollte jetzt &quot; Ao/alle Spiele lauten &quot; ).</li>
<li>Stellen Sie sicher, dass das Spiel mit diesen Einstellungen ausgeführt wird, wie User Jane.</li>
<li>Melden Sie sich als Andrea ab, und melden Sie sich als Toby an.</li>
<li>Stellen Sie sicher, dass das Spiel mit diesen Einstellungen als Benutzer-zu-Ende ausgeführt wird.</li>
<li>Melden Sie sich als Toby ab, und melden Sie sich als Jane an.</li>
<li>Kehren Sie zum vorherigen Bildschirm zurück, und wählen Sie &quot; Spiel Bewertungen festlegen aus &quot; .</li>
<li><p>Wählen Sie eine Bewertung aus, die niedriger als die ESRB-Bewertung des Spiels ist.</p>
<blockquote>
[!Note]<br />
Wenn das Spiel nicht bewertet wird, überspringen Sie diesen Schritt, und fahren Sie mit dem nächsten Teil dieses Tests fort. Es kann erforderlich sein, ein anderes Bewertungssystem auszuwählen, um eine Spiel Bewertung zu finden. Dies hängt vom Gebiets Schema der zu testenden SKU ab.
</blockquote>
<p><br/></p></li>
<li>Melden Sie sich als Andrea ab, und melden Sie sich als Toby an.</li>
<li>Stellen Sie sicher, dass das Spiel für den Benutzer "um" nicht gestartet wird, wenn ESRB von Benutzer Jane blockiert wird.</li>
<li>Melden Sie sich als Toby ab, und melden Sie sich als Jane an.</li>
<li>Wenn Sie zuvor geändert haben, stellen Sie die ESRB-Einstellungen wieder her</li>
<li>Wenn keine ESRB-Einstellungen vorhanden sind, wählen Sie &quot; bestimmte Spiele blockieren oder zulassen &quot; aus, und wählen Sie das Spiel nach Name aus.</li>
<li>Melden Sie sich als Andrea ab, und melden Sie sich als Toby an.</li>
<li>Stellen Sie sicher, dass das Spiel für den Benutzer "" nicht gestartet wird, wenn "exe/Name" von Benutzer Jane blockiert wird.</li>
<li>Melden Sie sich als "Toby" und "zurück" als Andrea ab.</li>
<li>Öffnen Sie als Andrea die Benutzer Steuerelemente > Anwendungs Einschränkungen.</li>
<li>Klicken Sie auf "durch Klicken" &quot; können Sie nur die Programme verwenden, die ich zulässt &quot; , und klicken Sie auf "OK" (keine exe-Datei zulassen)</li>
<li>Gehe zu Benutzer Steuerelementen | Games steuert und ermöglicht das jeweilige Spiel, das die ESRB-Bewertung verwendet.</li>
<li>Melden Sie sich als Andrea ab, und melden Sie sich als Toby an, und versuchen Sie, das Spiel zu spielen.</li>
<li>Stellen Sie sicher, dass das Spiel nicht blockiert ist und dass es von "tby" wiedergegeben werden kann, wenn " &quot; keine exe-Datei zulassen &quot;</li>
</ol></li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="13-windows-vista-rich-saved-games"></a>1,3 in Windows Vista umfassende gespeicherte Spiele

Diese Anforderung wurde zurückgezogen.

### <a name="14-xbox-360-common-controller-for-windows-conditional-requirement"></a>1,4 Xbox 360 allgemeiner Controller für Windows \[ bedingte Anforderung\]



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Spiele, die Gamepad-Controller unterstützen, müssen den Xbox 360-Controller für Windows mithilfe der xinput-API unterstützen. Alle Verweise auf allgemeine Controller Trigger und-Schaltflächen müssen die Xbox 360-Namen verwenden.</td>
</tr>
<tr class="even">

<td><ol>
<li>Starten Sie das Spiel.</li>
<li>Wechseln Sie zu den Controller Optionen. **</li>
<li>Vergewissern Sie sich, dass das Spiel Xbox 360-Controller für Windows als Eingabegerät erkennt.</li>
<li>Spielen Sie das Spiel, und überprüfen Sie, ob das Spiel und das Menüsystem mit Xbox 360 Controller für Windows steuerbar sind.</li>
<li>Vergewissern Sie sich, dass sich der Xbox 360-Controller für Windows gemäß den akzeptierten Standards verhält. (B für "zurück", "A" für "Accept", "Start" im Menü "Spiel", "anhalten", "annehmen</li>
<li>Stellen Sie sicher, dass sich das Spiel auf die Controller Schaltflächen und Trigger mit Xbox 360-Namen bezieht.</li>
</ol>
<br/>
<blockquote>
[!Note]<br />
Wenn das Spiel keinen Spiele Controller unterstützt und/oder nur Tastatur/Maus unterstützt, überspringen Sie diesen Testfall.
</blockquote>
<br/> * * Einstellungen für den Controller befinden sich möglicherweise außerhalb des Spiels. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="15-multiple-aspect-ratios-and-resolutions"></a>1,5 mehrere Seitenverhältnisse und Auflösungen



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Das Spiel muss mindestens die folgenden Seitenverhältnisse und zugeordneten Bildschirmauflösungen unterstützen: <br/>
<ul>
<li>4:3 &quot; Normal &quot; (800 600 oder 1024 768)</li>
<li>16:9- &quot; Breitbild &quot; (1280 720)</li>
<li>16:10- &quot; Breitbild &quot; (1152 720, 1680 1050 oder 800 480)</li>
</ul></td>
</tr>
<tr class="even">

<td>Suchen Sie die Video Optionen für das Spiel (diese sind möglicherweise im Spiel).<br/>
<blockquote>
[!Note]<br />
Die folgenden Tests müssen auf einem Breitbild Schirm ausgeführt werden.
</blockquote>
<br/>
<ol>
<li>Wählen Sie im Abschnitt Videoauflösung die Option 800 600 oder 1024 768 aus.</li>
<li>Überprüfen Sie, ob das Spiel bei einer 4:3-Seitenverhältnis Auflösung ausgeführt wird.</li>
<li>Wählen Sie im Abschnitt Videoauflösung die Option 1280 720 aus.</li>
<li>Überprüfen Sie, ob das Spiel bei einer 16:9-Seitenverhältnis Auflösung ausgeführt wird.</li>
<li>Wählen Sie im Abschnitt Videoauflösung die Option 1680 1050, 800 480 oder 1152 720 aus.</li>
<li>Überprüfen Sie, ob das Spiel bei einer 16:10-Seitenverhältnis Auflösung ausgeführt wird.</li>
<li>Stellen Sie sicher, dass das Spiel das Bild nicht Strecken und wiederum einen breiteren Bereich der Ansicht darstellt.</li>
<li>Überprüfen Sie, ob das Spiel den Benutzer auffordert, wenn eine Änderung an der Auflösung vorgenommen wird.</li>
<li>Wenn der Benutzer nicht innerhalb von 15 Sekunden akzeptiert, vergewissern Sie sich, dass die Anzeige auf die vorherige Einstellung zurückgesetzt wird.</li>
<li>Vergewissern Sie sich, dass das Spiel keine schwarzen Balken Links und rechts im Spielbereich des Spiels hinzufügt. (In diesem Fall wird der Spielbereich in einem 4:3-Verhältnis in der Mitte des Bildschirms angezeigt.)</li>
</ol>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="16-windows-media-center"></a>1,6 Windows Media Center

Diese Anforderung wurde zurückgezogen.

### <a name="17-direct3d-conditional-requirement"></a>1,7 Direct3D \[ bedingte Anforderung\]



|                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows 7<br/> Windows Vista<br/> Windows XP<br/> | Wenn das Spiel Direct3D verwendet, muss die mindestens unterstützte Version Direct3D 9 sein, und Direct3D muss der Standardwert für jede Anzeige Konfigurationsoption sein.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|                                                                     | <dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuell</dt> <dd> Starten Sie das Spiel. Überprüfen Sie in den Videooptionen, ob die Optionen "Rendering", "D3D" und "OpenGL" vorhanden sind. Wenn dies der Fall ist, überprüfen Sie, ob die spielend-Optionen standardmäßig auf Direct3D Wenn Sie nicht überprüfen können, ob d3d9 die verwendete Version von DirectX ist, fahren Sie mit dem automatisierten Test fort. <br/> </dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automatisierter Test</dt> <dd> Tool verwenden: Depends.exe <br/> </dd> </dl> |



 

### <a name="18-enable-high-dpi-aware"></a>1,8 Aktivieren von High-dpi-Werten



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Spiele und deren Installer müssen ohne visuelle Probleme ordnungsgemäß ausgeführt werden, wenn die DPI-Skalierung aktiviert ist.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuell</dt> <dd>
<ol>
<li>Legen Sie das System auf dpi 150% fest: <br/> Windows Vista: Systemsteuerung: Personalisierung, Schriftart anpassen (dpi), benutzerdefinierter dpi-Code. Auf 150% festgelegt.<br/> Windows 7: Systemsteuerung: Anzeige, Festlegung auf größer-150%.<br/></li>
<li>Führen Sie den Installationsprozess und das Spiel aus, um sicherzustellen, dass keine Probleme mit ausgeschnittenen Bildschirmen oder Dialogfeldern vorliegen.</li>
</ol>
</dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automatisierter Test</dt> <dd> Vergewissern Sie sich, dass das Element <dpiAware>true</dpiAware> im eingebetteten Manifest enthalten ist.<br/> Tool verwenden: Mt.exe <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="2-security-and-compatibility"></a>2. Sicherheit und Kompatibilität

### <a name="21-follow-user-account-control-guidelines"></a>2,1 befolgen Sie die Richtlinien zur Benutzerkontensteuerung



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Jede ausführbare Datei (. EXE-Erweiterung), die in einer Anwendung enthalten ist, muss ein eingebettetes Manifest aufweisen, das die Ausführungs Ebene definiert:
<pre class="syntax" data-space="preserve"><code><requestedExecutionLevel level=&quot;asInvoker|highestAvailable|requireAdministrator&quot; 
              uiAccess=&quot;true|false&quot;/></code></pre>
<br/>
<blockquote>
[!Note]<br />
Für Spiele und Spiel Installationsprogramme sollte UIAccess immer auf false festgelegt werden &quot; &quot; .
</blockquote>
<br/></td>
</tr>
<tr class="even">

<td><ol>
<li>Überprüfen, ob ausführbare Spieldateien Manifeste enthalten.</li>
<li>Überprüfen der ausführbaren Datei des ausführbaren Datei Manifests requestedExecutionLevel ist &quot; asInvoker &quot; .</li>
</ol>
Tool verwenden: Mt.exe <br/></td>
</tr>
</tbody>
</table>



 

### <a name="22-support-x64-versions-of-windows"></a>2,2 Unterstützung von x64-Versionen von Windows



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>So gewährleisten Sie die Kompatibilität mit x64-Versionen von Windows: <br/>
<ul>
<li>Titel und Titel-Installer dürfen keinen 16-Bit-Code enthalten oder auf eine 16-Bit-Komponente zurückgreifen.</li>
<li>Wenn das Spiel von Kernelmodustreibern für den Betrieb abhängt, müssen x64-Versionen dieser Treiber verfügbar sein. Die Spiel Einrichtung muss die richtigen Treiber und Komponenten für die 64-Bit-Editionen von Windows erkennen und installieren.</li>
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
<li>Führen Sie das Spiel auf 64-Bit-Editionen von Windows aus. Vergewissern Sie sich, dass der Spiele Installationsprozess auf 64-Bit-Editionen von Windows Vista oder Windows 7 normal ausgeführt wird.</li>
<li>Stellen Sie sicher, dass für das Spiel in den 64-Bit-Editionen von Windows Vista oder Windows 7 kein Fehler aufgrund von 16-Bit-ausführbaren Dateien auftritt. Der Fehler wird die 16-Bit-Anwendung im Fehler Fenster erwähnen.</li>
<li>Wenn das Spiel über eine systemeigene ausführbare 64-Bit-Datei verfügt, verwenden Sie diese ebenfalls.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="23-sign-files"></a>2,3 Signier Dateien



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Alle ausführbaren Code Dateien (z. b. exe-und dll-Erweiterungen) müssen mit einem Authenticode-Zertifikat signiert werden. <br/> Wenn Sie Windows Installer verwenden, müssen die Paketdateien (MSI-Dateien) des Installers signiert sein. <br/></td>
</tr>
<tr class="even">

<td>Manueller Test<br/>
<ol>
<li>Navigieren Sie zum Spielverzeichnis.</li>
<li>Suchen Sie alle exe-und dll-Dateien.</li>
<li>Klicken Sie mit der rechten Maustaste auf Eigenschaften für jede Datei.</li>
<li>Vergewissern Sie sich, dass die ausführbaren Dateien des Spiels eine digitale Signatur enthalten.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="24-sign-drivers"></a>2,4-Signatur Treiber



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Jeder Kernelmodustreiber, der durch das Spiel installiert wird, muss mit einem öffentlich gültigen Authenticode-Zertifikat signiert werden. <br/> Jeder vom Spiel installierte Kernel Modus-Hardware Gerätetreiber muss über eine Microsoft-Signatur verfügen, die über das Windows Hardware Quality Labs (WHQL) oder das DRS-Programm (Driver Zuverlässigkeits Signature) abgerufen wird. <br/></td>
</tr>
<tr class="even">

<td>Manueller Test<br/>
<ol>
<li>Installieren Sie das Spiel.</li>
<li>Vergewissern Sie sich, dass bei der Spiele Installation nicht signierte Treiber Dialogfelder angezeigt werden.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="25-perform-version-checking-properly"></a>2,5 Ausführen der Versions Überprüfung ordnungsgemäß



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Spiele dürfen nicht für zukünftige Betriebssysteme ausgeführt werden, die durch Änderungen der Windows-Versionsnummer angegeben werden, es sei denn, der Endbenutzer-Lizenzvertrag untersagt die Verwendung bei zukünftigen Betriebssystemen. Wenn das Spiel fehlschlagen soll, muss es ordnungsgemäß ausgeführt werden, indem eine Meldung für den Benutzer angezeigt wird.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>Manuell</dt> <dd>
<ol>
<li>Installieren Sie das Spiel unter Windows XP, auf 32-Bit-Editionen von Windows Vista und Windows 7 und auf 64-Bit-Editionen von Windows Vista und Windows 7.</li>
<li>Vergewissern Sie sich, dass bei der Spiele Installation kein Fehler in Bezug auf die Betriebssystemversion auftritt.</li>
</ol>
</dd> <dt><span id="Automated_Test"></span><span id="automated_test"></span><span id="AUTOMATED_TEST"></span>Automatisierter Test</dt> <dd> Tool verwenden: Application Verifier<br/>
<ol>
<li>Starten Sie Application Verifier.</li>
<li>Aktivieren Sie die Option Kompatibilität: highversionlie Test, nachdem Sie die INSTALL.EXE ausgewählt haben.</li>
<li>Installieren Sie das Spiel, und stellen Sie sicher, dass es die Installation nicht basierend auf der Betriebssystemversion blockiert.</li>
<li>Aktivieren Sie die Option Kompatibilität: highversionlie Test, nachdem Sie die GAME.EXE ausgewählt haben.</li>
<li>Führen Sie das Spiel aus, und stellen Sie sicher, dass die Ausführung auf Basis der Betriebssystemversion nicht blockiert wird</li>
</ol>
</dd> </dl></td>
</tr>
</tbody>
</table>



 

### <a name="26-support-concurrent-user-sessions"></a>2,6 Unterstützung von gleichzeitigen Benutzersitzungen



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Spiele müssen Windows-Multitasking-Standardszenarien unterstützen.</td>
</tr>
<tr class="even">

<td>Erstellen Sie ein Standard Benutzerkonto in Windows Vista oder Windows 7 namens Toby. Start->-Systemsteuerung-> Benutzerkonten hinzufügen oder entfernen-> neues Konto erstellen <br/>
<ol>
<li>Starten Sie das Spiel als Benutzer Jane.</li>
<li>Alt + Tab zurück zum Desktop.</li>
<li>Überprüfen Sie, ob das Spiel ordnungsgemäß alt + Tabstopps zum Windows-Desktop ist.</li>
<li>Klicken Sie auf Start-> [Pfeil rechts von Lock]-> Switch User.</li>
<li>Melden Sie sich als Benutzer Toby an.</li>
<li>Stellen Sie sicher, dass das Spiel als Benutzer-zu-Ende gestartet wird, während es weiterhin als Benutzer Jane ausgeführt</li>
<li>Stellen Sie sicher, dass für das Spiel während der benutzerswitchverarbeitung keine Fehler für Benutzer-oder Benutzer-Benutzer angezeigt werden.</li>
<li>Wenn Sie eine weitere Spielsitzung starten können, stellen Sie sicher, dass Sie kein Audiomaterial aus der ursprünglichen Spielsitzung hören können.</li>
<li>Schließen Sie das Spiel, und wechseln Sie zurück zum ursprünglichen Benutzer und Spiel.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="27-support-long-names"></a>2,7 Unterstützung von langen Namen



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Wenn ein Spiel das Speichern von Dateien unterstützt, muss es in der Lage sein, Dateien mit langen Namen und Pfaden zu speichern. Das Spiel muss spezielle Dateisystem Zeichen, wie z. b. \/: *, ordnungsgemäß verarbeiten. &quot; < oder > in den Benutzereingabe Feldern, die zum Erstellen von Dateinamen oder Pfaden verwendet werden.</td>
</tr>
<tr class="even">

<td><ol>
<li>Starten Sie das Spiel.</li>
<li>Starten Sie ein neues Spiel.</li>
<li>Speichern Sie das Spiel. Überprüfen Sie während des Speicher Vorgangs, ob das Spiel mit dem Speichern-Namen: mein erstes Save-Spiel gespeichert wird.</li>
<li>Kehren Sie zurück zum Hauptmenü.</li>
<li>Versuchen Sie, das neu gespeicherte Spiel zu laden.</li>
<li>Stellen Sie sicher, dass beim Umgang mit nicht unterstützten Dateisystem Zeichen, wie z. b. \/: *, keine Fehler im Spiel auftreten. &quot; < oder > Wenn Sie das Spiel zulässt, benennen Sie das gespeicherte Spiel.</li>
<li>Wenn der Benutzer das Profil und/oder das Zeichen benennen oder Spiele speichern darf, vergewissern Sie sich, dass beim Verwenden von langen Dateinamen auch bei dem Spiel keine Fehler auftreten.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="3-installation"></a>3. Installation

### <a name="31-easy-install"></a>3,1 einfache Installation



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Spiele mit einer herkömmlichen Installation müssen einen vereinfachten Pfad in der Setup-Benutzeroberfläche bereitstellen.</td>
</tr>
<tr class="even">

<td><ol>
<li>Legen Sie die Spiel-CD ein.</li>
<li>Stellen Sie sicher, dass das Spiel nicht mehr als einen End-User Lizenzvertrag (EULA) anzeigt.</li>
<li>Wenn das Spiel eine benutzerdefinierte oder erweiterte Installationsoption unterstützt, überprüfen Sie, ob diese Option während des Installationsvorgangs verfügbar ist.</li>
<li>Überprüfen Sie, ob die Standard Installationsoption die gesamte Benutzereingabe Auswahl für den Installationsvorgang umgeht (Auswahl von Installationsordner, Komponentenauswahl usw.).</li>
<li>Stellen Sie sicher, dass bei der Spiele Installation keine Eingabeaufforderung für das Setup der Betriebssystem Komponente (DirectX-Setup, Visual C-Runtimes usw.) angezeigt wird.</li>
<li>Vergewissern Sie sich, dass bei der Spiele Installation keine Firewall-Interaktion angefordert wird.</li>
<li>Überprüfen Sie, ob das Spiel automatisch ausgeführt wird oder ob ein Start Programm Menü am Ende des Installationsvorgangs vorhanden ist.</li>
<li>Vergewissern Sie sich, dass bei der Deinstallation des Spiels alle installierten, nicht neu verteilten Betriebssystem-Komponenten Dateien entfernt werden und alle Einstellungen gelöscht werden. Das Bereinigen aller benutzerspezifischen Einstellungen und Daten (z. b. gespeicherter Spiele) ist nicht erforderlich.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="32-support-user-account-control-for-installation"></a>3,2 Unterstützung der Benutzerkontensteuerung für die Installation



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/></td>
<td>Der Game Installer darf nicht davon ausgehen, dass er im gleichen Kontext wie der Benutzer ausgeführt wird. Spiele müssen daher benutzerspezifische Aufgaben bei der ersten Ausführung separat von der Installation ausführen.</td>
</tr>
<tr class="even">

<td><ol>
<li>Vergewissern Sie sich, dass Sie das Spiel als Benutzer Jane installieren können. (Dies erfordert erhöhte Rechte während des Setup-/Installationsprozesses.)</li>
<li>Vergewissern Sie sich, dass der Spiel Installationsprozess Benutzer Jane auffordert, Rechte über Administrator Anmelde Informationen zu erhöhen. (Die Aufforderung zur Erhöhung der Rechte wird angezeigt, wenn der Benutzer versucht, zu installieren.)</li>
<li>Deaktivieren Sie das Spiel am Ende der Installation, falls dies noch nicht der Fall ist, oder starten Sie es über das Menü, das angezeigt wird.</li>
<li>Erstellen Sie ein neues Profil, und spielen Sie ein Spiel, und speichern Sie es.</li>
<li>Beenden Sie das Spiel.</li>
<li>Starten Sie das Spiel neu, und stellen Sie sicher, dass das Benutzer-und die gespeicherten Spiele vom Benutzer-Jane-Konto aufgerufen wird.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="33-install-to-correct-folders"></a>3,3 in richtigen Ordnern installieren



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Spiele müssen standardmäßig im Ordner "Programme" installiert werden. Benutzerdaten müssen bei der ersten Testlauf und nicht während der Installation geschrieben werden.</td>
</tr>
<tr class="even">

<td><ol>
<li>Installieren Sie das Spiel mit dem Standard Installationstyp.</li>
<li>Vergewissern Sie sich, dass das Spiel für die Programmdateien installiert wurde.</li>
</ol>
<blockquote>
[!Note]<br />
Wenn bei diesem Test ein Fehler auftritt, überprüfen Sie, ob das Spiel für alle Benutzer installiert werden soll. Wenn dies der Fall ist, ist dies ein Fehler.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="34-install-windows-resources-properly"></a>3,4 Windows-Ressourcen ordnungsgemäß installieren



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Anwendungen dürfen nicht versuchen, Dateien oder Registrierungsschlüssel zu installieren, die durch Windows-Ressourcenschutz (WRP) geschützt sind.</td>
</tr>
<tr class="even">

<td><ul>
<li>Vergewissern Sie sich, dass während des Installationsvorgangs keine Windows-Ressourcenschutz WRP-Dialogfelder angezeigt werden.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="35-avoid-reboots-during-installation"></a>3,5 vermeiden Neustarts während der Installation



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Der Game Installer sollte nicht davon ausgehen, dass die Installation von Windows-Komponenten aus weitergabepaketen einen Neustart erfordert, es sei denn, der Neustart wird durch ein Rückgabe Ergebnis oder von der Microsoft-Dokumentation angegeben.</td>
</tr>
<tr class="even">

<td><ol>
<li>Installieren Sie das Spiel.</li>
<li>Vergewissern Sie sich, dass das System nach der Installation nicht neu gestartet werden muss.</li>
</ol>
<blockquote>
[!Note]<br />
Wenn ein Microsoft System Update Redist einen Neustart erfordert, führen Sie die folgenden Schritte aus: Beenden Sie die Spiele Installation, deinstallieren Sie das Spiel, und installieren Sie das Spiel ein zweites Mal. Bei der Installation des Spiels sollte bei dieser zweiten Installation kein Neustart erforderlich sein.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="36-use-file-versioning-correctly"></a>3,6 verwenden Sie die Datei Versionsverwaltung ordnungsgemäß.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Das Spiel Installationsprogramm muss ordnungsgemäß überprüft werden, um sicherzustellen, dass die aktuellsten Dateiversionen installiert sind. Bei der Installation eines Spiels dürfen keine Dateien erneut verwendet werden, die Sie nicht erstellt haben oder die von nicht erzeugten Anwendungen gemeinsam genutzt werden.</td>
</tr>
<tr class="even">

<td><ol>
<li>Erstellen Sie vor der Installation des Spiels eine Vorinstallations Momentaufnahme von system32.<br/>
<ol>
<li>Erstellen Sie ein Verzeichnis mit dem Namen G4Wtest.</li>
<li>Öffnen Sie ein Befehlsfenster (Start-> Run-> cmd).</li>
<li>Navigieren Sie zu "c:\Windows\System32.".</li>
<li>Geben Sie dir/o:-g/o:-d >> c:\G4Wtest\pregame.txt ein.</li>
</ol></li>
<li>Erstellen Sie eine Momentaufnahme nach der Installation von system32. <br/>
<ol>
<li>Öffnen Sie ein Befehlsfenster (Start-> Run-> cmd).</li>
<li>Navigieren Sie zu "c:\Windows\System32.".</li>
<li>Geben Sie dir/o:-g/o:-d >> c:\G4Wtest\postgame.txt ein.</li>
<li>Stellen Sie sicher, dass das Spiel keine Dateiversionen von Dateien, die das Spiel nicht erstellt hat (... der Dateien, die in den beiden Dokumenten aufgeführt sind, indem pregame.txt mit postgame.txt) verglichen werden.</li>
</ol></li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="37-support-autorun-conditional-requirement"></a>3,7 Unterstützung für die bedingte Anforderung von Autorun \[\]



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Bei spielen, die auf CD, DVD oder anderen Wechselmedien verteilt sind, die Autorun unterstützen, muss die Anwendung automatisch ausgeführt werden, um den Benutzer zur Installation des Spiels aufzufordern, wenn die Festplatte zum ersten Mal eingefügt wird. <br/>
<blockquote>
[!Note]<br />
Für autorun-Programme, die für Windows-Versionen vor Windows Vista geschrieben wurden, sollte die .NET-Laufzeit nicht verwendet werden, da diese Technologie nicht in Windows XP oder älteren Versionen von Windows enthalten ist.
</blockquote>
<br/> Weitere Anleitungen finden Sie unter <a href="/windows/win32/DxTechArts/games-for-windows-technical-requirements-1-1-0006">Games for Windows Technical Requirements</a> 3,7, Support Autorun. <br/></td>
</tr>
<tr class="even">

<td><ol>
<li>Fügen Sie die Spiel-CD oder die Medien ein.</li>
<li>Überprüfen Sie, ob das Dialogfeld installieren/ausführen automatisch angezeigt wird.</li>
<li>Windows Vista oder Windows 7: Vergewissern Sie sich, dass das Spiel Autorun-Programm selbst Benutzer Jane nicht auffordert, die Rechte über Administrator Anmelde Informationen zu erhöhen.</li>
<li>Vergewissern Sie sich, dass die ausführbare Datei Autorun keine standardmäßig erforderlichen Redist-Komponenten wie .NET 3,5, C Run-Time-Bibliotheken usw. benötigt.</li>
<li>Vergewissern Sie sich, dass die Installation des Laufwerks nach der Installation nicht automatisch startet.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="4-reliability"></a>4. Zuverlässigkeit

### <a name="41-eliminate-unnecessary-reboots"></a>4,1 Entfernen unnötiger Neustarts



|                                               |                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows 7<br/> Windows Vista<br/> | Alle Anwendungsinstallations Programme müssen die APIs für den Neustart-Manager nutzen, um Systemneustarts zu vermeiden (siehe [Anforderung 3,5](#35-avoid-reboots-during-installation)). |



 

### <a name="42-eliminate-application-verifier-failures"></a>4,2 Vermeiden von Application Verifier Fehlern



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Das Spiel muss in den folgenden Tests keine Fehler erzeugen, die unter Microsoft Application Verifier (AppVerifier), Version 4,0 oder höher, ausgeführt werden: <br/>
<ul>
<li>Grundlagen: Handles, Heaps, sperren, Arbeitsspeicher, TLS</li>
<li>Sonstige: dangerousapis, dirtystacks</li>
</ul></td>
</tr>
<tr class="even">

<td>Tool verwenden: AppVerifier 4,0 (oder höher)<br/>
<ol>
<li>Installieren Sie AppVerifier.</li>
<li>Starten Sie AppVerifier, und wählen Sie Datei-> Anwendung hinzufügen aus.</li>
<li>Suchen Sie die ausführbare Datei, wählen Sie Sie aus, und klicken Sie auf die &quot; &quot; Schaltfläche Öffnen</li>
<li>&quot; &quot; Wählen Sie im Abschnitt Anwendungen die ausführbare Datei für das Spiel aus.</li>
<li>&quot; &quot; Wählen Sie im Abschnitt Tests die oben aufgeführten Tests unter den Kategorien &quot; Grundlagen &quot; und &quot; Sonstiges aus &quot; (deaktivieren Sie Thread Pool und timerollover), und stellen Sie sicher, dass keine anderen Tests ausgewählt sind.</li>
<li>Starten Sie das Spiel.</li>
<li>Vergewissern Sie sich, dass das Spiel keine Fehler generiert, wenn es unter Application Verifier ausgeführt wird.</li>
</ol>
<blockquote>
[!Note]<br />
Für einige Tests muss ein Debugger vollständig ausgeführt werden. Dies erfordert möglicherweise eine ungeschützte Releaseversion der ausführbaren Datei des Spiels, da die Anticheat-/anticodeingtechnologie mit appverifer beeinträchtigt werden kann.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="43-support-windows-error-reporting"></a>4,3 Support Windows-Fehlerberichterstattung



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Spiele müssen nur bekannte Ausnahmen behandeln, und Windows-Fehlerberichterstattung dürfen nicht deaktiviert werden. Wenn ein Fehler (z. b. eine Zugriffsverletzung) in ein Spiel eingefügt wird, muss Windows-Fehlerberichterstattung den Absturz melden können.</td>
</tr>
<tr class="even">

<td>Tool verwenden: Thread-Hijacker <br/>
<ul>
<li>Wenn die Anwendung beim Testen abstürzt, vergewissern Sie sich, dass das Spiel Windows-Fehlerberichterstattung ordnungsgemäß angezeigt wird, und sammelt Absturz Daten.</li>
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
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Alle ausführbaren Dateien (z. b. exe-oder DLL-Dateien) müssen einen exakten Produktnamen, den Firmennamen und die Datei Version enthalten.</td>
</tr>
<tr class="even">

<td><dl> <dt><span id="Manual_test_"></span><span id="manual_test_"></span><span id="MANUAL_TEST_"></span>Manueller Test:</dt> <dd>
<ol>
<li>Klicken Sie mit der rechten Maustaste auf die ausführbaren Dateien des Spiels auf den Installationsmedien und auf den Computern, die auf der Computer Festplatte installiert sind.</li>
<li>Wählen Sie „Eigenschaften“.</li>
<li>Windows XP: Klicken Sie auf die Registerkarte <strong>Version</strong> . Überprüfen Sie, ob die Felder Produktname, Firmenname und Datei Version ordnungsgemäß ausgefüllt sind.</li>
<li>Windows Vista oder Windows 7: Klicken Sie auf die Registerkarte <strong>Details</strong> . Überprüfen Sie, ob die Felder Product Name und File Version ordnungsgemäß aufgefüllt sind. Der Name des Unternehmens ist auf der Eigenschaften Seite von Windows Vista oder Windows 7 nicht sichtbar.</li>
</ol>
</dd> <dt><span id="Automated_test_"></span><span id="automated_test_"></span><span id="AUTOMATED_TEST_"></span>Automatisierter Test:</dt> <dd>
<ul>
<li>Verwenden Sie das Microsoft Games for Windows-Testtool; siehe <a href="#64-microsoft-games-for-windows-test-tool">Abschnitt 6,4</a>.</li>
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
<td>Windows 7<br/> Windows Vista<br/> Windows XP<br/></td>
<td>Der normale Beenden des Spiels darf keinen unbekannten Ausnahme Fehler verursachen.</td>
</tr>
<tr class="even">

<td><ul>
<li>Nachdem Sie das Spiel für eine normale Gaming-Sitzung abgespielt haben, stellen Sie sicher, dass das Spiel beim Beenden keine Fehler generiert.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="5-sample-test-script"></a>5. Beispiel Test Skript

Dies ist ein Beispiel für einen typischen Test Durchlauf, bei dem die vorangehenden Testanforderungen als Leitfaden verwendet werden.

### <a name="51-tools"></a>5,1-Tools

-   32-Bit-Edition von Windows Vista SP1 und/oder Windows 7 auf einer AMD-CPU
-   32-Bit-Edition von Windows Vista SP1 und/oder Windows 7 auf einer Intel-CPU
-   64-Bit-Edition von Windows Vista SP1 und/oder Windows 7 auf einer AMD-CPU
-   64-Bit-Edition von Windows Vista SP1 und/oder Windows 7 auf einer Intel-CPU
-   32-Bit Edition Windows XP SP2 auf einer AMD-CPU
-   32-Bit Edition Windows XP SP2 auf einer Intel CPU
-   Monitor für Breite Bildschirm, der 1680 1050 unterstützt
-   Xbox 360-Controller für Windows

### <a name="52-pre-install"></a>5,2 vor der Installation

1.  Windows Vista und Windows 7: Erstellen Sie zwei Standard Benutzer: Jane und Deby
2.  Windows Vista und Windows 7: Stellen Sie sicher, dass die Benutzerkontensteuerung aktiviert ist.
3.  Erstellen einer Vorinstallations Momentaufnahme von system32

    1.  Erstellen Sie ein Verzeichnis mit dem Namen G4Wtest
    2.  Öffnen Sie ein Befehlsfenster (Start-> Run-> cmd).
    3.  Navigieren Sie zu "c: \\ Windows System32". \\
    4.  Geben Sie dir/o:-g/o:-d >> c: \\ G4Wtest \\pregame.txt

4.  Windows Vista und Windows 7: auf 150% dpi \[ 1,8 festlegen\]
5.  Mit der [Installation](#3-installation) fortfahren

### <a name="53-install"></a>5,3-Installation

1.  Anmelden als Benutzer Jane
2.  Legen Sie den Spiel Datenträger in das CD/DVD-Laufwerk ein, vergewissern Sie sich, dass das Dialogfeld installieren/ausführen automatisch angezeigt wird \[ 3,7\]
3.  Vergewissern Sie sich, dass der Spiel Installationsprozess Benutzer Jane auffordert, Administrator Anmelde Informationen zu erhöhen \[ 3,2\]
4.  Stellen Sie sicher, dass das Spiel Autorun-Programm selbst Benutzer Jane nicht auffordert, die Rechte über Administrator Anmelde Informationen zu erhöhen \[ 3,7\]
5.  Vergewissern Sie sich, dass das Spiel nicht mehr als einen End-User Lizenzvertrag (EULA) 3,1 anzeigt. \[\]
6.  Stellen Sie sicher, dass das Spiel die Optionen default/Easy und Custom/Advanced Installation \[ 3,1\]
7.  Vergewissern Sie sich, dass die Option Standard/einfache Installation alle Benutzereingabe-Auswahl Optionen für den Installationsvorgang umgeht (Auswahl von Installationsordner, Komponentenauswahl usw.) \[ . 3,1\]
8.  Vergewissern Sie sich, dass bei der Spiele Installation keine Eingabeaufforderung für das Setup der Betriebssystem Komponente (DirectX-Setup, C Run-Time-Bibliotheken usw.) \[ angezeigt wird. 3,1\]
9.  Stellen Sie sicher, dass bei der Spiele Installation keine Aufforderung zur firewallinteraktion 3,1 angezeigt wird. \[\]
10. Vergewissern Sie sich, dass bei der Spiele Installation kein Fehler in Bezug auf die Betriebssystem Version \[ 2,5 \] \[ 4,2 auftritt.\]
11. Stellen Sie sicher, dass bei der Spiele Installation nicht signierte Treiber Dialog (e) 2,4 angezeigt werden. \[\]
12. Vergewissern Sie sich, dass während des Installationsvorgangs 3,4 keine Windows-Ressourcenschutz (WRP)-Dialogfelder angezeigt werden. \[\]
13. Vergewissern Sie sich, dass die Installation des Laufwerks nach der Installation nicht automatisch startet.
14. Vergewissern Sie sich, dass das System nach der Installation 3,5 nicht neu gestartet werden muss. \[\]
15. Vergewissern Sie sich, dass Sie das Spiel als Benutzer Jane 3,2 installieren können. \[\]
16. Überprüfen Sie, ob das Spiel automatisch ausgeführt wird oder ob ein Start Programm Menü am Ende des Installationsvorgangs 3,1 vorhanden ist. \[\]
17. Wenn das Spiel nach der Installation automatisch ausgeführt wird, springen Sie zur [Laufzeit](#55-runtime) .
18. Wenn das Spiel ein Startmenü geöffnet hat oder die Deinstallation fehlgeschlagen ist, lesen Sie den Abschnitt [nach der Installation](#54-post-install) .

### <a name="54-post-install"></a>5,4 nach der Installation

1.  Stellen Sie sicher, dass das Spiel keine Start Verknüpfungen auf dem Benutzer Desktop 1,1 platziert. \[\]
2.  Stellen Sie sicher, dass das Spiel keine Start Verknüpfungen im Startmenü \[ 1,1.\]
3.  Überprüfen Sie, ob das Spiel Symbol in Windows Games Explorer 1,1 angezeigt wird. \[\]
4.  Vergewissern Sie sich, dass die Metadaten (Verleger, Entwickler, Genre, Veröffentlichungsdatum, Version) unten angezeigt werden und korrekt \[ 1,1\]
5.  Überprüfen Sie, ob das Symbol "Spiel" Informationen zum Windows-Erfahrungs Index (Wei) in Windows Games Explorer \[ 1,1 anzeigt\]
6.  Überprüfen Sie, ob die Spiel Hyperlinks für Metadaten in Windows Games Explorer 1,1 ordnungsgemäß funktionieren. \[\]
7.  Stellen Sie sicher, dass das Spiel in Windows Games Explorer 1,1 eine genaue Bewertung der Jugend Steuerung anzeigt. \[\]
8.  Erstellen einer nach Installations Momentaufnahme von system32

    1.  Öffnen Sie ein Befehlsfenster (Start-> Run-> cmd).
    2.  Navigieren Sie zu "c: \\ Windows System32". \\
    3.  Geben Sie dir/o:-g/o:-d >> c: \\ G4Wtest \\postgame.txt
    4.  Stellen Sie sicher, dass das Spiel keine Dateiversionen von Dateien, die in den beiden Dokumenten aufgeführt sind, wiederholt, indem Sie pregame.txt mit postgame.txt 3,6 vergleichen. \[\]

9.  Zur [Laufzeit](#55-runtime) fortfahren

### <a name="55-runtime"></a>5,5-Laufzeit

1.  Laufzeit 1: Wenn das Startmenü vorhanden ist, starten Sie das Spiel von dort aus. Wenn das Spiel automatisch ausgeführt wurde oder nach der Installation über das Spiel Startmenü gestartet wurde, führen Sie Folgendes aus: Wenn nicht, fahren Sie mit Laufzeit 2 fort:

    1.  Erstellen eines Profils (wenn das Spiel zulässt)
    2.  Neues Spiel starten
    3.  Speichern des Spiels
    4.  Beenden des Spiels
    5.  Starten Sie das Spiel im Spiele-Explorer.
    6.  Überprüfen Sie, ob das Spiel über das 1,2 Symbol "Games Explorer" gestartet wird \[\]
    7.  Stellen Sie sicher, dass das Spiel beim Start 1,2 keine Administrator Anmelde Informationen auffordert. \[\]
    8.  Stellen Sie sicher, dass Benutzer Jane Account 3,2 auf Benutzerprofile und Save Games zugreifen können. \[\]
    9.  Mit Laufzeit 3 fortfahren

2.  Laufzeit 2: Wenn das Spiel nicht automatisch ausgeführt wurde oder einen Start über das Spiel Startmenü anzeigt, ist dies ein Fehler von \[ 3,1 \] ; das Testen kann jedoch normal fortgesetzt werden:

    1.  Starten Sie das Spiel im Spiele-Explorer.
    2.  Überprüfen Sie, ob das Spiel über das 1,2 Symbol "Games Explorer" gestartet wird \[\]
    3.  Stellen Sie sicher, dass das Spiel beim Start 1,2 keine Administrator Anmelde Informationen auffordert. \[\]
    4.  Mit Laufzeit 3 fortfahren

3.  Laufzeit 3: Wenn das Spiel einen Spielblock unterstützt, vergewissern Sie sich, dass das Spiel Xbox 360-Controller für Windows als Eingabegerät (1,4) erkennt. \[\]

    1.  Aktivieren Sie den Controller bei Bedarf über das Menü "Optionen".
    2.  Stellen Sie sicher, dass das Spiel auf die Controller Schaltflächen und Trigger mit Xbox 360-Namen verweist.
    3.  Überprüfen Sie, ob das Spiel und das Menüsystem mit dem Xbox 360-Controller für Windows steuerbar sind.
    4.  Stellen Sie sicher, dass sich der Xbox 360-Controller für Windows gemäß den akzeptierten Standards verhält.

4.  Legen Sie das Video auf \[ 1,5 fest \] :

    1.  Überprüfen Sie, ob das Spiel bei einer 4:3-Seitenverhältnis Auflösung (800 600 oder 1024 768) ausgeführt wird.
    2.  Überprüfen Sie, ob das Spiel bei einer 16:9-Seitenverhältnis Auflösung (1280 720) ausgeführt wird.
    3.  Überprüfen Sie, ob das Spiel bei einer 16:10-Seitenverhältnis Auflösung (1680 1050, 800 480 oder 1152 720) ausgeführt wird.
    4.  Überprüfen Sie, ob das Spiel den Benutzer auffordert, wenn eine Änderung an der Auflösung vorgenommen wird.
    5.  Vergewissern Sie sich, dass die Anzeige auf die vorherige Einstellung zurückgesetzt wird, wenn Sie Sie nicht innerhalb von 15 Sekunden akzeptieren.
    6.  Stellen Sie sicher, dass das Spiel das Bild nicht gestreckt und wiederum einen breiteren Bereich der Ansicht darstellt.
    7.  Stellen Sie sicher, dass das Spiel keine schwarzen Balken Links und rechts im Spielbereich des Spiels hinzufügt.

5.  Wenn Sie in den Videoeinstellungen verfügbar sind, überprüfen Sie, ob die Optionen für das spielrendering standardmäßig Direct3D \[ 1,7 sind \] ; andernfalls fahren Sie mit [automatisierte Tests](#58-automated-tests) fort
6.  Wenn Sie dazu aufgefordert werden oder wenn die Option verfügbar ist, erstellen Sie ein Benutzerprofil. Stellen Sie sicher, dass für das Spiel keine Fehler auftreten, wenn Sie lange Dateinamen 2,7 verwenden. \[\]
7.  Starten Sie ein neues Spiel, erstellen Sie ein Spiel, und stellen Sie sicher, dass das Spiel bei der Behandlung nicht unterstützter Dateisystem Zeichen nicht fehlerhaft ist \[ 2,7\]
8.  Überprüfen Sie, ob das Spiel ordnungsgemäß alt + Tabstopps zum Windows-Desktop \[ 2,6\]

    1.  Benutzer mit dem Spiel wechseln, indem Sie auf Start > Switch-Benutzer klicken
    2.  Anmelden als Toby
    3.  Stellen Sie sicher, dass das Spiel als Benutzer-zu-Ende gestartet wird, während es weiterhin als Benutzer Jane \[ 2,6\]
    4.  Stellen Sie sicher, dass das Spiel während des Benutzer Umschalters nicht Fehler für Benutzer-oder Benutzer-Jane-Vorgang \[ 2,6\]
    5.  Vergewissern Sie sich, dass Sie Audiodaten aus der ursprünglichen Spielsitzung 2,6 nicht hören können. \[\]
    6.  Beenden des Spiels
    7.  Abmelden bei Toby
    8.  Wechseln Sie zurück zum ursprünglichen Benutzer, auf dem das Spiel ausgeführt wird.
    9.  Alt + Tab zurück zum Spiel

9.  Beenden des Spiels
10. Mit der [Post-Laufzeit](#56-post-runtime) fortfahren

### <a name="56-post-runtime"></a>5,6 nach der Laufzeit

1.  Stellen Sie sicher, dass das Spiel bei Exit 4,3 keine Fehler generiert. \[\]
2.  Überprüfen Sie, ob das auf den Programmdateien 3,3 installierte Spiel \[\]
3.  Mit [Eltern Steuerungs](/windows) Maßnahmen fortfahren

### <a name="57-parental-controls"></a>5,7 Eltern Steuerelemente

1.  Öffnen Sie in der Systemsteuerung die Option Jugendschutz
2.  Stellen Sie sicher, dass das Spiel unter dem Spieltitel in der Systemsteuerung \[ 1,2\]
3.  Weitere Informationen finden Sie unter Testfall \[ 1,2 \] für die folgenden Tests:

    1.  Überprüfen Sie nach dem Festlegen der Jugend Steuerelemente auf "ein", ob das Spiel mit diesen Einstellungen ausgeführt wird, als Benutzer Jane \[ 1,2.\]
    2.  Abmelden und Anmelden als Toby
    3.  Stellen Sie sicher, dass das Spiel mit diesen Einstellungen als Benutzer-/1,2 ausgeführt wird. \[\]
    4.  Melden Sie sich ab, und melden Sie sich als Jane an
    5.  Blockieren Sie im Abschnitt "Jugendschutz" den Benutzer damit, dass Spiele eine ESRB-Ebene von dem soeben installierten Spiel sehen.

        Beispiel: Wenn das Spiel mit E bewertet wird, legen Sie es so fest, dass "tby" nur Spiele abspielen kann, die als "C

    6.  Überprüfen Sie, ob das Spiel mit diesen Einstellungen ausgeführt wird, als Benutzer Jane \[ 1,2.\]
    7.  Melden Sie sich ab, und melden Sie sich als Benutzer Toby an
    8.  Stellen Sie sicher, dass das Spiel nicht für Benutzer "Deby" gestartet wird, wenn ESRB durch den Benutzer Jane 1,2 blockiert wird. \[\]
    9.  Melden Sie sich als Benutzer Toby und wieder als Benutzer Jane an.
    10. Stellen Sie die ESRB-Einstellungen wieder her
    11. Wenn keine ESRB-Einstellungen vorhanden sind, wählen Sie "bestimmte Spiele blockieren oder zulassen" aus, und wählen Sie das Spiel nach Name aus.
    12. Melden Sie sich als Andrea und als Toby ab.
    13. Stellen Sie sicher, dass das Spiel nicht für Benutzer "Deby" gestartet wird, wenn "exe/Name" vom Benutzer Jane 1,2 blockiert wird \[\]
    14. Melden Sie sich als "Toby" und "zurück" als Andrea an
    15. Als Andrea öffnen Sie die Benutzer Steuerelemente > Anwendungs Einschränkungen
    16. Klicken Sie auf "auf" kann nur die von mir zugelassenen Programme verwendet werden ", und klicken Sie dann auf" OK "(keine exe-Datei zulassen).
    17. Aktivieren Sie das Kontrollkästchen Alle deaktivieren, und klicken Sie dann auf OK.
    18. Wechseln Sie zu Benutzer Steuerelemente \| Spiele Steuerelemente, und lassen Sie das jeweilige Spiel mithilfe der ESRB-Bewertung zu
    19. Melden Sie sich als Andrea ab, und melden Sie sich als Toby an, und wiederholen Sie das Spiel.
    20. 1,2 Stellen Sie sicher, dass das Spiel nicht blockiert ist, und dass es von "von" (keine exe-Datei zulassen) wiedergegeben werden kann. \[\]
    21. Melden Sie sich als Benutzer Toby und wieder als Benutzer Jane an.
    22. Wechseln Sie in der Systemsteuerung zu Jugendschutz, und entfernen Sie die Einschränkungen.
    23. Stellen Sie sicher, dass beide Benutzer jetzt das Spiel abspielen können.

4.  Mit [automatisierten Tests](#58-automated-tests) fortfahren

### <a name="58-automated-tests"></a>5,8 automatisierte Tests

1.  Stellen Sie 4,2 sicher, dass das Spiel keine Fehler generiert, wenn Sie es unter Application Verifier ausführen \[\]
2.  Vergewissern Sie sich, dass die ausführbaren Dateien des Spiels Manifeste enthalten. siehe Branding-Test Tool Dokumentation \[ 2,1\]
3.  Vergewissern Sie sich, dass das ausführbare Datei Manifest requestedExecutionLevel "asInvoker" ist. Informationen hierzu finden Sie unter Branding Test Tool-Dokumentation \[ 2,1\]
4.  Mit [anderen Tests](#59-other-tests) fortfahren

### <a name="59-other-tests"></a>5,9 andere Tests

1.  Überprüfen Sie, ob die ausführbaren Dateien des Spiels eine digitale Signatur \[ 2,3 enthalten\]
2.  Überprüfen Sie, ob der Spiel Installationsprozess auf 64-Bit-Editionen von Windows Vista und/oder Windows 7 2,3 normal ausgeführt wird. \[\]
3.  Stellen Sie sicher, dass das Spiel aufgrund von 16-Bit-ausführbaren Dateien auf 64-Bit-Editionen von Windows Vista und/oder Windows 7 2,3 keinen Fehler verursacht. \[\]
4.  Erzwingen Sie einen Absturz der Anwendung beim Testen, und vergewissern Sie sich, dass das Spiel Windows-Fehlerberichterstattung ordnungsgemäß angezeigt wird, und erfasst die Absturz Daten \[ 4,3\]
5.  Ordnungsgemäße Datei Zusammenfassungen \[ 4,3\]

    1.  Klicken Sie auf Start-> Computer.
    2.  Navigieren Sie zum Spielverzeichnis.
    3.  Geben Sie im Suchfenster " \* . dll" ein.
    4.  Klicken Sie mit der rechten Maustaste auf die Datei, und klicken Sie dann auf Eigenschaften.

        -   Unter Windows XP: Klicken Sie auf die Registerkarte Version. Überprüfen Sie, ob die Felder Produktname, Firmenname und Datei Version ordnungsgemäß ausgefüllt sind. \[4.3\]
        -   In Windows Vista und Windows 7: Klicken Sie auf die Registerkarte Details. Überprüfen Sie, ob die Felder Product Name und File Version ordnungsgemäß aufgefüllt sind. Der Name des Unternehmens ist auf der Eigenschaften 4,3 Seite von Windows Vista oder Windows 7 nicht sichtbar. \[\]

    5.  Wiederholen Sie diese Prüfung auf exe-Dateien.

6.  Starten Sie das Spiel.

    1.  STRG + ALT + ENTF drücken
    2.  Klicken Sie auf den Pfeil "Optionen für das Herunterfahren"
    3.  Klicken Sie auf Neustart
    4.  Überprüfen, ob das Spiel das Herunterfahren \[ 3,1 blockiert\]

7.  [Deinstallation](#510-uninstall) fortsetzen

### <a name="510-uninstall"></a>5,10 deinstallieren

-   Überprüfen Sie, ob bei der Deinstallation des Spiels alle installierten, nicht verteilbaren Betriebssystem-Komponenten Dateien entfernt werden, und löschen Sie alle Einstellungen \[ 3,1.\]

    -   Überprüfen Sie unter Windows Vista oder Windows 7, dass die Systemsteuerung die einzige Möglichkeit zum Entfernen des Programms 1,1 ist. \[\]

## <a name="test-tool-notes"></a>Anmerkungen zum Testtool

Dies sind Hinweise für die einzelnen Testtools, die in den obigen Testanforderungen aufgeführt sind.

### <a name="61-appverifier-40-or-higher"></a>6,1 AppVerifier 4,0 (oder höher)

**Testfall: 2,5, 4,2**

> [!Note]  
> Einige Anwendungen können aufgrund des Kopierschutzes nicht mit AppVerifier ausgeführt werden. Dies kann durch Ausführen von mit einer ungeschützten Releaseversion der ausführbaren Spieldatei behoben werden.

 

1.  Installieren von AppVerifier 4,0 (oder höher) auf einem Computer mit Windows XP
2.  Starten Sie AppVerifier, und klicken Sie auf Datei > Anwendung hinzufügen.
3.  Suchen Sie die ausführbare Datei, wählen Sie Sie aus, und klicken Sie
4.  Wählen Sie im Abschnitt "Anwendungen" die ausführbare Datei für das Spiel aus.
5.  Wählen Sie im Abschnitt "Grundlagen" die folgenden Tests aus:

    -   Ziehpunkte
    -   Heaps
    -   Locks
    -   Arbeitsspeicher
    -   TLS

6.  Wählen Sie im Abschnitt "Verschiedenes" die folgenden Tests aus:

    -   Dangerousapis
    -   Dirtystacks

7.  Stellen Sie sicher, dass keine anderen Tests ausgewählt sind.
8.  Starten des Spiels
9.  Spielen Sie das Spiel
10. Schließen Sie das Spiel.
11. Wählen Sie in AppVerifier > Protokolle anzeigen aus.
12. Wählen Sie im Abschnitt "Anwendungen" die Datei "App. exe" aus.
13. Wählen Sie im Abschnitt "Protokolle" die Protokolldatei aus, und beobachten Sie die Fehler Anzahl. Wenn keine Fehler vorliegen, beenden Sie AppVerifier-Tests. Wenn Fehler auftreten, klicken Sie auf die Schaltfläche "Ansicht".
14. Durchsuchen Sie das Dokument (STRG + F) nach Schweregrad = "Fehler
15. Erstellen von Fehlern basierend auf dem "Layername ="-Teil des Fehlers

### <a name="62-manifest-test---mtexe"></a>6,2 Manifest-Test-mt.exe

**Testfall: 1,8, 2,1**

Dieses Tool wird an einer Eingabeaufforderung ausgeführt, in der sich MT.exe befindet.

Beispiel:

``` syntax
mt.exe -inputresource:"c:\yourdir\YourGame.exe";#1 -out:yourgame.manifest
```

1.  Klicken Sie auf Start-> Run-> type cmd, und klicken Sie auf die Schaltfläche OK.
2.  Führen Sie das mt.exe Tool aus, um für jede exe-Datei, die mit dem Spiel installiert wird, eine Manifest-Datei zu generieren.
3.  Öffnen Sie die generierte Manifest-Datei.
4.  Stellen Sie sicher, dass jede exe-Datei Folgendes enthält (angefordert:

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
> Die angeforderte Ausführungs Ebene sollte für jede Datei vorhanden sein, und für mindestens die ausführbare Datei des Spiels muss dpiaware vorhanden sein.

 

### <a name="63-thread-hijacker---threadhijackerexe"></a>6,3 Thread-Hijacker-threadhijacker.exe

Dieses Tool wird an einer Eingabeaufforderung ausgeführt, in der sich threadhijacker.exe befindet.

Beispiel:

``` syntax
threadhijacker.exe /process:str
```

Dabei ist Str der Name \_ \_program.exe

1.  Rufen Sie den Task-Manager auf, klicken Sie auf die Registerkarte Prozesse, und suchen Sie den Namen des ausführbaren Spiels.
2.  Öffnen Sie eine Eingabeaufforderung im Administrator Modus.
3.  Navigieren Sie zu dem Verzeichnis, in dem threadhijacker.exe
4.  Type: **threadhijacker.exe/Process:** Str, wobei Str der Name der ausführbaren Datei ist, die Sie erreichen möchten.

### <a name="64-microsoft-games-for-windows-test-tool"></a>6,4 Microsoft Games for Windows-Testtool

Dieses Tool befindet sich im DirectX SDK. Sobald das SDK auf einem Computer installiert ist, kann das Installationsprogramm für das Testtool Games for Windows auf dem Testcomputer abgelegt und installiert werden.

Suchen Sie auf dem Entwicklungs Computer, auf dem das DirectX SDK installiert ist, das Installationsprogramm für Microsoft Games for Windows Test Tool. Standardmäßig wird Sie an folgendem Speicherort platziert:

``` syntax
%SystemDrive%\Program Files (x86)\Microsoft DirectX SDK (Date)\Utilities\bin\x86\Microsoft Games for Windows Test Tools\
```

1.  Kopieren Sie das Installationsprogramm (MicrosoftGFWTestTool.msi/setup.exe) auf den Testcomputer.
2.  Führen Sie das Installationsprogramm aus.
3.  Starten Sie das Testtool Microsoft Games for Windows.
4.  Ersetzen Sie im Feld **Projektliste** das Feld **Neues Projekt** durch ihren Titel Namen erstellen, und klicken Sie auf **neu erstellen**.

    Warten Sie, bis die Baseline fertiggestellt ist.

5.  Geben Sie alle Informationen ein, die Sie möglicherweise im Abschnitt " **Spielinformationen** " haben, und klicken Sie auf " **Spielinformationen aktualisieren**".
6.  Klicken Sie auf die Registerkarte **Testfälle** .
7.  Beginnen Sie im oberen Bereich mit den Testfällen, und klicken Sie nach Bedarf auf **übergeben** oder **fehlschlagen** .

    Weitere Informationen zum Einschließen eines Fehlers in den Bericht finden Sie unter "Schreiben eines Fehlers" weiter unten in diesem Abschnitt.

8.  Kehren Sie nach dem Überprüfen des Berichts zur Registerkarte **Projekte** zurück (durch Überprüfen der Registerkarten **Bericht** und **Fehler Bearbeitung** ).
9.  Klicken Sie auf **Bericht kompilieren**.

    Ein Fenster wird geöffnet, wenn die Kompilierung des Berichts abgeschlossen ist. Hier finden Sie eine. ZIP-Dateinamen *Projektname* \_report.zip. Diese Datei enthält alle Protokolle und Ergebnisse, die während des Tests erfasst wurden.

### <a name="writing-a-bug"></a>Schreiben eines Fehlers

Es gibt zwei Möglichkeiten, einen Fehlerbericht zu schreiben: Sie können die Testfälle durchlaufen und auf "Fehler" klicken, wenn der Titel einen Testfall fehlschlägt, oder Sie können auf die Registerkarte " **Fehler Bearbeitung** **" klicken und** manuell einen Fehlerbericht hinzufügen.

### <a name="clicking-fail-on-a-test-case"></a>Klicken auf "Fehler" bei einem Testfall

1.  Wenn Sie bei einem Testfall **auf "Fehler" klicken,** wird die Dropdown Liste " **Problemtyp** " automatisch auf den Testfall-Typ festgelegt.
2.  Fügen Sie dem Feld **Title** eine kurze Beschreibung hinzu, in der das Problem kurz beschrieben wird.
3.  Fügen Sie dem Feld " **beobachteter Verhalten** " eine ausführliche Beschreibung des Problems hinzu.
4.  Fügen Sie ggf. das erwartete Verhalten (im Gegensatz zu einer Beschreibung des Problems) dem Feld **erwartetes Verhalten** hinzu.
5.  Fügen Sie eine ausführliche Beschreibung der Reproduktion des Problems im Feld **Reproduktions Schritte** hinzu.
6.  Klicken Sie abschließend auf die Schaltfläche **Speichern** .

### <a name="manually-adding-a-bug"></a>Manuelles Hinzufügen eines Fehlers

Dieser Prozess ist identisch mit dem Klicken auf " **fehl** geschlagen", mit Ausnahme der automatisch aufgefüllten Dropdown Liste. Wählen Sie in diesem Fall entweder den entsprechenden TCR-Fehlertyp aus, oder wählen Sie ein **\* \* nicht-TR-Problem \* \*** für Fehler aus, die außerhalb des TR-Bereichs liegen, aber trotzdem gemeldet werden sollen.

## <a name="resources"></a>Ressourcen

<dl> <dt>

<span id="Games_for_Windows__Technical_Requirements"></span><span id="games_for_windows__technical_requirements"></span><span id="GAMES_FOR_WINDOWS__TECHNICAL_REQUIREMENTS"></span>Spiele für Windows: technische Anforderungen
</dt> <dd>

[Spiele für technische Windows-Anforderungen: bewährte Methoden für Spiele unter Windows XP, Windows Vista und Windows 7](./games-for-windows-technical-requirements-1-1-0006.md)

</dd> <dt>

<span id="Windows_SDK"></span><span id="windows_sdk"></span><span id="WINDOWS_SDK"></span>Windows SDK
</dt> <dd>

[Windows sdche](https://msdn.microsoft.com/bb980924.aspx)

</dd> <dt>

<span id="User_Account_Control_Guidelines"></span><span id="user_account_control_guidelines"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES"></span>Richtlinien für die Benutzerkontensteuerung
</dt> <dd>

[Windows Vista-Anwendungs Entwicklungsanforderungen für die Kompatibilität mit der Benutzerkontensteuerung](/previous-versions/dotnet/articles/bb530410(v=msdn.10))

</dd> <dt>

<span id="Windows_Installer_Information"></span><span id="windows_installer_information"></span><span id="WINDOWS_INSTALLER_INFORMATION"></span>Windows Installer Informationen
</dt> <dd>

[Windows Installer](../msi/windows-installer-portal.md)

</dd> <dt>

<span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>Winqual-Entwickler Portal 
</dt> <dd>

[Windows Quality Online Services (Winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)

</dd> <dt>

<span id="DirectX_Developer_Portal"></span><span id="directx_developer_portal"></span><span id="DIRECTX_DEVELOPER_PORTAL"></span>DirectX-Entwickler Portal
</dt> <dd>

[DirectX-Entwickler Center](/previous-versions/windows/apps/hh452744(v=win.10))

</dd> <dt>

<span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog zu spielen für Windows und DirectX SDK
</dt> <dd>

[Spiele für Windows und das DirectX SDK](https://walbourn.github.io/)

</dd> <dt>

<span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Weitere DirectX-Artikel
</dt> <dd>

[Technische Artikel zu DirectX](./dx9-technical-articles.md)

</dd> </dl>

 

