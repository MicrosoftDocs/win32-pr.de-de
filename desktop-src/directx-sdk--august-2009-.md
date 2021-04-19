---
description: Ab Windows 8 ist das DirectX SDK als Teil der Windows SDK enthalten.
ms.assetid: d8765da9-e7cf-47e8-8bc3-4b29162da41b
title: Wo finde ich das DirectX SDK?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c070313c5c7f6105afaf7b629ff1ca2618a469fb
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314623"
---
# <a name="where-is-the-directx-sdk"></a>Wo finde ich das DirectX SDK?

Ab Windows 8 ist das DirectX SDK als Teil der Windows SDK enthalten.

Wir haben das DirectX SDK ursprünglich als hochleistungsfähige Plattform für die Spieleentwicklung auf Windows erstellt. Da DirectX-Technologien ausgereift sind, wurden Sie für eine größere Anzahl von Anwendungen relevant. Heute werden bei der Verfügbarkeit von Direct3D-Hardware auf Computern sogar herkömmliche Desktop Anwendungen für die Beschleunigung der Grafikhardware eingesetzt. Parallel sind DirectX-Technologien stärker in Windows integriert. DirectX ist nun ein grundlegender Bestandteil von Windows.

Da das Windows SDK das primäre SDK für Windows-Entwickler ist, enthält es jetzt auch DirectX. Nutzen Sie das Windows SDK ab sofort zum Entwickeln großartiger Spiele für Windows. Informationen zum Herunterladen des Windows 8. x SDK oder des Windows 10 SDK finden Sie unter [Windows SDK und Emulator Archive](https://developer.microsoft.com/windows/downloads/sdk-archive).

Die folgenden Technologien und Tools, ehemals Teil des DirectX SDK, sind jetzt Teil des Windows SDK.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Technologie oder Tool</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Windows_Graphics_Components"></span><span id="windows_graphics_components"></span><span id="WINDOWS_GRAPHICS_COMPONENTS"></span>Windows-Grafik Komponenten<br/></td>
<td>Die Header und Bibliotheken für <a href="/windows/desktop/direct3d">Direct3D</a> und andere Windows-Grafik-APIs, wie <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a>, sind im Windows SDK verfügbar. <br/>
<blockquote>
[!Note]<br />
Die veralteten D3DX9/d3dx10/Bibliothek d3dx11-Hilfsprogrammbibliotheken sind über <a href="https://www.nuget.org/packages/Microsoft.DXSDK.D3DX">nuget</a>verfügbar. es gibt jedoch auch eine Reihe von <a href="https://walbourn.github.io/living-without-d3dx/">Open Source-Alternativen</a>. Die D3DCSX DirectCompute Utility Library und die verteilbare dll sind im Windows SDK verfügbar. D3DX12 ist auf <a href="https://github.com/microsoft/DirectX-Headers">GitHub</a>verfügbar.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="HLSL_compiler__FXC.EXE_"></span><span id="hlsl_compiler__fxc.exe_"></span><span id="HLSL_COMPILER__FXC.EXE_"></span>HLSL-Compiler (FXC.EXE)<br/></td>
<td>Der <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL</a> -Compiler ist ein Tool im entsprechenden Architektur Unterverzeichnis im Ordner "bin" in der Windows SDK.<br/>
<blockquote>
[!Note]<br />
Die D3DCompiler-API und die verteilbare dll sind im Windows SDK verfügbar.
</blockquote>
<br/><br/>Verwenden Sie für die Entwicklung von DirectX 12 den dxcompiler in der Windows SDK und auf [GitHub](https://github.com/Microsoft/DirectXShaderCompiler)gehostet.
<br/></td>
</tr>
<tr class="odd">
<td><span id="PIX_for_"></span><span id="pix_for_"></span><span id="PIX_FOR_"></span>Pix für Windows<br/></td>
<td>Ein Ersatz für das PIX für Windows-Tool ist jetzt eine Funktion in Microsoft Visual Studio, die als Visual Studio-Grafik Debugger bezeichnet wird. Diese Funktion bietet eine stark verbesserte Benutzerfreundlichkeit, Unterstützung für Windows 8 und Direct3D 11,1 sowie die Integration in herkömmliche Microsoft Visual Studio Features, wie z. b. Aufruf Listen und Debuggingfenster für das <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL</a> -Debugging. Weitere Informationen zu dieser neuen Funktion finden Sie unter <a href="/visualstudio/debugger/visual-studio-graphics-diagnostics?view=vs-2015">Debuggen von DirectX-Grafiken</a>.<br/><br/>Informationen zur Entwicklung von DirectX 12 finden Sie unter der neuesten Generation von <a href="https://devblogs.microsoft.com/pix/">pix unter Windows</a> .<br/></td>
</tr>
<tr class="even">
<td><span id="XAudio2_for_"></span><span id="xaudio2_for_"></span><span id="XAUDIO2_FOR_"></span><a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> für Windows<br/></td>
<td>Die <a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> -API ist jetzt eine Systemkomponente in Windows 8. x und Windows 10. Die Header und Bibliotheken für XAudio2 sind im Windows SDK verfügbar. Informationen zur Unterstützung von Windows 7 finden Sie unter <a href="/windows/win32/xaudio2/xaudio2-redistributable">XAudio2Redist</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="XInput_for_"></span><span id="xinput_for_"></span><span id="XINPUT_FOR_"></span><a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">Xinput</a> für Windows<br/></td>
<td>Die <a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">xinput</a> 1,4-API ist jetzt eine Systemkomponente in Windows 8. x und Windows 10. Die Header und Bibliotheken für xinput sind im Windows SDK verfügbar.<br/>
<blockquote>
[!Note]<br />
Ältere xinput-9.1.0 ist auch als Teil von Windows 7 oder höher verfügbar.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="XNAMATH"></span><span id="xnamath"></span>Xnamath<br/></td>
<td>Die neueste Version von xnamath, die sowohl für neue Anweisungs Sätze als auch für Arm/ARM64 aktualisiert wird, ist jetzt <a href="/windows/desktop/dxmath/directxmath-portal">directxmath</a>. Die Header für directxmath sind im Windows SDK und auf <a href="https://github.com/Microsoft/DirectXMath">GitHub</a>verfügbar.<br/></td>
</tr>
<tr class="odd">
<td><span id="DirectX_Control_Panel_and_DirectX_Capabilities_Viewer"></span><span id="directx_control_panel_and_directx_capabilities_viewer"></span><span id="DIRECTX_CONTROL_PANEL_AND_DIRECTX_CAPABILITIES_VIEWER"></span>DirectX-Systemsteuerung und DirectX-Funktionen-Viewer<br/></td>
<td>Die DirectX-Systemsteuerung und die DirectX-Funktionen-Viewer-Hilfsprogramme sind im entsprechenden Architektur-Unterverzeichnis im Ordner bin im Windows SDK enthalten. Der DirectX-Funktionen-Viewer ist auch auf <a href="https://github.com/microsoft/DxCapsViewer">GitHub</a>verfügbar.<br/></td>
</tr>
<tr class="even">
<td><span id="XACT"></span><span id="xact"></span>XACT<br/></td>
<td>Das Xbox audiocross Platform-Tool (XACT) wird für die Verwendung unter Windows nicht mehr unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><span id="Games_Explorer_and_GDFMAKER"></span><span id="games_explorer_and_gdfmaker"></span><span id="GAMES_EXPLORER_AND_GDFMAKER"></span><a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">Spiele-Explorer</a> und gdfmaker<br/></td>
<td>Die <a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">Spiele-Explorer</a> -API stellt den Benutzern von Windows Spiele vor. Die Games Explorer-API wird nur unter Windows Vista und Windows 7 unterstützt. Verwenden Sie das Tool "Games Definition File Maker" (GDFMAKER.EXE), um Spiel Bewertungen für Windows Store-Apps zu deklarieren. <br/> Das Datei Erstellungs Tool für Spiel Definitionen (GDFMaker.exe) ist im Unterverzeichnis "bin" im Ordner "bin" im Windows SDK enthalten und unterstützt sowohl Windows Store-Apps als auch Win32-Desktop Anwendungen.<br/>
<br/></td>
</tr>
<tr class="even">
<td><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span>Beispiele<br/></td>
<td>Beispielanwendungen, die DirectX 12-Technologien unter Windows im <a href="https://github.com/Microsoft/DirectX-Graphics-Samples">DirectX</a> -beispielrepository hervorheben, finden Sie hier. Die meisten Beispiele für ältere Versionen von Direct3D sind auch online verfügbar. Weitere Informationen zu diesen Beispielen finden Sie unter <a href="https://walbourn.github.io/directx-sdk-samples-catalog/">DirectX SDK Samples Catalog</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="Managed_DirectX_1.1"></span><span id="managed_directx_1.1"></span><span id="MANAGED_DIRECTX_1.1"></span>Verwaltetes DirectX 1,1<br/></td>
<td>Die .net DirectX-Assemblys sind veraltet und werden nicht für die Verwendung durch neue Anwendungen empfohlen. Es stehen eine Reihe von Alternativen zur Verfügung. Siehe <a href="https://walbourn.github.io/directx-and-net/">DirectX und .net</a>. <br/></td>
</tr>
</tbody>
</table>



 

Das Legacy-DirectX-SDK steht bei Bedarf im [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkId=226640) zum Download zur Verfügung, aber es wird nicht empfohlen, für neue Projekte zu verwenden.

> [!Note]  
> Das DirectX SDK kann nicht installiert werden, wenn Sie eine bestimmte Version des verteilbaren Pakets Visual C++ 2010 bereits installiert haben. Weitere Informationen zu und eine Lösung zur Behebung dieses Problems finden Sie unter ["S1023"-Fehler bei der Installation des DirectX SDK (Juni 2010)](https://support.microsoft.com/kb/2728613).

 

## <a name="using-directx-sdk-projects-with-visual-studio"></a>Verwenden von DirectX SDK-Projekten mit Visual Studio

Die Beispiele aus dem DirectX SDK vom Juni 2010 werden mit den Premium-Visual Studio-SKUs (Microsoft Visual Studio Professional 2012, Microsoft Visual Studio Ultimate 2012, Microsoft Visual Studio Professional 2013 oder Microsoft Visual Studio Ultimate 2013) unter Windows 7 und Windows 8 und höheren Versionen unterstützt. Aufgrund des Übergangs von DirectX-Headern und-Bibliotheken in den Windows SDK sind Änderungen an den Projekteinstellungen erforderlich, um diese Beispiele ordnungsgemäß zu erstellen, wenn das Windows 8 SDK und spätere Versionen mit den Premium-SKUs von Visual Studio verpackt werden.

Diese Schritte gelten auch für Ihre eigenen Projekte, die vom DirectX SDK abhängig sind.

1.  Stellen Sie sicher, dass die Version vom Juni 2010 des DirectX SDK auf dem Entwicklungs Computer installiert ist. Wenn Sie auf einem Computer installieren, auf dem Windows 8 und höher ausgeführt wird, werden Sie aufgefordert, .NET 3,5 als erforderliche Installation für das DirectX SDK zu aktivieren.

    > [!Note]  
    > Das DirectX SDK kann nicht installiert werden, wenn Sie eine bestimmte Version des verteilbaren Pakets Visual C++ 2010 bereits installiert haben. Weitere Informationen zu und eine Lösung zur Behebung dieses Problems finden Sie unter ["S1023"-Fehler bei der Installation des DirectX SDK (Juni 2010)](https://support.microsoft.com/kb/2728613).

     

2.  Stellen Sie sicher, dass Sie eine der Premium-SKUs von Visual Studio verwenden. Microsoft Visual Studio Express 2012 für Windows 8 oder Microsoft Visual Studio Express 2013 für Windows erstellt keine Windows 8 und spätere Desktop Anwendungen, wie z. b. die DirectX SDK-Beispiele. Um eine der Premium-SKUs von Visual Studio zu installieren, wechseln Sie zu [Visual Studio-Downloads](https://www.microsoft.com/visualstudio/11/downloads) , und befolgen Sie die Anweisungen.

3.  Verwenden Sie den DirectX SDK-Beispiel Browser, um die Projektdateien für das gewünschte Beispiel zu installieren. Öffnen Sie die Microsoft Visual Studio 2010 kompatible Projektmappendatei (mit dem Suffix **\_ 2010**).

4.  Wenn Sie das Beispiel auf einem System öffnen, auf dem nur Microsoft Visual Studio 2012 oder Microsoft Visual Studio 2013 installiert ist, erhalten Sie die folgende Meldung: "Diese Lösung enthält ein oder mehrere Projekte, die eine frühere Version von VC + +-Compiler und-Bibliotheken verwenden. Jedes Projekt kann so aktualisiert werden, dass der VC + +-Compiler und-Bibliotheken (v110) verwendet werden. " Wählen Sie in diesem Dialogfeld die Option **Aktualisieren** aus, um das Projekt zu aktualisieren, bevor Sie das Projekt öffnen.

    Andernfalls können Sie den Compiler und die Bibliotheken von Visual Studio 2012 oder Visual Studio 2013 C++ 11 aktualisieren, nachdem diese geladen wurden. Klicken Sie hierzu mit der rechten Maustaste auf die Projekt Mappe, und wählen Sie **VC + +-Projekte aktualisieren** aus.

5.  D3DX wird nicht als kanonische API für die Verwendung von Direct3D in Windows 8 und höher betrachtet und ist daher nicht in der entsprechenden Windows SDK enthalten. Untersuchen alternativer Lösungen für die Arbeit mit der Direct3D-API. Für Legacy Projekte, wie z. b. die Windows 7 (und frühere) DirectX SDK-Beispiele, sind die folgenden Schritte erforderlich, um mit dem DirectX SDK Anwendungen mit D3DX zu erstellen:

    1.  Ändern Sie die **VC + +** -Verzeichnisse des Projekts wie folgt, um die richtige Reihenfolge für SDK-Header und-Bibliotheken zu verwenden.

        <dl> i. Öffnen Sie die **Eigenschaften** für das Projekt, und wählen Sie die Seite **VC + +-Verzeichnisse** aus.  
        ii. Wählen Sie **alle Konfigurationen und alle Plattformen** aus.  
        iii. Legen Sie diese Verzeichnisse wie folgt fest:

        -   Ausführbare Verzeichnisse: **<inherit from parent or project defaults>** (auf der rechten Seite Dropdown)
        -   **Includeverzeichnisse: $ (INCLUDEPATH); $ (dxsdk \_ dir) include**
        -   Bibliotheks Verzeichnisse einschließen: **$ (LibraryPath); $ (dxsdk \_ dir) lib \\ x86**

          
        iv. Klicken Sie auf **Anwenden**.  
        v. Wählen Sie die **x64-Plattform** aus.  
        vi. Legen Sie das **Bibliotheksverzeichnis** wie folgt fest:

        -   Bibliotheks Verzeichnisse: **$ (LibraryPath); $ (dxsdk \_ dir) lib \\ x64**

          
        </dl>

    2.  Wenn "d3dx9. h", "d3dx10. h" oder "Bibliothek d3dx11. h" in Ihrem Projekt enthalten sind, müssen Sie zunächst "d3d9. h", "d3d10. h" und "dxgi. h" oder "d3d11. h" und "dxgi. h" explizit einbeziehen, um sicherzustellen, dass Sie die neuere Version auswählen. Sie können die **Warnung C4005** bei Bedarf deaktivieren. Diese Warnung weist jedoch darauf hin, dass Sie die ältere Version dieser Header verwenden.
    3.  Entfernen Sie alle Verweise auf "dxgitype. h" in Ihrem Projekt. Dieser Header ist nicht im Windows SDK vorhanden, und die DirectX SDK-Version steht in Konflikt mit der neuen Winerror. h.
    4.  Alle D3DX-DLLs werden von der DirectX SDK-Installation auf dem Entwicklungs Computer installiert. Stellen Sie sicher, dass die erforderlichen D3DX-Abhängigkeiten mit einem beliebigen Beispiel oder mit der Anwendung neu verteilt werden, wenn Sie auf einen anderen Computer verschoben wird.
    5.  Beachten Sie, dass die Ersetzungs Technologien für die aktuelle Verwendung von Bibliothek d3dx11 [directxtex](https://github.com/Microsoft/DirectXTex), [directxtk](https://github.com/Microsoft/DirectXTK), [directxmesh](https://github.com/Microsoft/DirectXMesh)und [uvatlas](https://github.com/Microsoft/UVAtlas)enthalten. D3DXMath wird durch [directxmath](./dxmath/directxmath-portal.md)ersetzt.

6.  Stellen Sie sicher, dass Sie die neue Version des HLSL-Shader-Compilers verwenden, indem Sie die folgenden Bedingungen beachten:

    1.  Wenn das ausführbare Verzeichnis gemäß Schritt 5 geändert wird, werden die Projekt Builds FXC aus der Windows SDK Installation verwenden. Beachten Sie, dass HLSL-Dateien nun offiziell von Visual Studio erkannt werden. Sie können Sie als Projektdateien hinzufügen und Compileroptionen über das Projekt System festlegen.

    2.  Wenn Sie die Lauf Zeit Kompilierung über die Legacy-D3DX-DLL aufrufen, wird die falsche ältere Version des HLSL-Compilers verwendet. Ersetzen Sie alle Verweise auf D3DXCompile \* -, D3DX10Compile \* -und D3DX11Compile- \* APIs in Ihrem Code durch die D3DCompile-Funktion in D3DCOMPILER \_46.DLL oder D3DCOMPILER \_47.DLL.

    3.  Jedes Projekt, das die Laufzeit-Shader-Kompilierung verwendet, muss über D3DCOMPILER \_xx.DLL in den lokalen Pfad der ausführbaren Datei für das Projekt kopiert werden. Diese dll ist in diesem Unterverzeichnis der Windows SDK-Installation unter **% Program Files (x86)% \\ Windows Kits \\ 8,0 \\ Redist \\ D3D \\ <arch>** oder **% Program Files (x86)% \\ Windows Kits \\ 8,1 \\ Redist \\ D3D \\ <arch>** verfügbar, wobei **<arch>** **x86** und **x64** ist.

        Der D3DCOMPILER \_46.DLL-oder D3DCOMPILER \_ -47.DLL aus dem Windows SDK ist keine Systemkomponente und sollte nicht in das Windows-System Verzeichnis kopiert werden. Sie können diese DLL mit Ihrer Anwendung als parallele dll an andere Computer verteilen.

7.  Jedes Projekt, das die xinput-API verwendet und für die Ausführung unter Windows 7 oder einer älteren Windows-Version vorgesehen ist, muss entweder die Legacy Version (9.1.0) verwenden oder die Header und Bibliotheken für diese Komponente explizit aus dem DirectX SDK einschließen. Der xinput-Header und xinput. LIB, die in der Windows SDK enthalten ist, nur auf die Version (1,4) abzielen, die als Teil von Windows 8 und höher ausgeliefert wird. Der gleiche Header kann mit XINPUT9 \_ 1 \_ 0. lib verwendet werden, um die Legacy Version zu verwenden, die in älteren Versionen von Windows enthalten ist. Die Legacy Version von xinput erkennt keine vollständigen Funktionen oder unterstützt Controller-integrierte Audiodaten. wenn die Unterstützung für diese Features erforderlich ist, müssen Sie daher die DirectX SDK-Version (1,3) verwenden.

    Um die voll ausgestattete xinput-API mit vollem Funktionsumfang zu verwenden, sollten Sie `#include` die spezifischen xinput-Header aus dem DirectX SDK direkt verwenden:

    `#include <%DXSDK_DIR%Include\xinput.h>`

    ... und in den Linkeroptionen für zusätzliche Abhängigkeiten direkt mit der DirectX SDK-xinput-Bibliothek verknüpfen:

    **% Dxsdk \_ dir% include \\ <arch> \\ xinput. lib**

    Die \_ Binärdatei XINPUT13.DLL wird von der DirectX SDK-Installation auf dem Entwicklungs Computer in den Windows-Systemverzeichnissen installiert. Sie müssen diese Binärdatei mit Ihrer Anwendung neu verteilen, indem Sie die DirectX-Setup Installation aus dem DirectX SDK verwenden.

8.  Jedes Projekt, das die XAudio2-API verwendet und für die Ausführung unter Windows 7 oder einer älteren Windows-Version vorgesehen ist, muss entweder die ältere Version (9.1.0) verwenden oder die Header und Bibliotheken für diese Komponente explizit aus dem DirectX SDK einschließen. Die XAudio2-Header und-Bibliotheken, die in der Windows SDK enthalten sind, Zielen nur auf die Version (2,8) ab, die als Teil von Windows 8 enthalten ist.

    Mit XAudio2 sollten Sie z. b. `#include` die spezifischen XAudio2-Header aus dem DirectX SDK direkt ausführen:

    `  #include <%DXSDK_DIR%Include\xaudio2.h> `

    ... und in den Linkeroptionen für zusätzliche Abhängigkeiten direkt mit der DirectX SDK-XAudio2-Bibliothek verknüpfen:

    **% Dxsdk \_ dir% include \\ <arch> \\ xaudio2. lib**

    Die \_ Binärdatei XAUDIO27.DLL wird von der DirectX SDK-Installation auf dem Entwicklungs Computer in den Windows-Systemverzeichnissen installiert. Sie müssen diese Bibliotheken mithilfe der DirectX-Setup Installation aus dem DirectX SDK mit Ihrer Anwendung neu verteilen.

9.  Wenn Sie das DirectX SDK mit früheren Versionen von Visual Studio verwendet haben, wurde das Visual Studio 2010-Upgrade möglicherweise den DirectX SDK-Pfad in Ihre Standard Projekteinstellungen migriert. Es wird empfohlen, diese Einstellungen zu entfernen, um zukünftige Buildfehler zu vermeiden. Ändern Sie im Verzeichnis " **% User Profile% \\ AppData \\ local \\ Microsoft \\ MSBuild \\ v 4.0** " die Dateien " **Microsoft. cpp. Win32. User** " und " **Microsoft. cpp. x64. User** ", um alle Verweise auf dxsdk-Verzeichnispfade zu entfernen \_ . Alternativ können Sie den gesamten Knoten entfernen <PropertyGroup> , der die Pfad Einträge enthält, z <ExecutablePath> . b. und, um <IncludePath> zu Standard Standardwerten zurückzukehren. Wenn in diesen Dateien keine Verweise auf dxsdk-dir angezeigt werden \_ , sind keine Änderungen erforderlich.

10. Wenn die resultierende APP Windows Vista mit Service Pack 2 (SP2) sowie Windows 7 und Windows 8 und höher unterstützt, legen Sie die Präprozessordefinition namens **\_ Win32 \_ Winnt** auf 0x600 fest. Wenn nur Windows 7 und Windows 8 und höher unterstützt werden, legen Sie es auf 0x601 fest.

    Beispiel:

    1.  Öffnen Sie die **Eigenschaften** für das Projekt, und wählen Sie **C/C++**-  >  **Präprozessor** aus.
    2.  Wählen Sie **alle Konfigurationen** und **alle Plattformen** aus.
    3.  Wechseln Sie zum Abschnitt mit den **Präprozessordefinitionen** , und legen Sie \_ Win32 \_ Winnt = 0x600 fest.
    4.  Klicken Sie auf **Anwenden**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Spiele für Windows und das DirectX SDK**
</dt> <dt>

[Wo ist das DirectX SDK (2021 Edition)?](https://walbourn.github.io/where-is-the-directx-sdk-2021-edition/)
</dt> <dt>

[DirectX-sdche eines bestimmten Alters](https://walbourn.github.io/directx-sdks-of-a-certain-age/)
</dt> <dt>

[Leben ohne D3DX](https://walbourn.github.io/living-without-d3dx/)
</dt> </dl> 
