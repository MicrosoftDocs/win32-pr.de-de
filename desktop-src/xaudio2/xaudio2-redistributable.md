---
description: Entwicklerhandbuch für die weiterverteilbare Version von XAudio 2.9
ms.assetid: ''
title: Entwicklerhandbuch für die weiterverteilbare Version von XAudio 2.9
ms.topic: article
ms.date: 10/17/2019
ms.openlocfilehash: a87c2dc44179f2c189270dfa91d2cf2696ea98a7
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103961256"
---
# <a name="developer-guide-for-redistributable-version-of-xaudio-29"></a>Entwicklerhandbuch für die weiterverteilbare Version von XAudio 2.9

Eine Version von xaudio2,9 ist als [nuget-Paket](/nuget/what-is-nuget)verfügbar. Entwickler können diese Version von xaudio2,9 mit ihren apps neu verteilen. Dadurch kann eine APP xaudio2,9 für ältere Versionen von Windows verwenden, die nicht als Teil des Betriebssystem Abbilds xaudio2,9 enthalten. Die Verwendung dieser weitervertreibbaren Komponente wird bei der Neuverteilung von xaudio2,7 aus dem DirectX SDK bevorzugt, da xaudio2,7 seit 2010 nicht aktualisiert wurde.

## <a name="supported-platforms"></a>Unterstützte Plattformen

Das xaudio2,9 nuget-Paket (*Microsoft. XAudio2. Redist. \* . nupkg*) umfasst eine 32-Bit-und eine 64-Bit-Version einer DLL, die die xaudio2,9-API implementiert. Die dll wird als XAUDIO2- \_9REDIST.DLL bezeichnet. Diese DLL funktioniert unter Windows 7 SP1, Windows 8, Windows 8.1 und Windows 10.

Wenn die dll auf einem Windows 10-System verwendet wird, wird die Versionsnummer des XAUDIO2-9.DLL überprüft, der \_ Teil des Betriebssystems ist. wenn das Betriebssystem neuer ist, werden alle API-Aufrufe an XAUDIO2- \_9.DLL im Betriebssystem delegiert. Dadurch wird sichergestellt, dass apps immer die neueste Version von xaudio2,9 verwenden, die auf der aktuellen Plattform verfügbar ist.

Die dll ist nicht für Xbox One vorgesehen. Bei Verwendung auf Xbox One delegiert die dll stets alle API-Aufrufe an XAUDIO2- \_9.DLL im Xbox One-Betriebssystem.

Die dll ist nicht für UWP-apps vorgesehen. UWP-apps sollten den XAUDIO2- \_9.DLL verwenden, der Teil des Betriebssystems ist.

## <a name="installing-the-nuget-package"></a>Installieren des NuGet-Pakets

Die einfachste Möglichkeit, das nuget-Paket zu installieren, ist die Verwendung des [nuget-Paket-Managers](/nuget/consume-packages/install-use-packages-visual-studio) in Microsoft Visual Studio. Wenn Sie dies tun, wird die Visual Studio-Projektdatei automatisch aktualisiert, sodass Sie *Microsoft. XAudio2. Redist. targets* enthält. Die *Targets* -Datei fügt den includeordner mit den Header Dateien für den XAudio2 ihrer Auflistung von Project Include-Pfaden hinzu. Die *Targets* -Datei macht auch Ihren. DLL oder. EXE-Verknüpfung mit XAUDIO2REDIST. LIB und xapobaseredist. LIB.

Die Bibliothek xapobaseredist. LIB ist nur erforderlich, wenn Sie ein benutzerdefiniertes xapo (xaudioprocessing Object)-Element beeinflussen möchten, und Sie es aus *Microsoft. XAudio2. Redist. targets* entfernen können, wenn es nicht verwendet wird.

Sie können auch andere Tools verwenden, um den Inhalt des nuget-Pakets zu extrahieren. Sie können auch die Dateierweiterung in ZIP-Dateien umbenennen und die Dateien mit einem beliebigen Zip-Extraktions Tool extrahieren.

## <a name="compiling-your-app"></a>Kompilieren der APP

### <a name="choosing-which-headers-to-include"></a>Auswählen der einzuschließüber Schriften

