---
description: Ab Windows 8 ist das DirectX SDK als Teil des Windows SDK enthalten.
ms.assetid: d8765da9-e7cf-47e8-8bc3-4b29162da41b
title: Wo finde ich das DirectX SDK?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d46559e839abea9d6e0c89ab7e5940e46b2d4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886453"
---
# <a name="where-is-the-directx-sdk"></a>Wo finde ich das DirectX SDK?

Ab Windows 8 ist das DirectX SDK als Teil des Windows SDK enthalten.

Wir haben das DirectX SDK ursprünglich als Hochleistungsplattform für die Spieleentwicklung auf grundlage Windows erstellt. Mit zunehmender Reife von DirectX-Technologien wurden sie für eine größere Palette von Anwendungen relevant. Heutzutage steuert die Verfügbarkeit von Direct3D-Hardware auf Computern sogar herkömmliche Desktopanwendungen, um die Grafikhardwarebeschleunigung zu verwenden. Parallel dazu sind DirectX-Technologien stärker in Windows integriert. DirectX ist jetzt ein grundlegender Bestandteil Windows.

Da das Windows SDK das primäre SDK für Windows-Entwickler ist, enthält es jetzt auch DirectX. Nutzen Sie das Windows SDK ab sofort zum Entwickeln großartiger Spiele für Windows. Informationen zum Herunterladen des Windows 8.x SDK oder Windows 10 SDK finden Sie unter [Windows SDK und Emulatorarchiv.](https://developer.microsoft.com/windows/downloads/sdk-archive)

Die folgenden Technologien und Tools, früher Teil des DirectX SDK, sind jetzt Teil des Windows SDK.


| Technologie oder Tool | Beschreibung | 
|--------------------|-------------|
| <span id="Windows_Graphics_Components"></span><span id="windows_graphics_components"></span><span id="WINDOWS_GRAPHICS_COMPONENTS"></span>Windows Grafikkomponenten<br /> | Die Header und Bibliotheken für <a href="/windows/desktop/direct3d">Direct3D</a> und andere Windows Grafik-APIs wie <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a>sind im Windows SDK verfügbar. <br /><blockquote>[!Note]<br />Die veralteten Hilfsprogrammbibliotheken D3DX9/D3DX10/D3DX11 sind über <a href="https://www.nuget.org/packages/Microsoft.DXSDK.D3DX">NuGet</a>verfügbar, es gibt jedoch auch eine Reihe von <a href="https://walbourn.github.io/living-without-d3dx/">Open Source-Alternativen.</a> Die Hilfsprogrammbibliothek D3DCSX DirectCompute und die verteilbare DLL sind im Windows SDK verfügbar. D3DX12 ist auf <a href="https://github.com/microsoft/DirectX-Headers">GitHub</a>verfügbar.</blockquote><br /> | 
| <span id="HLSL_compiler__FXC.EXE_"></span><span id="hlsl_compiler__fxc.exe_"></span><span id="HLSL_COMPILER__FXC.EXE_"></span>HLSL-Compiler (FXC.EXE)<br /> | Der <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL-Compiler</a> ist ein Tool im entsprechenden Architekturunterverzeichnis unter dem Ordner bin im Windows SDK.<br /><blockquote>[!Note]<br />Die D3DCompiler-API und die verteilbare DLL sind im Windows SDK verfügbar.</blockquote><br /><br />Verwenden Sie für die DirectX 12-Entwicklung den DXCompiler im Windows SDK, der auf [GitHub](https://github.com/Microsoft/DirectXShaderCompiler)gehostet wird.<br /> | 
| <span id="PIX_for_"></span><span id="pix_for_"></span><span id="PIX_FOR_"></span>PIX für Windows<br /> | Ein Ersatz für das PIX für Windows Tool ist jetzt ein Feature in Microsoft Visual Studio, das als Visual Studio Grafikdebugger bezeichnet wird. Dieses Feature hat die Benutzerfreundlichkeit, die Unterstützung für Windows 8 und Direct3D 11.1 sowie die Integration mit herkömmlichen Microsoft Visual Studio Features wie Aufruflisten und Debugfenstern für <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">hlsl-Debuggen</a> erheblich verbessert. Weitere Informationen zu diesem neuen Feature finden Sie unter <a href="/visualstudio/debugger/visual-studio-graphics-diagnostics?view=vs-2015">Debuggen von DirectX-Grafiken.</a><br /><br />Informationen zur DirectX 12-Entwicklung finden Sie in der neuesten Generation von <a href="https://devblogs.microsoft.com/pix/">PIX auf Windows</a><br /> | 
| <span id="XAudio2_for_"></span><span id="xaudio2_for_"></span><span id="XAUDIO2_FOR_"></span><a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> für Windows<br /> | Die <a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2-API</a> ist jetzt eine Systemkomponente in Windows 8.x und Windows 10. Die Header und Bibliotheken für XAudio2 sind im Windows SDK verfügbar. Informationen zur Unterstützung Windows 7 finden Sie unter <a href="/windows/win32/xaudio2/xaudio2-redistributable">XAudio2Redist</a>.<br /> | 
| <span id="XInput_for_"></span><span id="xinput_for_"></span><span id="XINPUT_FOR_"></span><a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">XInput</a> für Windows<br /> | Die <a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">XInput</a> 1.4-API ist jetzt eine Systemkomponente in Windows 8.x und Windows 10. Die Header und Bibliotheken für XInput sind im Windows SDK verfügbar.<br /><blockquote>[!Note]<br />Legacy-XInput 9.1.0 ist auch als Teil von Windows 7 oder höher verfügbar.</blockquote><br /> | 
| <span id="XNAMATH"></span><span id="xnamath"></span>XNAMATH<br /> | Die neueste Version von XNAMATH, die für neue Anweisungssätze sowie ARM/ARM64 aktualisiert wird, ist jetzt <a href="/windows/desktop/dxmath/directxmath-portal">DirectXMath.</a> Die Header für DirectXMath sind im Windows SDK und auf <a href="https://github.com/Microsoft/DirectXMath">GitHub</a>verfügbar.<br /> | 
| <span id="DirectX_Control_Panel_and_DirectX_Capabilities_Viewer"></span><span id="directx_control_panel_and_directx_capabilities_viewer"></span><span id="DIRECTX_CONTROL_PANEL_AND_DIRECTX_CAPABILITIES_VIEWER"></span>DirectX Systemsteuerung und DirectX Capabilities Viewer<br /> | Die Hilfsprogramme DirectX Systemsteuerung und DirectX Capabilities Viewer sind im entsprechenden Architekturunterverzeichnis unter dem Ordner bin im Windows SDK enthalten. DirectX Capabilities Viewer ist auch auf <a href="https://github.com/microsoft/DxCapsViewer">GitHub</a>verfügbar.<br /> | 
| <span id="XACT"></span><span id="xact"></span>XACT<br /> | Das Plattformübergreifende Xbox Audio-Tool (XACT) wird für die Verwendung auf Windows nicht mehr unterstützt.<br /> | 
| <span id="Games_Explorer_and_GDFMAKER"></span><span id="games_explorer_and_gdfmaker"></span><span id="GAMES_EXPLORER_AND_GDFMAKER"></span><a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">Games Explorer</a> und GDFMAKER<br /> | Die <a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">Spiele-Explorer-API</a> stellt Spiele für Benutzer von Windows dar. Die Games Explorer-API wird nur für Windows Vista und Windows 7 unterstützt. Verwenden Sie das Game Definition File Maker-Tool (GDFMAKER.EXE), um Spielbewertungen für Windows Store Apps zu deklarieren. <br /> Das Game Definition File Maker-Tool (GDFMaker.exe) ist im Unterverzeichnis x86 unter dem Ordner bin im Windows SDK enthalten und unterstützt sowohl Windows Store-Apps als auch Win32-Desktopanwendungen.<br /><br /> | 
| <span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span>Beispiele<br /> | Beispielanwendungen, die DirectX 12-Technologien auf Windows hervorheben, finden Sie im Repository mit <a href="https://github.com/Microsoft/DirectX-Graphics-Samples">DirectX-Beispielen.</a> Die meisten Beispiele für ältere Versionen von Direct3D sind auch online verfügbar. Weitere Informationen zu diesen Beispielen finden Sie unter <a href="https://walbourn.github.io/directx-sdk-samples-catalog/">DirectX SDK Samples Catalog</a>.<br /> | 
| <span id="Managed_DirectX_1.1"></span><span id="managed_directx_1.1"></span><span id="MANAGED_DIRECTX_1.1"></span>Managed DirectX 1.1<br /> | Die .NET DirectX-Assemblys sind veraltet und werden nicht für die Verwendung durch neue Anwendungen empfohlen. Es gibt eine Reihe von Alternativen. Weitere Informationen finden Sie unter <a href="https://walbourn.github.io/directx-and-net/">DirectX und .NET.</a> <br /> | 




 

Das Ältere DirectX SDK steht bei Bedarf aus dem [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkId=226640) zum Download zur Verfügung, die Verwendung für neue Projekte wird jedoch nicht empfohlen.

> [!Note]  
> Das DirectX SDK kann nicht installiert werden, wenn Sie bereits eine bestimmte Version des Visual C++ 2010 Redistributable Package installiert haben. Weitere Informationen zu und eine Lösung zum Beheben dieses Problems finden Sie unter [Fehler "S1023" beim Installieren des DirectX SDK (Juni 2010).](https://support.microsoft.com/kb/2728613)

 

## <a name="using-directx-sdk-projects-with-visual-studio"></a>Verwenden von DirectX SDK-Projekten mit Visual Studio

Die Beispiele aus dem DirectX SDK vom Juni 2010 werden mit Premium-SKUs für Visual Studio (Microsoft Visual Studio Professional 2012, Microsoft Visual Studio Ultimate 2012, Microsoft Visual Studio Professional 2013 oder Microsoft Visual Studio Ultimate 2013) am Windows 7 und der Windows 8 und höher unterstützt. Aufgrund des Übergangs von DirectX-Headern und -Bibliotheken in das Windows SDK sind Änderungen an den Projekteinstellungen erforderlich, um diese Beispiele ordnungsgemäß mit der Gepacktkeit des Windows 8 SDK und höher mit den PREMIUM Visual Studio-SKUs zu erstellen.

Diese Schritte gelten auch für Ihre eigenen Projekte, die vom DirectX SDK abhängig sind.

1.  Stellen Sie sicher, dass die Version vom Juni 2010 des DirectX SDK auf Ihrem Entwicklungscomputer installiert ist. Wenn Sie auf einem Computer installieren, auf dem Windows 8 und höher ausgeführt wird, werden Sie aufgefordert, .NET 3.5 als erforderliche Installation für das DirectX SDK zu aktivieren.

    > [!Note]  
    > Das DirectX SDK kann nicht installiert werden, wenn Sie bereits eine bestimmte Version des Visual C++ 2010 Redistributable Package installiert haben. Weitere Informationen zu und eine Lösung zum Beheben dieses Problems finden Sie unter [Fehler "S1023" beim Installieren des DirectX SDK (Juni 2010).](https://support.microsoft.com/kb/2728613)

     

2.  Stellen Sie sicher, dass Sie eine der Premium-Visual Studio-SKUs verwenden. Microsoft Visual Studio Express 2012 für Windows 8 oder Microsoft Visual Studio Express 2013 für Windows werden keine Windows 8 und spätere Desktopanwendungen wie directX SDK-Beispiele erstellt. Um eine der Premium-Visual Studio-SKUs zu installieren, wechseln Sie [zu: Visual Studio Downloads,](https://www.microsoft.com/visualstudio/11/downloads) und befolgen Sie die Anweisungen.

3.  Verwenden Sie den DirectX SDK-Beispielbrowser, um die Projektdateien für das gewünschte Beispiel zu installieren. Öffnen Sie die Microsoft Visual Studio 2010-kompatible Projektmappendatei des Beispiels (mit dem Suffix **\_ 2010).**

4.  Wenn Sie das Beispiel auf einem System öffnen, auf dem nur Microsoft Visual Studio 2012 oder Microsoft Visual Studio 2013 installiert ist, erhalten Sie die folgende Meldung: "Diese Projektmappe enthält mindestens ein Projekt mit einer früheren Version von VC++ Compiler und Bibliotheken. Jedes Projekt kann aktualisiert werden, um den VC++ Compiler und Bibliotheken (v110) zu verwenden." Wählen Sie in diesem Dialogfeld die Option **Aktualisieren** aus, die Aktualisiert werden soll, bevor Sie das Projekt öffnen.

    Andernfalls können Sie nach dem Laden auf die Visual Studio 2012 oder Visual Studio 2013 C++ 11-Compilers und -Bibliotheken aktualisieren, indem Sie mit der rechten Maustaste auf die Projektmappe klicken und **aktualisieren VC++ Projekte** auswählen.

5.  D3DX gilt nicht als kanonische API für die Verwendung von Direct3D in Windows 8 und höher und ist daher nicht im entsprechenden Windows SDK enthalten. Untersuchen Sie alternative Lösungen für die Arbeit mit der Direct3D-API. Für Ältere Projekte, z. B. die DirectX SDK-Beispiele Windows 7 (und früheren Versionen), sind die folgenden Schritte erforderlich, um Anwendungen mit D3DX mithilfe des DirectX SDK zu erstellen:

    1.  Ändern Sie die **VC++** Verzeichnisse des Projekts wie folgt, um die richtige Reihenfolge für SDK-Header und -Bibliotheken zu verwenden.

        <dl> i. Öffnen **Sie Eigenschaften** für das Projekt, und wählen Sie die Seite **VC++Verzeichnisse** aus.  
        ii. Wählen Sie **Alle Konfigurationen und Alle Plattformen aus.**  
        iii. Legen Sie diese Verzeichnisse wie folgt fest:

        -   Ausführbare Verzeichnisse: (Dropdown auf **<inherit from parent or project defaults>** der rechten Seite)
        -   Includeverzeichnisse: **$(IncludePath);$(DXSDK \_ DIR)Include**
        -   Include Library Directories: **$(LibraryPath);$(DXSDK \_ DIR)Lib \\ x86**

          
        iv. Klicken Sie auf **Übernehmen**.  
        v. Wählen Sie die **x64-Plattform aus.**  
        vi. Legen Sie das **Bibliotheksverzeichnis** wie folgt fest:

        -   Bibliotheksverzeichnisse: **$(LibraryPath);$(DXSDK \_ DIR)Lib \\ x64**

          
        </dl>

    2.  Wenn "d3dx9.h", "d3dx10.h" oder "d3dx11.h" in Ihrem Projekt enthalten sind, achten Sie darauf, dass Sie "d3d9.h", "d3d10.h" und "dxgi.h" oder "d3d11.h" und "dxgi.h" explizit einschließen, um sicherzustellen, dass Sie die neuere Version auswählen. Sie können die **Warnung C4005** bei Bedarf deaktivieren. Diese Warnung weist jedoch darauf hin, dass Sie die ältere Version dieser Header verwenden.
    3.  Entfernen Sie alle Verweise auf DXGIType.h in Ihrem Projekt. Dieser Header ist im Windows SDK nicht vorhanden, und die DirectX SDK-Version führt zu einem Konflikt mit der neuen Datei winerror.h.
    4.  Alle D3DX-DLLs werden von der DirectX SDK-Installation auf Ihrem Entwicklungscomputer installiert. Stellen Sie sicher, dass die erforderlichen D3DX-Abhängigkeiten mit jedem Beispiel oder mit Ihrer Anwendung neu verteilt werden, wenn sie auf einen anderen Computer verschoben werden.
    5.  Beachten Sie, dass Ersetzungstechnologien für die aktuelle Verwendung von D3DX11 [DirectXTex,](https://github.com/Microsoft/DirectXTex) [DirectXTK,](https://github.com/Microsoft/DirectXTK) [DirectXMesh](https://github.com/Microsoft/DirectXMesh)und [UVAtlas](https://github.com/Microsoft/UVAtlas)umfassen. D3DXMath wird durch [DirectXMath](./dxmath/directxmath-portal.md)ersetzt.

6.  Stellen Sie sicher, dass Sie die neue Version des HLSL-Shadercompiler verwenden, indem Sie die folgenden Bedingungen beachten:

    1.  Das Ändern des ausführbaren Verzeichnisses gemäß Schritt 5 bewirkt, dass Projektbuilds FXC aus der installation Windows SDK verwenden. Beachten Sie, dass HLSL-Dateien jetzt offiziell von Visual Studio erkannt werden. Sie können sie als Projektdateien hinzufügen und Compileroptionen über das Projektsystem festlegen.

    2.  Beim Aufrufen der Laufzeitkompilierung über die ältere D3DX-DLL wird die falsche ältere Version des HLSL-Compilers verwendet. Ersetzen Sie alle Verweise auf die D3DXCompile-, \* D3DX10Compile- \* und D3DX11Compile-APIs \* in Ihrem Code durch die D3DCompile-Funktion in D3DCOMPILER \_46.DLL oder D3DCOMPILER \_47.DLL.

    3.  Für jedes Projekt, das die Laufzeit-Shaderkompilierung verwendet, muss D3DCOMPILER \_xx.DLL in den lokalen ausführbaren Pfad für das Projekt kopiert werden. Diese DLL ist in diesem Unterverzeichnis der Windows SDK-Installation unter **%ProgramFiles(x86)% \\ Windows Kits \\ 8.0 \\ Redist \\ D3D \\ &lt; &gt; arch** oder **%ProgramFiles(x86)% \\ Windows Kits \\ 8.1 \\ Redist \\ D3D \\ &lt; &gt; arch** verfügbar, wobei **&lt; arch &gt;** **x86** und **x64** ist.

        Der D3DCOMPILER \_46.DLL oder D3DCOMPILER \_47.DLL aus dem Windows SDK ist keine Systemkomponente und sollte nicht in das Windows Systemverzeichnis kopiert werden. Sie können diese DLL an andere Computer verteilen, wobei Ihre Anwendung als dll-Datei nebeneinander verwendet wird.

7.  Jedes Projekt, das die XInput-API verwendet und auf Windows 7 oder älteren Versionen von Windows ausgeführt werden soll, muss entweder die Legacyversion (9.1.0) verwenden oder die Header und Bibliotheken für diese Komponente explizit aus dem DirectX SDK einschließen. Der XInput-Header und XINPUT. LIB, die im Windows SDK enthalten sind, ist nur auf die Version (1.4) ausgerichtet, die als Teil von Windows 8 und höher geliefert wird. Der gleiche Header kann mit XINPUT9 \_ 1 \_ 0.LIB verwendet werden, um die Legacyversion zu verwenden, die in älteren Versionen von Windows enthalten ist. Die Legacyversion von XInput erkennt keine vollständigen Funktionen oder unterstützt controllerintegriert Audio. Wenn also Unterstützung für diese Features erforderlich ist, müssen Sie die DirectX SDK-Version (1.3) verwenden.

    Um die vollständige Downlevel-XInput-API zu verwenden, sollten Sie `#include` die spezifischen XInput-Header aus dem DirectX SDK direkt verwenden:

    `#include <%DXSDK_DIR%Include\xinput.h>`

    ... Und verknüpfen Sie in den Linkeroptionen für Zusätzliche Abhängigkeiten direkt mit der XInput-Bibliothek des DirectX SDK:

    **%DXSDK \_ DIR%Include \\ &lt; arch &gt; \\ xinput.lib**

    Die \_ XINPUT1-3.DLL-Binärdatei wird von der DirectX SDK-Installation auf Ihrem Entwicklungscomputer in den Windows Systemverzeichnissen installiert. Sie müssen diese Binärdatei mit Ihrer Anwendung neu verteilen, indem Sie die DirectX-Setupinstallation aus dem DirectX SDK verwenden.

8.  Jedes Projekt, das die XAudio2-API verwendet und auf Windows 7 oder älteren Versionen von Windows ausgeführt werden soll, muss entweder die ältere Version (9.1.0) verwenden oder explizit die Header und Bibliotheken für diese Komponente aus dem DirectX SDK einschließen. Die im Windows SDK enthaltenen XAudio2-Header und -Bibliotheken sind nur auf die Version (2.8) ausgerichtet, die als Teil Windows 8 enthalten ist.

    Bei XAudio2 sollten Sie beispielsweise `#include` die spezifischen XAudio2-Header direkt aus dem DirectX SDK abrufen:

    `  #include <%DXSDK_DIR%Include\xaudio2.h> `

    ... Und verknüpfen Sie in den Linkeroptionen für Zusätzliche Abhängigkeiten direkt mit der XAudio2-Bibliothek des DirectX SDK:

    **%DXSDK \_ DIR%Include \\ &lt; arch &gt; \\ xaudio2.lib**

    Die \_ XAUDIO2-7.DLL-Binärdatei wird von der DirectX SDK-Installation auf Ihrem Entwicklungscomputer in den Windows Systemverzeichnissen installiert. Sie müssen diese Bibliotheken mit Ihrer Anwendung neu verteilen, indem Sie die DirectX-Setupinstallation aus dem DirectX SDK verwenden.

9.  Wenn Sie das DirectX SDK mit früheren Versionen von Visual Studio verwendet haben, wurde beim Upgrade von Visual Studio 2010 möglicherweise der DirectX SDK-Pfad in Ihre Standardprojekteinstellungen migriert. Es wird empfohlen, diese Einstellungen zu entfernen, um zukünftige Buildfehler zu vermeiden. Ändern Sie im Verzeichnis **%USERPROFILE% \\ AppData \\ Local Microsoft MSBuild \\ \\ \\ v4.0** die Dateien **Microsoft.Cpp.Win32.user** und **Microsoft.Cpp.x64.user,** um alle Verweise auf DXSDK \_ DIR-Pfade zu entfernen. Alternativ können Sie den gesamten &lt; PropertyGroup-Knoten entfernen, &gt; der die Pfadeinträge enthält, z. B. &lt; ExecutablePath und &gt; &lt; &gt; IncludePath, um die Standardstandardwerte wiezu kehren. Wenn in diesen Dateien keine Verweise auf DXSDK DIR angezeigt \_ werden, sind keine Änderungen erforderlich.

10. Wenn die resultierende App Windows Vista mit Service Pack 2 (SP2) sowie Windows 7 und Windows 8 und höher unterstützt, legen Sie die Präprozessordefinition **\_ win32 \_ WINNT** auf 0x600 fest. Wenn es nur Windows 7 und Windows 8 und höher unterstützt, legen Sie es auf 0x601 fest.

    Beispiel:

    1.  Öffnen **Sie Eigenschaften** für das Projekt, und wählen Sie **C/C++-Präprozessor**  >  aus.
    2.  Wählen Sie **Alle Konfigurationen** und **Alle Plattformen aus.**
    3.  Wechseln Sie zum Abschnitt **Präprozessordefinitionen,** und legen Sie \_ WIN32 \_ WINNT=0x600 fest.
    4.  Klicken Sie auf **Übernehmen**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Spiele für Windows und das DirectX SDK**
</dt> <dt>

[Wo befindet sich das DirectX SDK (2021 Edition)?](https://walbourn.github.io/where-is-the-directx-sdk-2021-edition/)
</dt> <dt>

[DirectX SDKs eines bestimmten Alters](https://walbourn.github.io/directx-sdks-of-a-certain-age/)
</dt> <dt>

[Leben ohne D3DX](https://walbourn.github.io/living-without-d3dx/)
</dt> </dl> 
