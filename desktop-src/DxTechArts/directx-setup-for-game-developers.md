---
title: DirectX-Installation für Spieleentwickler
description: In diesem Artikel werden einige häufig gestellte Fragen zur DirectX-Laufzeit und die Verwendung von DirectSetup zur Installation von DirectX behandelt.
ms.assetid: 2ab439be-8d99-bcf8-89af-d4274e044c88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9c0faf346bd8793e61a89128ce573e29b7a8267
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039468"
---
# <a name="directx-installation-for-game-developers"></a>DirectX-Installation für Spieleentwickler

In diesem Artikel werden einige häufig gestellte Fragen zur DirectX-Laufzeit und die Verwendung von DirectSetup zur Installation von DirectX behandelt.

-   [DirectX-Laufzeit](#directx-runtime)
-   [DirectX-Versionsnummer](#directx-version-number)
-   [DirectX-Bibliotheken](#directx-libraries)
-   [Installation von DirectX durch das Installationsprogramm des Spiels](#installation-of-directx-by-the-games-installer)
-   [Kleine Installationspakete](#small-installation-packages)
-   [Interne Bereitstellung der Debuggen DirectX-Laufzeit](#internal-deployment-of-the-debug-directx-runtime)

> [!IMPORTANT]
> Das Legacy-DirectX-SDK ist am Ende des Lebenszyklus, aber es ist immer noch verfügbar, um alte Spiele, Tutorials und Projekte zu unterstützen. In neuen Projekten sollte Sie nicht verwendet werden. Die Verwendung des Legacy-DirectX SDK erfordert die Verwendung des veralteten DirectSetup für Komponenten wie D3DX9, d3dx10, Bibliothek d3dx11, xaudio2,7, xinput 1,3 und Xact. Weitere Informationen zum aktuellen Status des DirectX SDK finden Sie unter [wo ist das DirectX SDK?](../directx-sdk--august-2009-.md)und im Blogbeitrag [nicht so direkt Setup](https://walbourn.github.io/not-so-direct-setup/).

## <a name="directx-runtime"></a>DirectX-Laufzeit

Die DirectX-Laufzeit besteht aus Kernkomponenten und optionalen Komponenten.

Die Kernkomponenten, z. b. Direct3D und DirectInput, werden als Teil des Betriebssystems betrachtet. Die Kernkomponenten für DirectX 9.0 c wurden seit dem DirectX SDK Summer 2004-Update nicht geändert, und Sie entsprechen denen, die mit Microsoft Windows XP SP2, Windows XP Pro x64 Edition und Windows Server 2003 SP1 veröffentlicht wurden. Windows Vista umfasst DirectX 10, das das Windows-Anzeigetreiber Modell (WDDM) und Direct3D 10. x unterstützt. Windows 7 und Windows Vista (siehe [KB971644](https://support.microsoft.com/kb/971644)) unterstützen DirectX 11, das Direct3D 11, Direct2D, DirectWrite, das WARP10-softwarrenderinggerät und die 10level9-Funktionsebenen unterstützt. Weitere Informationen finden Sie [unter Grafik-APIs in Windows](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista) .

Die optionalen Komponenten werden in Updates des DirectX SDK veröffentlicht und enthalten D3DX, XACT, XAudio2, xinput, Managed DirectX und andere Komponenten. Viele optionale Komponenten werden regelmäßig aktualisiert, um Kundenfeedback zu integrieren und neue Features verfügbar zu machen.

## <a name="directx-version-number"></a>DirectX-Versionsnummer

Die DirectX-Versionsnummer, z. b. 9.0 c, bezieht sich nur auf die Version der Kernkomponenten, z. b. Direct3D, DirectInput oder DirectSound. Diese Zahl deckt nicht die Versionen der verschiedenen optionalen Komponenten ab, die im DirectX SDK freigegeben werden, z. b. D3DX, XACT, xinput usw.

Im Allgemeinen ist die DirectX-Versionsnummer nicht sinnvoll, außer als Kurzübersicht zu den Kern Lauf Zeit Bits. Diese Zahl sollte nicht verwendet werden, um zu überprüfen, ob die richtige DirectX-Laufzeit bereits installiert ist, da die optionalen DirectX-Komponenten nicht berücksichtigt werden.

## <a name="directx-libraries"></a>DirectX-Bibliotheken

In der Vergangenheit wurden die optionalen Komponenten des DirectX SDK, einschließlich D3DX, als statische Bibliotheken veröffentlicht. Diese werden jedoch jetzt als Dynamic-like-Bibliotheken (dll) veröffentlicht, da die Nachfrage nach besseren Sicherheitspraktiken erhöht wird. DLLs ermöglichen die Wartung von zuvor freigegebenen Code. Wenn diese Komponenten als statische Bibliotheken bereitgestellt wurden, gibt es keine Möglichkeit für Microsoft, Sicherheitsprobleme zu beheben, die nach der Veröffentlichung aufgetreten sind.

Beim Hinzufügen oder Ändern von Features zu den optionalen Komponenten werden die Namen der entsprechenden DLLs ebenfalls geändert, um sicherzustellen, dass keine Regressionen für vorhandene Spiele, die freigegebene Komponenten verwenden, entstehen. Die DLLs für jede Komponente sind nebeneinander, und Spielentwickler können genau auswählen, welche DLL-Version das Spiel verwendet, indem Sie eine Verknüpfung mit der entsprechenden Import Bibliothek herstellen.

Obwohl die Installation von DLLs auf einem System nicht so einfach ist wie das einfache Verknüpfen mit statischen Bibliotheken, wurden einige Änderungen am DirectX SDK vorgenommen, um die Probleme des dll-Modells zu beheben:

-   Die DirectX Redistributable kann so konfiguriert werden, dass Sie nur die Komponenten enthält, die Ihre Anwendung benötigt, um die Verteilung und die Mediengröße zu minimieren.
-   Der verteilbare Ordner "Programmdateien \\ DirectX SDK \\ Redist" \\ enthält jetzt eine CAB-Datei für jede mögliche optionale Komponente, sodass Sie kein älteres SDK mehr benötigen, um Sie zu finden.
-   Bei der Installation des SDK selbst werden alle möglichen optionalen Komponenten installiert.
-   Eine Redistributable von DirectX, die alle optionalen Komponenten enthält, ist sowohl als webbasiertes Installationsprogramm als auch als herunterladbares Paket verfügbar. Weitere Informationen finden Sie im DirectX Developer Center ([DirectX](/previous-versions/windows/apps/hh452744(v=win.10))).

## <a name="installation-of-directx-by-the-games-installer"></a>Installation von DirectX durch das Installationsprogramm des Spiels

> [!Note]  
> Weitere Informationen finden Sie unter [Direct3D 11 Deployment for Game Developers](/windows/desktop/direct3darticles/direct3d11-deployment).

 

Im folgenden sind die bewährten Methoden zum Hinzufügen der Installation von DirectX zum Installationsprogramm eines Spiels aufgeführt:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Begriff</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Install_the_redistributable_components_every_time.__"></span><span id="install_the_redistributable_components_every_time.__"></span><span id="INSTALL_THE_REDISTRIBUTABLE_COMPONENTS_EVERY_TIME.__"></span>Installieren Sie jedes Mal die verteilbaren Komponenten. <br/></td>
<td>Bei der Installation eines Spiels müssen die DirectX-weitervertreibbaren Komponenten bei jeder einzelnen Installation installiert werden, ohne dass die Benutzer dies ablehnen können. Wenn Sie die Abmeldung zulassen, werden einige Benutzer vermuten, dass Sie Sie nicht benötigen. Wenn Sie dies tatsächlich tun, wird das Spiel nicht ausgeführt. <br/></td>
</tr>
<tr class="even">
<td><span id="Let_the_DirectX_installer_check_for_optional_components.__"></span><span id="let_the_directx_installer_check_for_optional_components.__"></span><span id="LET_THE_DIRECTX_INSTALLER_CHECK_FOR_OPTIONAL_COMPONENTS.__"></span>Überprüfen Sie das DirectX-Installationsprogramm auf optionale Komponenten. <br/></td>
<td>Gehen Sie nicht davon aus, dass die neuesten optionalen Komponenten bereits auf einem System installiert sind, weil Windows Update und Service Packs keine der optionalen DirectX-Komponenten bereitstellen. Sie müssen die DirectX-Laufzeit entweder durch direktes Ausführen von dxsetup.exe oder durch Aufrufen von DirectSetup installieren. <br/></td>
</tr>
<tr class="odd">
<td><span id="Set_up_silently.__"></span><span id="set_up_silently.__"></span><span id="SET_UP_SILENTLY.__"></span>Im Hintergrund einrichten. <br/></td>
<td>Starten Sie das Setup im unbeaufsichtigten Modus, damit Benutzer nicht versehentlich das Aktualisieren der DirectX-Laufzeit überspringen. Hierzu können Sie dxsetup.exe mit dem folgenden Befehl starten: <br/>
<pre class="syntax" data-space="preserve"><code>   path-to-redistributable\dxsetup.exe /silent</code></pre>
oder durch Aufrufen von DirectSetup und ohne Anzeige einer Benutzeroberfläche. <br/></td>
</tr>
<tr class="even">
<td><span id="Combine_EULA_acceptances.__"></span><span id="combine_eula_acceptances.__"></span><span id="COMBINE_EULA_ACCEPTANCES.__"></span>Kombinieren Sie die EULA-Annahmen. <br/></td>
<td>Wenn Sie den Benutzer auffordern, einen Lizenzvertrag zu akzeptieren, kombinieren Sie ihn bei der Installation im unbeaufsichtigten Modus mit der Aufforderung zur Annahme der DirectX-EULA, damit die Anforderung zur Annahme von EULAs nur einmal erfolgt. Die Eingabeaufforderung sollte vor der Installation von etwas erfolgen, damit Sie, wenn der Benutzer nicht akzeptiert, nicht mit einer fehlgeschlagenen und partiellen Installation endet. <br/></td>
</tr>
<tr class="odd">
<td><span id="Just_run_dxsetup_or_call_DirectSetup.__"></span><span id="just_run_dxsetup_or_call_directsetup.__"></span><span id="JUST_RUN_DXSETUP_OR_CALL_DIRECTSETUP.__"></span>Führen Sie einfach dxsetup aus, oder nennen Sie DirectSetup. <br/></td>
<td>Da sich die DirectX-Versionsnummer nicht auf die DirectX-Kernkomponenten bezieht, sollten Sie eine installierte Version nicht überprüfen, bevor Sie dxsetup.exe ausführen oder DirectSetup aufrufen. Überprüfen Sie außerdem nicht, ob eine Datei vorhanden ist, um zu testen, ob eine optionale Komponente bereits installiert ist, da dies in der Regel nicht korrekt feststellt, wann eine Komponente vorhanden ist, aber aktualisiert werden muss. Das DirectX-Setup Paket wird dies jedoch schnell ermitteln und die richtige Aktion ausführen. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="small-installation-packages"></a>Kleine Installationspakete

Sie können kleinere Installationspakete für DirectX erstellen, indem Sie den Inhalt des Ordners "DirectX Redistributable" auf den minimalen Satz von Dateien herabsetzen, der zum Ausführen des Installationsprogramms erforderlich ist, und alle weiteren von Ihrem Spiel verwendeten Komponenten beibehalten.

Abhängig von den minimalen Spezifikationen müssen Sie möglicherweise nicht einmal die zentralen DirectX 9.0 c-CAB-Dateien in den verteilbaren Ordner Ihres Installationsmediums einschließen. Bei einer großen Mehrheit der Windows XP-Installationen ist Service Pack 2 enthalten, das die Kernkomponenten von DirectX 9.0 c umfasst, sodass der DirectX-Setup Vorgang sehr schnell ist und kein Neustart erforderlich ist. Das kleinste Paket, das erstellt werden kann, beträgt ca. 3 MB und kann auf ungefähr die Hälfte der Größe komprimiert werden. Ein Paket wie dieses enthält eine Version der D3DX-dll und erfordert, dass DirectX 9.0 c bereits vorhanden ist.

Die Mindestanzahl von Dateien, die zum Erstellen eines verteilbaren Pakets erforderlich sind, sind die folgenden Dateien im Ordner "DirectX SDK Redist" (Programmdateien \\ DirectX SDK \\ Redist \) :

-   dxsetup.exe
-   dsetup32.dll
-   dsetup.dll
-   dxupdate.cab

Fügen Sie den CAB-Dateien für die Komponenten hinzu, die Sie installieren möchten. Wenn Sie möchten, dass die Benutzer Ihrer Anwendung bereits über DirectX 9.0 c verfügen, müssen Sie keine DirectX.cab oder dxnt.cab einschließen, die den größten Teil der Speicherplatz Anforderung ausmachen. DirectX.cab wird nur für Windows 98 und Windows Me benötigt. dxnt.cab ist nur für Windows 2000, Windows XP und Windows XP SP1 erforderlich. und dxdllreg \_x86.cab ist nur für Windows 2000, Windows XP RTM, Windows XP SP1 und Windows Server 2003 RTM erforderlich. Wenn Sie DirectShow nicht verwenden oder wenn Sie davon ausgehen, dass es bereits installiert ist, können Sie BDA.cab, BDANT.cab und BDAXP.cab weglassen.

> [!Note]  
> Sie können davon ausgehen, dass die Benutzer Ihrer Anwendung bereits über DirectX 9.0 c verfügen, wenn Sie von einer früheren Version der Anwendung installiert wurde. Sie erzwingen, dass Benutzer über den Webinstaller manuell aktualisiert werden, oder Sie gehen davon aus, dass Sie über Windows XP SP2 oder höher verfügen.

 

Wenn Sie mit diesem Beispiel fortfahren, wenn Sie nur die 32-Bit-Version von D3DX für den 2006. April verwenden, können Sie Apr2006 \_ d3dx9 \_ 30x86.cab hinzufügen \_ . Wenn Sie die 32-Bit-Version der 2006 32-Bit-Version von xinput verwenden, fügen Sie Aug2006 \_ xinput- \_x86.cab hinzu.

Wenn Sie über eine systemeigene 64-Bit-Anwendung verfügen, müssen Sie die \_ x64-Versionen hinzufügen. Wenn Sie jedoch über eine 32-Bit-Anwendung verfügen, die auf einem 64-Bit-Betriebssystem ausgeführt wird, funktionieren die 32-Bit-Versionen der DLLs.

Anschließend können Sie dieses Paket von Dateien verteilen und DirectSetup im unbeaufsichtigten Modus starten oder dxsetup.exe in der Befehlsshell im unbeaufsichtigten Modus ausführen. Denken Sie daran, dieses Paket nicht durch eine Versions Überprüfung von Dateien zu schützen, und stellen Sie sicher, dass Ihre Benutzer die Ausführung des DirectX-Setups nicht deaktivieren können. Eines dieser Ereignisse führt zu einem fehl verfügbaren Installationsvorgang.

## <a name="internal-deployment-of-the-debug-directx-runtime"></a>Interne Bereitstellung der Debuggen DirectX-Laufzeit

Die debuglaufzeiten der DirectX-Komponenten werden bei der Installation des DirectX SDK installiert, aber die Installation des SDK auf jedem Testcomputer kann mühsam sein. Sie müssen den Setup Vorgang so entwerfen, dass die Debug-Lauf Zeit-DLLs aus den Programmdateien \\ Microsoft DirectX SDK \\ Developer Runtime \\ Architecture \\ in Windows \\ system32 \\ oder in den Ordner des Spiels kopiert werden.

Es wird jedoch dringend empfohlen, dass Sie die veröffentlichten Lauf Zeit-DLLs nicht einfach kopieren, da Sie leicht vergessen werden, Sie für das endgültige Produkt zu entfernen. Platzieren Sie stattdessen die DirectX-Setup Dateien in einem freigegebenen Ordner, und führen Sie das Setup automatisch aus dem freigegebenen Ordner aus.

## <a name="desktop-bridge-applications"></a>Desktop Bridge Anwendungen 

Desktop Bridge Anwendungen, die D3DX9, d3dx10, Bibliothek d3dx11, xaudio2,7, xinput 1,3 oder XACT verwenden, müssen entweder das [Microsoft. DirectX. x86](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x86.appx) -oder das [Microsoft. DirectX. x64](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x64.appx) -Framework herunterladen, um diese SDK-Komponenten parallel bereitzustellen. Alternativ dazu können Sie alle Abhängigkeiten entfernen (Weitere Informationen finden Sie &mdash; im [Entwicklerhandbuch für die weitervertreibbare Version von xaudio2,9 und in](../xaudio2/xaudio2-redistributable.md)den Blogbeiträgen, die [ohne D3DX](https://walbourn.github.io/living-without-d3dx/) und [XInput und Windows 8](https://walbourn.github.io/xinput-and-windows-8/)Leben).