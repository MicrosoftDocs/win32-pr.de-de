---
description: Entwicklerhandbuch für die weiterverteilbare Version von XAudio 2.9
ms.assetid: ''
title: Entwicklerhandbuch für die weiterverteilbare Version von XAudio 2.9
ms.topic: article
ms.date: 10/17/2019
ms.openlocfilehash: a73ebd01d599446dc96e1e6735d8af572203a23b
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262592"
---
# <a name="developer-guide-for-redistributable-version-of-xaudio-29"></a>Entwicklerhandbuch für die weiterverteilbare Version von XAudio 2.9

Eine Version von XAudio 2.9 ist als [NuGet-Paket](/nuget/what-is-nuget)verfügbar. Entwickler können diese Version von XAudio 2.9 mit ihren Apps neu verteilen. Dadurch kann eine App XAudio 2.9 unter älteren Windows-Versionen verwenden, die XAudio 2.9 nicht als Teil des Betriebssystemimages enthalten. Die Verwendung dieses weitervertrender Verteilbaren wird gegenüber der Weiterverteilung von XAudio 2.7 aus dem DirectX SDK bevorzugt, da XAudio 2.7 seit 2010 nicht aktualisiert wurde.

Stellen Sie sicher, dass Sie die [DirectX-Landing Page](https://devblogs.microsoft.com/directx/landing-page/) besuchen, um weitere Ressourcen für DirectX-Entwickler zu erhalten.

## <a name="supported-platforms"></a>Unterstützte Plattformen

Das XAudio 2.9 NuGet-Paket (*Microsoft.XAudio2.Redist. \* . nupkg*) enthält eine 32-Bit- und eine 64-Bit-Version einer DLL, die die XAudio 2.9-API implementiert. Die DLL wird als \_ XAUDIO2-9REDIST.DLL bezeichnet. Diese DLL funktioniert unter Windows 7 SP1, Windows 8, Windows 8.1 und Windows 10.

Wenn die DLL auf einem Windows 10 System verwendet wird, überprüft sie die Versionsnummer der \_ XAUDIO2-9.DLL, die Teil des Betriebssystems ist, und wenn das Betriebssystem neuer ist, werden alle API-Aufrufe an XAUDIO2-9.DLL im Betriebssystem delegiert. \_ Dadurch wird sichergestellt, dass Apps immer die neueste Version von XAudio 2.9 verwenden, die auf der aktuellen Plattform verfügbar ist.

Die DLL ist nicht für Xbox One vorgesehen. Bei Verwendung auf Xbox One delegiert die DLL immer alle API-Aufrufe an XAUDIO2-9.DLL \_ im Xbox One Betriebssystem.

Die DLL ist nicht für UWP-Apps vorgesehen. UWP-Apps sollten die XAUDIO2-9.DLL \_ verwenden, die Teil des Betriebssystems ist.

## <a name="installing-the-nuget-package"></a>Installieren des NuGet-Pakets

Die einfachste Möglichkeit zum Installieren des NuGet-Pakets ist die Verwendung des [NuGet-Paket-Manager](/nuget/consume-packages/install-use-packages-visual-studio) in Microsoft Visual Studio. Wenn Sie dies tun, wird Ihre Visual Studio-Projektdatei automatisch aktualisiert, um *Microsoft.XAudio2.Redist.targets* einzuschließt. Die *TARGETS-Datei* fügt den Ordner Include mit den Headerdateien für XAudio2 ihrer Sammlung von Projekteinschließtpfaden hinzu. Die *TARGETS-Datei* stellt auch ihren .DLL- oder .EXE-Link mit XAUDIO2REDIST her. LIB und XAPOBASEREDIST. Lib.

Die Bibliothek XAPOBASEREDIST. LIB ist nur erforderlich, wenn Sie beabsichtigen, ein benutzerdefiniertes XAudio Processing Object (XAPO) zu impementieren, und Sie können es aus *Microsoft.XAudio2.Redist.targets* entfernen, wenn es nicht verwendet wird.

Sie können auch andere Tools verwenden, um den Inhalt des NuGet-Pakets zu extrahieren, oder sogar die Dateierweiterung umbenennen, um die Dateien mit einem beliebigen ZIP-Extraktortool zu .zip und zu extrahieren.

> Es ist auch ein ``xaudio2redist`` Port für die [VC++-Paket-Manager](https://github.com/microsoft/vcpkg)verfügbar.

## <a name="compiling-your-app"></a>Kompilieren Ihrer App

### <a name="choosing-which-headers-to-include"></a>Auswählen der einzufügenden Header

Das XAudio 2.9 NuGet-Paket enthält die gleichen XAudio2-Headerdateien, die im Windows 10 SDK enthalten sind. Für die Headerdateien wurden jedoch einige Anpassungen vorgenommen, um sicherzustellen, dass Sie sie verwenden können, während sie explizit auf alle [unterstützten Plattformen](#supported-platforms)ausgerichtet sind, einschließlich älterer Versionen von Windows.

Wenn Sie [das NuGet-Paket](#installing-the-nuget-package) mithilfe des NuGet-Paket-Manager in Microsoft Visual Studio wird der Pfad zu den Headerdateien vor dem Pfad zu den Windows SDK Headerdateien platziert. Dies bedeutet, dass , wenn Code in Ihrem Projekt XAUDIO2 enthält. H-Header: Er übernimmt den plattformübergreifenden Header aus dem NuGet-Paket. Dies ist normalerweise das gewünschte Verhalten.

Sie sollten vorsichtig sein, wenn Sie den Pfad zu den Includeheadern manuell zum Projekt hinzufügen, da die Angabe in falscher Reihenfolge zu der betriebssystemversionsspezifischen [XAUDIO2 führen kann. H,](/windows/win32/api/xaudio2/) das aus dem Windows SDK und nicht aus der plattformübergreifenden Version von XAUDIO2.H aufgenommen werden soll.

Um die Einbindung von Headern weniger fehleranfällig zu machen, enthält das NuGet-Paket eine Version jedes Headers, an die "REDIST" angefügt ist. Beispielsweise zusätzlich zu XAUDIO2. H enthält das NuGet-Paket auch XAUDIO2REDIST.H. Wenn Sie möchten, kann Ihr Code XAUDIO2REDIST direkt enthalten. H, um mehrdeutige Informationen darüber zu vermeiden, welche Headerdatei verwendet wird. Beim Einschließen von -REDIST. H-Version einer Headerdatei, die Reihenfolge, in der die Includedateiverzeichnisse in der Projektdatei aufgeführt sind, spielt keine Rolle.

Beachten Sie, dass Sie XAUDIO2 weiterhin einschließen sollten, wenn Ihre App auch für Xbox One kompiliert wird. H beim Kompilieren für Xbox One, da einige Xbox One-spezifischen APIs von XAUDIO2REDIST.H ausgeschlossen werden. Dieses NuGet-Paket ist nicht für Xbox One vorgesehen.

### <a name="loading-the-dll"></a>Laden der DLL

Es wird empfohlen, Ihre App mit XAUDIO2REDIST zu verknüpfen. Lib and install XAUDIO2 \_9REDIST.DLL in demselben Ordner wie die ausführbare Datei Ihrer App. Dies führt dazu, dass XAUDIO2-9REDIST.DLL \_ geladen werden, sobald die ausführbare Datei gestartet wird. Wenn Sie dies jedoch vorziehen, können Sie [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um XAUDIO2-9REDIST.DLL bei Bedarf zu \_ laden. Dies ist eine gute Lösung, wenn Ihre App nicht immer die XAudio2-APIs verwenden muss. Wenn Sie dies tun, sollten Sie jedoch die XAUDIO2-9REDIST.DLL \_ geladen lassen, bis die App beendet wird, da der Versuch, die DLL zu entladen, einen Absturz verursachen kann, wenn ein Hintergrundthread weiterhin Code in der DLL ausführt.

Im Gegensatz zum älteren XAudio 2.7 ist es nicht möglich, CoCreateInstance zum Laden der DLL zu verwenden.

### <a name="verifying-the-dll-signature"></a>Überprüfen der DLL-Signatur

Die \_ XAUDIO2-9REDIST.DLL-Binärdatei wird von Microsoft mithilfe einer SHA-2-Signatur signiert. Jeder Code, der versucht, die Signatur zu überprüfen, z.B. Antispickzettelmodule für Spiele, muss daher SHA-2 unterstützen. Beachten Sie, dass Windows 7 SP1 SHA-2 ursprünglich nicht unterstützt hat und ein Update erforderlich ist, um diese Funktionalität hinzuzufügen. Das Update ist als [KB4474419](https://support.microsoft.com/help/4474419/sha-2-code-signing-support-update)verfügbar.

## <a name="testing"></a>Test

### <a name="spatial-sound-in-newer-versions-of-windows-10"></a>Räumlicher Sound in neueren Versionen von Windows 10

Ab dem Update Windows 10 1903 verwendet XAudio 2.9 automatisch [virtuellen Surround-Sound,](#spatial-sound-and-virtual-surround)wenn bestimmte Bedingungen erfüllt sind. Es wird empfohlen, ein Spiel zu testen, das mehrkanaligen Sound auf Windows 10 1903 (oder neuer) generiert, um zu überprüfen, ob das Spiel wie erwartet klingt.

#### <a name="enabling-spatial-sound"></a>Aktivieren von raumbezogenem Sound

Der Benutzer kann ein räumliches Soundformat aktivieren, indem er in der Windows-Taskleiste mit der rechten Maustaste auf das Lautsprechersymbol klickt. 

XAudio 2.9 verwendet nur das vom Benutzer ausgewählte Räumliche Soundformat, wenn der Prozess, der die XAudio2-API verwendet, vom Windows-Game Bar als Spiel erkannt wird. Während der Entwicklung ist es möglich, dass der Prozess noch nicht vom Game Bar als Spiel erkannt wird. Um dies zu ändern, verwenden Sie die Win+G-Tastenkombination, um die Game Bar während der Ausführung des Spiels aufzuführen. Klicken Sie dann auf das Symbol "Einstellungen", und aktivieren Sie das Kontrollkästchen "Denken Sie daran, dass dies ein Spiel ist".

#### <a name="opting-out-from-spatial-sound"></a>Deaktivieren von räumlichem Sound

Es gibt eine Möglichkeit, die Verwendung des Encoders für räumlichen Sound durch XAudio2 zu deaktivieren, indem Sie bestimmte Werte für den [**parameter AUDIO_STREAM_CATEGORY**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) in [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)angeben. 

Räumlicher Sound ist für diese Kategorien aktiviert:

* AudioCategory_ForegroundOnlyMedia
* AudioCategory_GameEffects
* AudioCategory_GameMedia
* AudioCategory_Movie
* AudioCategory_Media

Räumlicher Sound ist nicht aktiviert, wenn eine der folgenden Kategorien angegeben ist:

* AudioCategory_Other
* AudioCategory_Communications
* AudioCategory_Alerts
* AudioCategory_SoundEffects
* AudioCategory_GameChat
* AudioCategory_Speech

### <a name="error-handling"></a>Fehlerbehandlung

Es ist wichtig zu testen, ob Das Spiel eine Änderung des Audiogeräts verarbeiten kann, z. B. wenn Stecker angeschlossen oder nicht angeschlossen sind. Dies sollte mit Ausstellern getestet werden, die nur eine Samplingrate von 44,1 kHz unterstützen. Viele Low-End-USB-Headsets und Bluetooth-Headsets unterstützen nur 44,1 kHz. Der Übergang zwischen einer Samplingrate von 48 kHz und einer Samplingrate von 44,1 kHz kann auch dann einen Fehler verursachen, wenn das Feature für den [virtuellen Audioendpunkt](#virtual-audio-endpoint) verwendet wird. Der Fehler tritt nicht auf, wenn die Frequenzen auch 48 kHz unterstützen. Beachten Sie, dass das Feature für virtuelle Audioendpunkte unter Windows 7 SP1 nicht verfügbar ist.

Der von XAudio 2.9 zurückgegebene Fehlercode, wenn er nach einer Änderung des Audioendpunkts nicht automatisch wiederhergestellt werden kann, ist [XAUDIO2 \_ E \_ DEVICE \_ INVALIDATED.](xaudio2-error-codes.md) Es wird jedoch empfohlen, dass Apps keine Abhängigkeit vom Fehlercode mit einem bestimmten Wert hart coden.

Um über den Fehler benachrichtigt zu werden, sollte die App die [**IXAudio2EngineCallback-Schnittstelle**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) implementieren und einen Zeiger auf diese Schnittstelle bereitstellen, indem sie die [**IXAudio2::RegisterForCallbacks-Methode aufruft.**](xaudio2-callbacks.md) Die Implementierung der App von [**IXAudio2EngineCallback::OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) wird von der XAudio2-API aufgerufen, wenn während der Wiedergabe ein Fehler auftritt.

Beachten Sie, dass [**IXAudio2EngineCallback::OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) nicht unbedingt aufgerufen wird, wenn die Audiopipeline angehalten wird. Wenn der Benutzer beispielsweise die App minimiert oder die App aus irgendeinem Grund angehalten wird, wird die Audiowiedergabe möglicherweise angehalten. Wenn die Änderung des Audiogeräts während dieser Zeit erfolgt, wird der Fehler nur zurückgegeben, wenn die App [**IXAudio2::StartEngine**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-startengine) und/oder [**IXAudio2SourceVoice::Start**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)aufruft. Wenn die Wiedergabe mit Ihrer App angehalten werden kann, sollten Sie das Ändern des Audiogeräts testen, während die Wiedergabe angehalten ist, um zu überprüfen, ob die App nach dieser Situation wiederhergestellt werden kann.

## <a name="xaudio-29-api-differences-compared-to-xaudio-27"></a>Unterschiede der XAudio 2.9-API im Vergleich zu XAudio 2.7

Dieser Abschnitt enthält eine Zusammenfassung einiger API-Unterschiede zwischen XAudio 2.7 und der verteilbaren Version von XAudio 2.9.

### <a name="supported-formats"></a>Unterstützte Formate

XAudio 2.9 unterstützt diese Eingabeformate auf dem PC:

* Lineares 16-Bit-PCM
* Lineares 32-Bit-Float-PCM
* 16-Bit-ADPCM
* xWMA

Das XMA-Format wird nur auf Xbox One unterstützt.

### <a name="preferred-cpu-core"></a>Bevorzugter CPU-Kern

Es ist möglich anzugeben, welcher CPU-Kern XAudio 2.9 für den Audioverarbeitungsthread verwendet werden soll. Es wird jedoch in der Regel bevorzugt, XAudio 2.9 diesen Wert selbst auswählen zu lassen. Dies erfolgt durch Festlegen des **XAudio2Processor-Parameters** im Aufruf von [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) auf XAUDIO2 \_ USE DEFAULT \_ \_ PROCESSOR. 

XAudio 2.9 wählt einen anderen CPU-Kern auf Xbox One als auf dem PC aus. Die IXAudio2Extension::GetProcessor-Methode kann verwendet werden, um zu bestimmen, welcher CPU-Kern XAudio2 ausgewählt hat.

### <a name="virtual-audio-endpoint"></a>Virtueller Audioendpunkt

XAudio 2.9 verwendet standardmäßig einen virtuellen Audioendpunkt, wenn er auf Windows 8 oder höher ausgeführt wird. Dies bedeutet, dass, wenn sich der Standardaudioendpunkt ändert, während XAudio 2.9 verwendet wird, versucht wird, automatisch zum neuen Audioendpunkt zu wechseln. Ein Beispiel dafür, wann dies passieren kann, wenn der Standardaudioendpunkt ein Paar von Kabelträgern ist, die über USB verbunden sind, und der Benutzer dann die Verbindungspunkte entpackt. Dies führt dazu, dass die Lautsprecher der neue Standardaudioendpunkt sind.

Wenn die App beim Aufrufen von [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)ein bestimmtes Audioformat angibt, kann XAudio 2.9 diesen Schalter möglicherweise nicht ausführen. Wenn die App beispielsweise angegeben hat, dass die Mastering Voice eine Samplingrate von 48 kHz verwenden soll und das neue Audiogerät nur 44,1 kHz unterstützt, schlägt der automatische Switch fehl, und XAudio 2.9 meldet den Fehler [XAUDIO2 \_ E \_ DEVICE \_ INVALIDATED.](xaudio2-error-codes.md)

Es ist möglich, dass die App die Verwendung des virtuellen Audioendpunkts abwählt, indem sie das [**XAUDIO2 \_ NO VIRTUAL AUDIO \_ \_ \_ CLIENT-Flag**](xaudio2-boundary-values-and-flags.md) an [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)übergibt.

Virtuelle Audioendpunkte sind unter Windows 7 SP1 nicht verfügbar. Das **XAUDIO2 \_ NO VIRTUAL AUDIO \_ \_ \_ CLIENT-Flag** hat keine Auswirkungen auf Windows 7 SP1.

### <a name="audio-categories"></a>Audiokategorien

Die App sollte eine Kategorie für ihren Audiostream angeben. Dazu wird beim Aufrufen der [**IXAudio2::CreateMasteringVoice-Methode**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) ein Wert aus der AudioCategory-Enumeration angegeben. Beispiel: AudioCategory_GameEffects. Die Audiokategorie kann sich darauf auswirken, wie Windows den Sound verarbeitet oder wie er den Audiostream in der Lautstärkesteuerung darstellt. Die Audiokategorie wirkt sich auch darauf aus, ob [virtueller Surround-Sound](#spatial-sound-and-virtual-surround) automatisch aktiviert wird.

### <a name="duration-of-audio-processing-quantum"></a>Dauer der Audioverarbeitung von Quantendaten

Auf den meisten PCs verarbeitet XAudio 2.9 Audio in Blöcken von 10 Millisekunden. Dies wird als Verarbeitungsquant bezeichnet. Die Dauer dieses Quantums kann sich jedoch auf einer Hardware von 10 Millisekunden unterscheiden. Apps, die das genaue Quantum kennen müssen, können die IXAudio2Extension::GetProcessingQuantum-Methode aufrufen, um den Wert abzurufen.

### <a name="spatial-sound-and-virtual-surround"></a>Räumlicher Sound und virtueller Umschließen

Ab dem Update Windows 10 1903 verwendet XAudio 2.9 automatisch virtuellen Surround-Sound, wenn bestimmte Bedingungen erfüllt sind. Es wird empfohlen, ein Spiel zu testen, das mehrkanaligen Sound auf Windows 10 1903 (oder neuer) generiert, um zu überprüfen, ob das Spiel wie erwartet klingt. Im Abschnitt Testen des [räumlichen Sounds](#spatial-sound-in-newer-versions-of-windows-10) finden Sie eine Erläuterung zum Testen dieses Features.

Normalerweise führt XAudio 2.9 ein Folds down beliebiger Mehrkanalaudiodaten aus, um die "physische" Anzahl von Audiokanälen abzugleichen, die vom Audioendpunkt unterstützt werden. Wenn das Spiel z. B. eine 7.1-Kanalaudioquelle bereitstellt, der Sound jedoch auf 1-1-1-Kanälen wiedergegeben wird, wird XAudio 2.9 die 7.1-Kanalaudiodaten mithilfe einer branchenüblichen Fold-Down-Matrix in Stereo aufklappen. Wenn der PC mit einem PCI-Audioendpunkt verbunden ist, werden die Audiodaten des 7.1-Kanals über die CSV-Verbindung wie besehen übertragen.

Windows 10 fügt Unterstützung für räumliche Audioinhalte hinzu, indem ein zentralisierter Encoder verwendet wird, der Audiodaten in ein vom Benutzer ausgewähltes [räumliches Soundformat](../coreaudio/spatial-sound.md) codiert. Windows 10 ist im Raumtonformat Windows Sonic enthalten. Andere Formate, z. B. Dolby Atmos for Headphones, können von der Microsoft Store heruntergeladen werden. Einige räumliche Soundformate, z. B. Windows Sonic und Dolby Atmos for Headphones, sind für die Verwendung auf Stereoaudioendpunkten konzipiert. Diese Formate werden mithilfe proprietärer Algorithmen, die einen "virtuellen" Surround-Soundeffekt erzielen, in Stereo umschlossen. Mit anderen Worten: Der Listener kann Töne erkennen, die von unterschiedlichen Positionen im 3D-Raum angezeigt werden, auch wenn er nur Rauschen oder ein einzelnes Paar stereo-Lautsprecher lauscht.

Ähnliche Effekte können mithilfe der [X3DAudio-APIs](x3daudio.md) erzielt werden, die in XAudio 2.9 enthalten sind. Der Hauptunterschied besteht darin, dass X3DAudio erfordert, dass der App-Entwickler explizit für 3D-Audio programmiert, während virtueller Surround-Sound automatisch auf jede tradionale kanalbasierte Soundquelle angewendet wird.

Ab Windows 10 1903 verwenden Spiele, die XAudio 2.9 verwenden, das systemweite räumliche Soundformat, das der Benutzer ggf. auf dem Audioendpunkt aktiviert hat. Dies bedeutet, dass XAudio 2.9 nicht die übliche Abklappung von Surround-Sound in Stereo ausführt. Stattdessen wird das Umschließen des Soundsignals an den Encoder für räumlichen Sound (z. B. Windows Sonic) übermittelt, um einen virtuellen Surround-Soundeffekt zu erzielen.

### <a name="createhrtfapo"></a>CreateHrtfApo

Die [**CreateHrtfApo-Funktion**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo) ist nur auf Windows 10 verfügbar. Sie ist in XAudio 2.9 Redistributable nicht implementiert.