Das nuget-Paket xaudio2,9 enthält dieselben XAudio2-Header Dateien, die im Windows 10 SDK enthalten sind. Die Header Dateien wurden jedoch angepasst, um sicherzustellen, dass Sie Sie verwenden können, während Sie explizit auf alle [unterstützten Plattformen](#supported-platforms)abzielen, einschließlich älterer Versionen von Windows.

Wenn Sie [das nuget-Paket](#installing-the-nuget-package) mit dem nuget-Paket-Manager in installieren Microsoft Visual Studio dann wird der Pfad zu den Header Dateien vor dem Pfad zu den Windows SDK Header Dateien platziert. Dies bedeutet, dass der Code in Ihrem Projekt das XAUDIO2 enthält. H-Header wird der plattformübergreifende Header aus dem nuget-Paket abgerufen. Dies ist normalerweise das gewünschte Verhalten.

Sie sollten sorgfältig vorgehen, wenn Sie den Pfad zu den Include-Headern manuell zum Projekt hinzufügen. Wenn Sie diese in der falschen Reihenfolge angeben, kann dies zu der Betriebssystem-Versions spezifischen [XAUDIO2 führen. H](/windows/win32/api/xaudio2/) , der aus dem Windows SDK eingeschlossen werden soll, anstelle der plattformübergreifenden Version von XAUDIO2. H.

Das nuget-Paket enthält eine Version der einzelnen Header mit angefügtem "Redist", damit Header weniger fehleranfällig werden. Beispielsweise zusätzlich zu XAUDIO2. H, das nuget-Paket enthält auch XAUDIO2REDIST. h. Wenn Sie es vorziehen, kann Ihr Code XAUDIO2REDIST direkt einschließen. H, um Mehrdeutigkeit zu vermeiden, welche Header Datei verwendet wird. Beim Einschließen von-Redist. H-Version einer Header Datei, die Reihenfolge, in der die includedateiverzeichnisse in der Projektdatei aufgeführt sind, spielt keine Rolle.

Beachten Sie, dass Sie weiterhin XAUDIO2 einschließen müssen, wenn Ihre APP auch für Xbox One kompiliert wird. H beim Kompilieren für Xbox One, da einige Xbox One-spezifische APIs aus XAUDIO2REDIST. H ausgeschlossen werden. Dieses nuget-Paket ist nicht für Xbox One vorgesehen.

### <a name="loading-the-dll"></a>Die dll wird geladen.

Es wird empfohlen, dass Sie Ihre APP mit XAUDIO2REDIST verknüpfen. LIB und installieren \_ Sie XAUDIO29REDIST.DLL im selben Ordner wie die ausführbare Datei Ihrer APP. Dadurch werden XAUDIO2- \_9REDIST.DLL geladen, sobald die ausführbare Datei gestartet wird. Wenn Sie es jedoch bevorzugen, können Sie [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um XAUDIO2 \_9REDIST.DLL Bedarfs gesteuert zu laden. Dies ist eine gute Lösung, wenn Ihre APP nicht immer die XAudio2-APIs verwenden muss. Wenn Sie dies jedoch tun, sollten Sie die XAUDIO2- \_9REDIST.DLL so lange geladen werden, bis die APP beendet wird, da der Versuch, die dll zu entladen, einen Absturz verursachen kann, wenn ein Hintergrund Thread noch Code in der DLL ausführt.

Im Gegensatz zum älteren xaudio2,7 ist es nicht möglich, cokreateinzustance zum Laden der dll zu verwenden.

### <a name="verifying-the-dll-signature"></a>Überprüfen der dll-Signatur

Die XAUDIO2- \_9REDIST.DLL Binärdatei wird von Microsoft mit einer SHA-2-Signatur signiert. Jeder Code, der versucht, die Signatur zu überprüfen, z. b. antispick Module für Spiele, muss daher SHA-2 unterstützen. Beachten Sie, dass Windows 7 SP1 ursprünglich SHA-2 nicht unterstützte und ein Update erfordert, um diese Funktionalität hinzuzufügen. Das Update ist als [KB4474419](https://support.microsoft.com/help/4474419/sha-2-code-signing-support-update)verfügbar.

## <a name="testing"></a>Test

### <a name="spatial-sound-in-newer-versions-of-windows-10"></a>Räumlicher Sound in neueren Versionen von Windows 10

Beginnend mit dem Windows 10 1903-Update verwendet xaudio 2,9 automatisch den [virtuellen Umschließungs Sound](#spatial-sound-and-virtual-surround), wenn bestimmte Bedingungen erfüllt sind. Es empfiehlt sich, das Spiel zu testen, das Multi-Channel-Sound unter Windows 10 1903 (oder höher) generiert, um sicherzustellen, dass das Spiel erwartungsgemäß klingt.

#### <a name="enabling-spatial-sound"></a>Aktivieren von räumlichem Sound

Der Benutzer kann ein räumliches Sound Format aktivieren, indem er in der Windows-Taskleiste mit der rechten Maustaste auf das Redner Symbol klickt. 

Xaudio 2,9 verwendet nur das ausgewählte räumliche Audioformat des Benutzers, wenn der Prozess, der die XAudio2-API verwendet, von der Windows-Spiel Leiste als Spiel erkannt wird. Während der Entwicklung ist es möglich, dass der Prozess noch nicht als Spiel von der Spiel Leiste erkannt wird. Um dies zu ändern, verwenden Sie die Tastenkombination "Win + G", um die Spiel Leiste zu aktivieren, während das Spiel ausgeführt wird. Klicken Sie dann auf das Symbol "Einstellungen", und aktivieren Sie das Kontrollkästchen "denken Sie daran, dass es sich um ein Spiel handelt".

#### <a name="opting-out-from-spatial-sound"></a>Ablehnen aus räumlichem Sound

Es gibt eine Möglichkeit, sich zu entscheiden, dass XAudio2 den räumlichen Sound Encoder verwenden soll, indem Sie bestimmte Werte für den [**AUDIO_STREAM_CATEGORY**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) -Parameter in [**IXAudio2::**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)Erstellungs Sprache angeben. 

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

Es ist wichtig, zu testen, ob Sie eine Änderung des Audiogeräts durchführen können, z. b. wenn sich der Kopfhörer angeschlossen oder getrennt wird. Dies sollte mit einem Kopfhörer getestet werden, der nur die Stichprobenrate von 44,1 kHz unterstützt. Viele Low-End-USB-Kopfhörer und Bluetooth-Headsets unterstützen nur 44,1 kHz. Der Übergang zwischen 48 kHz-Samplingrate und 44,1 kHz-Samplingrate kann einen Fehler verursachen, auch wenn die Funktion des [virtuellen audioendpunkts](#virtual-audio-endpoint) verwendet wird. Der Fehler tritt nicht auf, wenn der Kopfhörer auch 48 kHz unterstützt. Beachten Sie, dass die Funktion für virtuelle audioendpunkte unter Windows 7 SP1 nicht verfügbar ist.

Der Fehlercode, der von xaudio2,9 zurückgegeben wird, wenn er von einer Änderung des audioendpunkts nicht automatisch wieder hergestellt werden kann, ist [XAUDIO2 \_ E \_ Gerät \_ ungültig](xaudio2-error-codes.md). Es wird jedoch empfohlen, dass apps keine Abhängigkeit von dem Fehlercode mit einem bestimmten Wert hart codieren.

Um über den Fehler benachrichtigt zu werden, sollte die APP die [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) -Schnittstelle implementieren und einen Zeiger auf diese Schnittstelle bereitstellen, indem die [**IXAudio2:: registerforcallbacks**](xaudio2-callbacks.md) -Methode aufgerufen wird. Die APP-Implementierung von [**IXAudio2EngineCallback:: oncriticalerror**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) wird von der XAudio2-API aufgerufen, wenn ein Fehler während der Wiedergabe auftritt.

Beachten Sie, dass [**IXAudio2EngineCallback:: oncriticalerror**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror) nicht notwendigerweise aufgerufen wird, wenn die audiopipeline angehalten wurde. Wenn der Benutzer z. b. die APP minimiert oder die APP aus irgendeinem Grund angehalten wird, wird die Audiowiedergabe möglicherweise angehalten. Wenn die Änderung des Audiogeräts während dieser Zeit erfolgt, wird der Fehler nur zurückgegeben, wenn die APP [**IXAudio2:: startEngine**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-startengine) aufruft und/oder [**IXAudio2SourceVoice:: Start**](/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)aufruft. Wenn die Wiedergabe mit Ihrer APP angehalten werden kann, sollten Sie die Änderung des Audiogeräts testen, während die Wiedergabe angehalten wird, um zu überprüfen, ob die APP nach dieser Situation weiterhin wieder hergestellt werden kann.

## <a name="xaudio-29-api-differences-compared-to-xaudio-27"></a>Xaudio2,9-API-Unterschiede im Vergleich zu xaudio2,7

Dieser Abschnitt enthält eine Zusammenfassung einiger API-Unterschiede zwischen xaudio2,7 und der verteilbaren Version von xaudio2,9.

### <a name="supported-formats"></a>Unterstützte Formate

Xaudio2,9 unterstützt diese Eingabeformate auf dem PC:

* Lineares 16-Bit-PCM
* Lineares 32-Bit Float-PCM
* 16-Bit-ADPCM
* xwma

Das XMA-Format wird nur auf Xbox One unterstützt.

### <a name="preferred-cpu-core"></a>Bevorzugter CPU-Kern

Es ist möglich, anzugeben, welcher CPU-Core-xaudiowert 2,9 für den audioverarbeitungsthread verwenden soll. Es ist jedoch in der Regel vorzuziehen, xaudio2,9 den Wert selbst auszuwählen. Dies erfolgt durch Festlegen des **XAudio2Processor** -Parameters im Aufrufen von [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) auf XAUDIO2 \_ \_ Standard Prozessor verwenden \_ . 

Xaudio2,9 wählt einen anderen CPU-Kern auf Xbox One als auf dem PC aus. Die IXAudio2Extension:: getprocessor-Methode kann verwendet werden, um zu bestimmen, welcher CPU-Kern XAudio2 ausgewählt hat.

### <a name="virtual-audio-endpoint"></a>Virtueller audioendpunkt

Xaudio2,9 verwendet standardmäßig einen virtuellen audioendpunkt, wenn er unter Windows 8 oder höher ausgeführt wird. Dies bedeutet Folgendes: Wenn der standardaudioendpunkt bei Verwendung von xaudio2,9 geändert wird, wird versucht, automatisch zum neuen audioendpunkt zu wechseln. Dies kann beispielsweise vorkommen, wenn der standardaudioendpunkt ein paar von über USB verbundenen Paaren ist und der Benutzer dann die Plug-ins entrichtet. Dies führt dazu, dass die Redner als neuer standardaudioendpunkt verwendet werden.

Wenn die APP ein bestimmtes Audioformat beim Aufrufen von [**IXAudio2:: deatemasteringvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)angibt, ist es möglicherweise nicht möglich, dass xaudio2,9 diesen Switch ausführt. Wenn die APP beispielsweise festgelegt hat, dass die Mastering-Stimme eine 48 kHz-Samplingrate verwenden soll und das neue Audiogerät nur 44,1 kHz unterstützt, schlägt der automatische Switch fehl, und xaudio2,9 meldet den Fehler " [XAUDIO2 \_ E \_ Device \_ invalidiert](xaudio2-error-codes.md) ".

Es ist möglich, dass die APP die Verwendung des virtuellen audioendpunkts deaktiviert, indem das Flag [**XAUDIO2 \_ No \_ Virtual \_ \_ AudioClient**](xaudio2-boundary-values-and-flags.md) an [**IXAudio2:: kreatemasteringvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)übergeben wird.

Virtuelle audioendpunkte sind unter Windows 7 SP1 nicht verfügbar. Das **Flag \_ XAUDIO2 \_ No \_ Virtual \_ AudioClient** hat keine Auswirkung auf Windows 7 SP1.

### <a name="audio-categories"></a>Audiokategorien

Die APP sollte eine Kategorie für Ihren Audiostream angeben. Dies erfolgt durch Bereitstellen eines Werts aus der audiocategory-Enumeration beim Aufrufen der [**IXAudio2:: deatemasteringvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) -Methode. Beispielsweise AudioCategory_GameEffects. Die Kategorie Audio kann beeinflussen, wie der Sound von Windows verarbeitet wird oder wie er den Audiostream in der Systemsteuerung des Volumes darstellt. Die Kategorie Audio wirkt sich auch darauf aus, ob der [virtuelle Umschließungs Sound](#spatial-sound-and-virtual-surround) automatisch aktiviert wird.

### <a name="duration-of-audio-processing-quantum"></a>Dauer der Audioverarbeitung (Quantum)

Auf den meisten PCs verarbeitet xaudio2,9 Audiodaten in Blöcken von 10 Millisekunden. Dies wird als Verarbeitungs Quantum bezeichnet. Die Dauer dieses Quantums kann sich jedoch auf der Hardware von 10 Millisekunden unterscheiden. Apps, die das exakte Quantum kennen müssen, können die IXAudio2Extension:: getprocessingquantum-Methode aufrufen, um den Wert abzurufen.

### <a name="spatial-sound-and-virtual-surround"></a>Räumlicher Sound und virtueller Umschlag

Beginnend mit dem Windows 10 1903-Update verwendet xaudio 2,9 automatisch den virtuellen Umschließungs Sound, wenn bestimmte Bedingungen erfüllt sind. Es empfiehlt sich, das Spiel zu testen, das Multi-Channel-Sound unter Windows 10 1903 (oder höher) generiert, um sicherzustellen, dass das Spiel erwartungsgemäß klingt. Eine Erläuterung zum Testen dieses Features finden Sie im Abschnitt [Testen des räumlichen Sounds](#spatial-sound-in-newer-versions-of-windows-10) .

Normalerweise führt xaudio2,9 alle multikanalaudiodaten so aus, dass Sie mit der "physischen" Anzahl von Audiokanälen identisch sind, die vom audioendpunkt unterstützt werden. Wenn das Spiel z. b. eine 7,1-Kanal-Audioquelle bereitstellt, der Sound aber auf einem Kopfhörer abgespielt wird, wird xaudio 2,9 die 7,1 Channel-Audiodaten in Stereo unter Verwendung einer nach Industriestandard mäßigen Fold-Down-Matrix ablegen. Wenn der PC mit einem HDMI-audioendpunkt verbunden ist, wird der 7,1-Channel-Audioinhalt unverändert über die HDMI-Verbindung übertragen.

Windows 10 bietet Unterstützung für räumliche Audiodaten mithilfe eines zentralisierten Encoders, der Audio in ein vom Benutzer ausgewähltes [räumliches](../coreaudio/spatial-sound.md) Audioformat codiert. Windows 10 ist in einem räumlichen Sound Format namens Windows Sonic enthalten. Andere Formate, z. b. Dolby Atmos für Kopfhörer, können vom Microsoft Store heruntergeladen werden. Einige der räumlichen Audioformate, wie z. b. Windows Sonic und Dolby Atmos für Kopfhörer, sind so konzipiert, dass Sie auf Stereo-audioendpunkten verwendet werden. Diese Formate werden mit proprietären Algorithmen, die einen "virtuellen" einschließenden Effekt erzielen, als "virtuell" formatiert. Mit anderen Worten: der Listener kann Sound erkennen, der von unterschiedlichen Positionen in 3D-Raum angezeigt wird, auch wenn nur die Kopfzeile oder ein einzelnes Paar von Stereo Referenten gehört.

Ähnliche Effekte können mithilfe der [X3DAudio](x3daudio.md) -APIs erzielt werden, die in xaudio2,9 enthalten sind. Der Hauptunterschied besteht darin, dass für X3DAudio der App-Entwickler explizit für 3D-Audiodaten programmieren muss, während der virtuelle Einschließungs Sound automatisch auf eine beliebige traditionelle kanalbasierte Audioquelle angewendet wird.

Bei Windows 10 1903 und neueren Anwendungen verwenden Spiele, die xaudio 2,9 verwenden, das systemweite räumliche Audioformat, das der Benutzer ggf. auf dem audioendpunkt aktiviert hat. Dies bedeutet, dass xaudio 2,9 nicht das übliche Abbild von Umschließungs Sound zu Stereo durchführt. Stattdessen wird das umschließende Sound Signal an den räumlichen Audioencoder (z. b. Windows-Sonic) übermittelt, um einen virtuellen umschließenden Soundeffekt zu erzielen.

### <a name="createhrtfapo"></a>"Kreatehrtfapo"

Die Funktion "| [**atehrtfapo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo) " ist nur unter Windows 10 verfügbar. Sie ist nicht in der weitervertreibbaren Komponente von xaudio2,9 implementiert.
