---
description: XAudio2 ist eine plattformübergreifende API, die für die Verwendung auf Xbox 360 und Versionen von Windows, einschließlich Windows XP, Windows Vista, Windows 7 und Windows 8, ausgeliefert wurde.
ms.assetid: 875b44c4-30d6-8a6e-0cfc-9beb8c46f1b4
title: XAudio2-Versionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c9facfe357c323bd8f7b607460a8f59bd062fe
ms.sourcegitcommit: 010f524cd6098a5941de77907d4d6ae7871f8af1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "106366351"
---
# <a name="xaudio2-versions"></a>XAudio2-Versionen

XAudio2 ist eine plattformübergreifende API, die für die Verwendung auf Xbox 360 und Versionen von Windows, einschließlich Windows XP, Windows Vista, Windows 7 und Windows 8, ausgeliefert wurde. Auf Xbox 360 wird XAudio2 als statische Bibliothek ausgeliefert, die in die ausführbare Datei des Hauptspiels kompiliert wird. Unter Windows wird XAudio2 als Dynamic Link Library (dll) bereitgestellt, die in den Systemordnern des Betriebssystems installiert ist.

## <a name="xaudio-29-windows-10-and-redistributable-for-windows-7-and-windows-8x"></a>Xaudio2,9 (Windows 10 und verteilbare Komponente für Windows 7 und Windows 8. x)

XAudio2 Version 2,9 wird als Teil von Windows 10, XAudio2 \_9.DLL zusammen mit xaudio2,8 zur Unterstützung älterer Anwendungen ausgeliefert. Eine Verteil [Bare Version von xaudio2,9](xaudio2-redistributable.md) ist auch für Windows 7 SP1, Windows 8 und Windows 8.1 verfügbar.

Xaudio2.9 wurde mit den folgenden Änderungen aktualisiert:

-   Neue erstellungsflags: XAUDIO2 \_ Debug \_ Engine, XAUDIO2 \_ Beenden \_ Engine \_ When \_ Idle, XAUDIO2 \_ 1024 \_ Quantum
-   xwma-Unterstützung ist in dieser Version von XAudio2 verfügbar.
-   Die [**Funktion "**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo) Funktion" in Windows 10 wird in der Windows 10-Version von xaudioversion 2,9 unterstützt.
-   [**XAUDIO2FX \_ Die \_ Parameter "Reverb**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) " enthält jetzt den Wert " *sidedelay* " für 7,1 Systeme.
-   Die [**ReverbConvertI3DL2ToNative**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative) -Funktion enthält jetzt den booleschen Parameter " *sevendotonereverb* ", der 7,1-Hall aktiviert.

## <a name="xaudio-28-windows-8x"></a>Xaudio2,8 (Windows 8. x)

XAudio2 Version 2,8 wird heute als Systemkomponente in Windows 8, XAudio2 \_8.DLL ausgeliefert. Es ist "Inbox" verfügbar und erfordert keine Neuverteilung mit einer App. Es wird empfohlen, das Windows Software Development Kit (SDK) für Windows 8 für die Entwicklung mit XAudio2 zu verwenden. der Windows SDK für Windows 8 enthält die erforderliche Header-und Import Bibliothek für die statische Verknüpfung mit XAUDIO2 \_8.DLL.

XAudio2 2,8 wurde mit den folgenden Änderungen aktualisiert:

-   Diese Version unterstützt die Entwicklung von Windows Store-Apps. die XAudio2-API kann in C++/DirectX Windows Store-Apps verwendet werden.
-   [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) ist ein flacher Win32-API-Rückruf, der keine XAudio2 CLSID mehr erstellt. Die Unterstützung für die Instanziierung von XAudio2 durch cokreatanstance wurde entfernt.
-   Die Initialize-Funktion wird jetzt vom Erstellungs Prozess implizit aufgerufen und aus der [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) -Schnittstelle entfernt.
-   Die Geräte Aufzählungs Funktion wurde aus XAudio2 entfernt; die Funktionen getdevicedetails und getdevicecount wurden aus der [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) -Schnittstelle entfernt. Apps, die auf anderen Audiogeräten auf dem System Renderinginformationen darstellen möchten, müssen eine gerätebezeichnerzeichenfolge anstelle eines Geräte Indexes an " [**kreatemasteringvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) " übergeben. Das standardaudiorendering-Gerät kann weiterhin ohne Enumeration erstellt werden.
-   [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) verfügt über die hinzugefügte Funktion [**IXAudio2MasteringVoice:: getchannelmask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) für, die die Kanalmaske für das Ziel Ausgabegerät zurückgibt.
-   Die [X3DAudio](x3daudio.md) -und [xapofx](xapofx-overview.md) -Bibliotheken werden in XAudio2 zusammengeführt. Der app-Code verwendet weiterhin separate Header, X3DAUDIO. H und xpofx. H, aber jetzt mit einer einzelnen Import Bibliothek verknüpft, XAUDIO2 \_ 8. lib.
-   xwma-Unterstützung ist in dieser Version von XAudio2 nicht verfügbar; xwma wird beim Aufrufen von createsourcevoice nicht als audiopufferformat unterstützt. Wir empfehlen nun das Media Foundation Quell-Lese Objekt, um eine Vielzahl von Medienformaten in in-Memory-PCM-Puffer zu decodieren.
-   " [**Kreatefx**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) " benötigt nun vier Parameter anstelle von zwei. Die neueren Parameter geben die Anfangsdaten im Rahmen der [xapofx](xapofx-overview.md) -Erstellung an.

## <a name="xaudio-27-and-earlier-windows-7"></a>Xaudioversion 2,7 und früher (Windows 7)

Alle früheren Versionen von XAudio2 für die Verwendung in-apps wurden als verteilbare DLLs im DirectX SDK bereitgestellt. Die erste Version von XAudio2, XAudio2 2,0, ausgeliefert in der Version vom März 2008 des DirectX SDK. Die letzte Version, die im DirectX SDK ausgeliefert werden soll, war XAudio2 2,7, verfügbar in der letzten Version des DirectX SDK im Juni 2010.

Das Legacy-DirectX SDK ist aufgrund der Deaktivierung aller mit SHA-1 signierten Inhalte nicht mehr in Microsoft-Downloads verfügbar. Der Juni 2010 war das Ende der Lebensdauer.

Frühere Versionen von XAudio2 können nicht zum Erstellen von Windows Store-Apps für Windows 8 verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte](getting-started.md)
</dt> <dt>

[XAudio2 Schlüsselkonzepte](xaudio2-key-concepts.md)
</dt> </dl>

[Entwicklerhandbuch für die weiterverteilbare Version von XAudio 2.9](xaudio2-redistributable.md)
</dt> </dl>
 

 
