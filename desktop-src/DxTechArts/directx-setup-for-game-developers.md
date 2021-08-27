---
title: DirectX-Installation für Spieleentwickler
description: In diesem Artikel werden einige der häufig gestellten Fragen zur DirectX-Runtime und die Verwendung von DirectSetup zum Installieren von DirectX behandelt.
ms.assetid: 2ab439be-8d99-bcf8-89af-d4274e044c88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0509084232f1dcfe63a7d956516aa723f8cd724b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477286"
---
# <a name="directx-installation-for-game-developers"></a>DirectX-Installation für Spieleentwickler

In diesem Artikel werden einige der häufig gestellten Fragen zur DirectX-Runtime und die Verwendung von DirectSetup zum Installieren von DirectX behandelt.

-   [DirectX-Runtime](#directx-runtime)
-   [DirectX-Versionsnummer](#directx-version-number)
-   [DirectX-Bibliotheken](#directx-libraries)
-   [Installation von DirectX durch den Installer des Spiels](#installation-of-directx-by-the-games-installer)
-   [Kleine Installationspakete](#small-installation-packages)
-   [Interne Bereitstellung der Debug-DirectX-Runtime](#internal-deployment-of-the-debug-directx-runtime)

> [!IMPORTANT]
> Das Legacy-DirectX SDK befindet sich am Ende der Lebensdauer, ist aber weiterhin verfügbar, um alte Spiele, Tutorials und Projekte zu unterstützen. Neue Projekte sollten sie nicht verwenden. Die Verwendung des älteren DirectX SDK erfordert die Verwendung des veralteten DirectSetup für Komponenten wie D3DX9, D3DX10, D3DX11, XAudio 2.7, XInput 1.3 und XACT. Weitere Informationen zum aktuellen Zustand des DirectX SDK finden Sie unter Wo befindet sich [das DirectX SDK?](../directx-sdk--august-2009-.md)und im Blogbeitrag [Not So Direct Setup](https://walbourn.github.io/not-so-direct-setup/).

## <a name="directx-runtime"></a>DirectX-Runtime

Die DirectX-Runtime besteht aus Kernkomponenten und optionalen Komponenten.

Die Kernkomponenten wie Direct3D und DirectInput werden als Teil des Betriebssystems betrachtet. Die Kernkomponenten für DirectX 9.0c haben sich seit dem DirectX SDK-Update von Sommer 2004 nicht geändert und entsprechen den Veröffentlichungen von Microsoft Windows XP SP2, Windows XP Pro x64 Edition und Windows Server 2003 SP1. Windows Vista enthält DirectX 10, das das Windows Display Driver Model (WDDM) und Direct3D 10.x unterstützt. Windows 7 und Windows Vista (siehe [KB971644)](https://support.microsoft.com/kb/971644)unterstützen DirectX 11, das Direct3D 11, Direct2D, DirectWrite, das WARP10-Softwarerenderinggerät und die 10level9-Featureebenen unterstützt. Weitere Informationen finden Sie [unter Grafik-APIs in Windows.](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista)

Die optionalen Komponenten werden in Updates des DirectX SDK veröffentlicht und umfassen D3DX, XACT, XAudio2, XINPUT, Managed DirectX und andere solche Komponenten. Viele der optionalen Komponenten werden regelmäßig aktualisiert, um Kundenfeedback zu integrieren und neue Features verfügbar zu machen.

## <a name="directx-version-number"></a>DirectX-Versionsnummer

Die DirectX-Versionsnummer, z.B. 9.0c, bezieht sich nur auf die Version der Kernkomponenten wie Direct3D, DirectInput oder DirectSound. Diese Zahl deckt nicht die Versionen der verschiedenen optionalen Komponenten ab, die im DirectX SDK veröffentlicht werden, z. B. D3DX, XACT, XINPUT usw.

Im Allgemeinen ist die DirectX-Versionsnummer nur als Kurzübersicht auf die Kernlaufzeitbits sinnvoll. Diese Zahl sollte nicht verwendet werden, um zu überprüfen, ob die richtige DirectX-Runtime bereits installiert ist, da sie die optionalen DirectX-Komponenten nicht berücksichtigt.

## <a name="directx-libraries"></a>DirectX-Bibliotheken

In der Vergangenheit wurden die optionalen Komponenten des DirectX SDK, einschließlich D3DX, als statische Bibliotheken veröffentlicht. Diese werden jetzt jedoch als dll-ähnliche Bibliotheken (Dynamic-Like Libraries) veröffentlicht, da die Nachfrage nach besseren Sicherheitsmethoden steigt. DLLs ermöglichen die Wartung von zuvor freigegebenen Code. Wenn diese Komponenten als statische Bibliotheken bereitgestellt würden, gibt es für Microsoft keine Möglichkeit, nach der Veröffentlichung gefundene Sicherheitsprobleme zu beheben.

Wenn den optionalen Komponenten Features hinzugefügt oder geändert werden, werden auch die Namen der entsprechenden DLLs geändert, um sicherzustellen, dass keine Regressionen auf vorhandene Spiele zurückzuführen sind, die freigegebene Komponenten verwenden. Die DLLs für jede Komponente werden nebeneinander gespeichert, und Spieleentwickler können genau auswählen, welche DLL-Version vom Spiel verwendet wird, indem sie mit der entsprechenden Importbibliothek verknüpft werden.

Es ist zwar nicht so einfach, sicherzustellen, dass DLLs auf einem System installiert sind, als einfach mit statischen Bibliotheken zu verknüpfen, aber es wurden einige Änderungen am DirectX SDK vorgenommen, um die Probleme des DLL-Modells zu beheben:

-   DirectX Redistributable kann so konfiguriert werden, dass es nur die Komponenten enthält, die Ihre Anwendung benötigt, um die Verteilungs- und Mediengrößen zu minimieren.
-   Der verteilbare Ordner Program Files \\ DirectX SDK \\ Redist \\ enthält jetzt eine .cab datei für jede mögliche optionale Komponente, sodass Sie kein älteres SDK suchen müssen, um sie zu finden.
-   Bei der Installation des SDK selbst wird jede mögliche optionale Komponente installiert.
-   Ein DirectX Redistributable, das alle optionalen Komponenten enthält, ist sowohl als webbasiertes Installationsprogramm als auch als herunterladbares Paket verfügbar. Weitere Informationen finden Sie im DirectX Developer Center[(DirectX).](/previous-versions/windows/apps/hh452744(v=win.10))

## <a name="installation-of-directx-by-the-games-installer"></a>Installation von DirectX durch den Installer des Spiels

> [!Note]  
> Weitere Informationen finden Sie unter [Direct3D 11-Bereitstellung für Spieleentwickler.](/windows/desktop/direct3darticles/direct3d11-deployment)

 

Im Folgenden werden die bewährten Methoden zum Hinzufügen der Installation von DirectX zum Installationsprogramm eines Spiels angezeigt:




| Begriff | BESCHREIBUNG | 
|------|-------------|
| <span id="Install_the_redistributable_components_every_time.__"></span><span id="install_the_redistributable_components_every_time.__"></span><span id="INSTALL_THE_REDISTRIBUTABLE_COMPONENTS_EVERY_TIME.__"></span>Installieren Sie die verteilbaren Komponenten jedes Mal. <br /> | Beim Installationsprozess eines Spiels sollten die verteilbaren DirectX-Komponenten während jeder einzelnen Installation installiert werden, ohne dass Benutzer dies deaktivieren können. Wenn Sie die Deaktivierung zulassen, werden einige Benutzer erraten, dass sie sie nicht benötigen, und wenn sie dies tatsächlich tun, wird das Spiel nicht ausgeführt. <br /> | 
| <span id="Let_the_DirectX_installer_check_for_optional_components.__"></span><span id="let_the_directx_installer_check_for_optional_components.__"></span><span id="LET_THE_DIRECTX_INSTALLER_CHECK_FOR_OPTIONAL_COMPONENTS.__"></span>Lassen Sie das DirectX-Installationsprogramm nach optionalen Komponenten suchen. <br /> | Gehen Sie nicht davon aus, dass die neuesten optionalen Komponenten bereits auf einem System installiert sind, da Windows Update und Service Packs keine optionalen DirectX-Komponenten bereitstellen. Sie müssen die DirectX-Runtime installieren, indem Sie dxsetup.exe direkt ausführen oder DirectSetup aufrufen. <br /> | 
| <span id="Set_up_silently.__"></span><span id="set_up_silently.__"></span><span id="SET_UP_SILENTLY.__"></span>Im Hintergrund einrichten. <br /> | Starten Sie das Setup im unbeaufsichtigten Modus, damit Benutzer die Aktualisierung der DirectX-Runtime nicht versehentlich überspringen. Hierzu können Sie dxsetup.exe mit dem folgenden Befehl starten: <br /><pre class="syntax" data-space="preserve"><code>   path-to-redistributable\dxsetup.exe /silent</code></pre>oder durch Aufrufen von DirectSetup und ohne Anzeige einer Benutzeroberfläche. <br /> | 
| <span id="Combine_EULA_acceptances.__"></span><span id="combine_eula_acceptances.__"></span><span id="COMBINE_EULA_ACCEPTANCES.__"></span>Kombinieren Sie die Zustimmungen zu Lizenzvereinbarung. <br /> | Wenn Sie den Benutzer auffordern, eine Lizenzvereinbarung zu akzeptieren, kombinieren Sie dies mit der Aufforderung zur Annahme der DirectX-Lizenzvereinbarung bei der Installation im unbeaufsichtigten Modus, sodass die Aufforderung zur Zustimmung zu EULAs nur einmal erfolgt. Es sollte eine Aufforderung erfolgen, bevor Sie etwas installieren. Wenn der Benutzer dies nicht akzeptiert, tritt keine fehlerhafte und teilweise Installation auf. <br /> | 
| <span id="Just_run_dxsetup_or_call_DirectSetup.__"></span><span id="just_run_dxsetup_or_call_directsetup.__"></span><span id="JUST_RUN_DXSETUP_OR_CALL_DIRECTSETUP.__"></span>Führen Sie einfach dxsetup aus, oder rufen Sie DirectSetup auf. <br /> | Da sich die DirectX-Versionsnummer nur auf die DirectX-Kernkomponenten bezieht, überprüfen Sie keine installierte Version, bevor Sie dxsetup.exe ausführen oder DirectSetup aufrufen. Überprüfen Sie außerdem nicht, ob eine Datei vorhanden ist, um zu testen, ob bereits eine optionale Komponente installiert ist, da dadurch normalerweise nicht richtig bestimmt wird, wann eine Komponente vorhanden ist, aber aktualisiert werden muss. Das DirectX-Setuppaket ermittelt dies jedoch schnell und führt die richtige Aktion aus. <br /> | 




 

## <a name="small-installation-packages"></a>Kleine Installationspakete

Sie können kleinere Installationspakete für DirectX erstellen, indem Sie den Inhalt des verteilbaren DirectX-Ordners auf den minimalen Satz von Dateien verschieben, die erforderlich sind, damit das Installationsprogramm funktioniert, und alle zusätzlichen Komponenten beibehalten, die ihr Spiel verwendet.

Abhängig von Ihren Mindestspezifikationen müssen Sie möglicherweise nicht einmal die DirectX 9.0c-Kernschränkdateien in den verteilbaren Ordner Ihrer Installationsmedien einschließen. Ein großteil der Windows XP-Installationen verfügt über Service Pack 2, das die DirectX 9.0c-Kernkomponenten enthält, sodass der DirectX-Setupvorgang sehr schnell ist und kein Neustart erforderlich ist. Das kleinste Paket, das erstellt werden kann, beträgt etwa 3 MB und kann auf etwa die Hälfte dieser Größe komprimiert werden. Ein Paket wie dieses enthält eine Version der D3DX-DLL und erfordert, dass DirectX 9.0c bereits vorhanden ist.

Die minimalen Dateien, die zum Erstellen eines verteilbaren Pakets erforderlich sind, sind die folgenden Dateien, die sich im Ordner DirectX SDK Redist befinden (Program Files \\ DirectX SDK \\ Redist \) :

-   dxsetup.exe
-   dsetup32.dll
-   dsetup.dll
-   dxupdate.cab

Fügen Sie diesen die Cab-Dateien für die Komponenten hinzu, die Sie installieren möchten. Wenn Die Benutzer Ihrer Anwendung bereits über DirectX 9.0c verfügen müssen, müssen Sie keine DirectX.cab oder dxnt.cab einschließen, die den größten Teil des Speicherplatzbedarfs ausmachen. DirectX.cab wird nur für Windows 98 und Windows ME benötigt. dxnt.cab wird nur für Windows 2000, Windows XP und Windows XP SP1 benötigt. und dxdllreg \_x86.cab ist nur für Windows 2000, Windows XP RTM, Windows XP SP1 und Windows Server 2003 RTM erforderlich. Wenn Sie DirectShow nicht verwenden oder davon ausgehen, dass es bereits installiert ist, können Sie BDA.cab, BDANT.cab und BDAXP.cab weglassen.

> [!Note]  
> Sie können davon ausgehen, dass Benutzer Ihrer Anwendung bereits über DirectX 9.0c verfügen, wenn sie von einer früheren Version Ihrer Anwendung installiert wurde, Sie erzwingen, dass Benutzer manuell über den Webinstaller aktualisieren, oder Sie gehen davon aus, dass sie über Windows XP SP2 oder höher verfügen.

 

Wenn Sie in diesem Beispiel nur die 32-Bit-Version von D3DX für April 2006 verwenden, können Sie Apr2006 \_ d3dx9 \_ 30 \_x86.cab hinzufügen. Wenn Sie die 32-Bit-Version von XINPUT vom August 2006 verwenden, fügen Sie Aug2006 \_ xinput \_x86.cab hinzu.

Wenn Sie über eine native 64-Bit-Anwendung verfügen, müssen Sie die \_ x64-Versionen hinzufügen. Wenn Sie jedoch über eine 32-Bit-Anwendung verfügen, die unter einem 64-Bit-Betriebssystem ausgeführt wird, funktionieren die 32-Bit-Versionen der DLLs.

Anschließend können Sie dieses Paket von Dateien verteilen und DirectSetup im unbeaufsichtigten Modus starten oder dxsetup.exe in der Befehlsshell im unbeaufsichtigten Modus ausführen. Denken Sie daran, dieses Paket nicht durch eine Versionsüberprüfung von Dateien zu schützen, und stellen Sie sicher, dass Ihre Benutzer die Ausführung des DirectX-Setups nicht deaktivieren können. Eines dieser Ereignisse erstellt einen fehlbaren Installationsvorgang.

## <a name="internal-deployment-of-the-debug-directx-runtime"></a>Interne Bereitstellung der Debug-DirectX-Runtime

Die Debuglaufzeiten der DirectX-Komponenten werden installiert, wenn das DirectX SDK installiert wird. Die Installation des SDK auf jedem Testcomputer kann jedoch mühsam sein. Sie müssen Ihren Setupprozess so entwerfen, dass die Debugruntime-DLLs aus der Microsoft DirectX SDK Developer Runtime-Architektur von Programme in \\ \\ Windows \\ \\ \\ System32 oder in den Ordner des \\ Spiels kopiert werden.

Es wird jedoch dringend empfohlen, die freigegebenen Laufzeit-DLLs nicht einfach zu kopieren, da sie leicht vergessen werden, sie für das endgültige Produkt zu entfernen. Legen Sie stattdessen die DirectX-Setupdateien in einem freigegebenen Ordner ab, und führen Sie das Setup im Hintergrund aus dem freigegebenen Ordner aus.

## <a name="desktop-bridge-applications"></a>Desktop-Brücke Anwendungen 

Desktop-Brücke Anwendungen, die D3DX9, D3DX10, D3DX11, XAudio 2.7, XInput 1.3 oder XACT verwenden, müssen entweder [Microsoft.DirectX.x86](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x86.appx) oder das [Microsoft.DirectX.x64-Framework](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x64.appx) herunterladen, um diese älteren DirectX SDK-Komponenten parallel bereitzustellen. Alternativ können Sie alle abhängigkeiten dieser Art entfernen (weitere Informationen &mdash; finden Sie im [Entwicklerhandbuch für die verteilbare Version von XAudio 2.9](../xaudio2/xaudio2-redistributable.md)und in den Blogbeiträgen [Living without D3DX](https://walbourn.github.io/living-without-d3dx/) and [XINPUT and Windows 8](https://walbourn.github.io/xinput-and-windows-8/)).
