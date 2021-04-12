---
description: Informationen zu Windows Media-Codecs
ms.assetid: C0B0265C-AD20-433B-A554-112AEB0208B9
title: Informationen zu Windows Media-Codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2240176de22682451814609abc94f33a52300563
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104218992"
---
# <a name="about-the-windows-media-codecs"></a>Informationen zu Windows Media-Codecs

-   [Windows Media Audio Codecs](#windows-media-audio-codecs)
    -   [Windows Media Audio 9](#windows-media-audio-9)
    -   [Windows Media Audio 10 Professional](#windows-media-audio-10-professional)
    -   [Windows Media Audio 9 verlustfreier](#windows-media-audio-9-lossless)
    -   [Windows Media Audio 9-Stimme](#windows-media-audio-9-voice)
    -   [Kompatibilität](#compatibility)
-   [Codecs der Windows Media Video 9-Serie](#windows-media-video-9-series-codecs)
    -   [Windows Media Video 9](#windows-media-video-9-series-codecs)
    -   [Windows Media Video 9-Bildschirm](#windows-media-video-9-screen)
    -   [Windows Media Video 9 Image Version 2](#windows-media-video-9-image-version-2)
    -   [Windows Media Video 9 VCM](#windows-media-video-9-vcm)
    -   [Kompatibilität](#compatibility)
-   [Zugehörige Themen](#related-topics)

## <a name="windows-media-audio-codecs"></a>Windows Media Audio Codecs

### <a name="windows-media-audio-9"></a>Windows Media Audio 9

Dieser Codec prüft Audiodaten bei 44,1 oder 48 Kilohertz (kHz) mit 16 Bits, ähnlich dem aktuellen CD-Standard, und bietet CD-Qualität bei den Datensätzen zwischen 64 und 192 kbit pro Sekunde (Kbit/s). Die resultierende Soundqualität ist 20 Prozent besser als audiostich Probe mit Windows Media Audio 8 zu den entsprechenden Datensätzen.

Der Windows Media Audio 9-Codec (WMA 9) unterstützt die variablenbitrate-Codierung (VBR), mit der sich die Codierungs Bitrate entsprechend der Komplexität der Audiodaten automatisch unterscheiden lässt. Mit VBR nimmt die Codierungs Bitrate zu, um komplexe Datenabschnitte aufzuzeichnen und dann zu verringern, um die Komprimierung der weniger komplexen Abschnitte zu maximieren und so eine kompakte, hochwertige Komprimierung zu erzielen.

WMA 9 ist abwärts kompatibel mit vorherigen Windows Media Audio kompatiblen Decodern. Dies bedeutet, dass WMA 9-Inhalte mit früheren Versionen von Windows Media Player oder älteren elektronischen Geräten, die Windows-Medien unterstützen, wiedergegeben werden können. Wie bei allen Codecs der Windows Media 9-Serie unterstützt es die Windows Media Digital Rights Management-Plattform, die zum sicheren Verpacken und Verteilen von kopiergeschützten digitalen Medien verwendet wird.

### <a name="windows-media-audio-10-professional"></a>Windows Media Audio 10 Professional

Windows Media Audio 10 Professional (WMA 10 pro) ist der flexibelste verfügbare Windows Media-Audio-Codec – unterstützende Profile, die alles von der Vollauflösung von 24-Bit-/96-kHz-Audiodaten in Stereo-, 5,1-Channel-oder sogar 7,1-channelumschließungs 256 128 96 Sound enthalten. WMA 10 pro bietet eine unglaubliche Qualität für Consumer, die High-Fidelity-Hardware und 5,1-channelumschließende Computer verwenden – und für Kunden, die Audioinhalte auf Ihren mobilen Geräten abspielen. WMA 10 pro unterstützt Streaming, progressiven Download oder eine Download-und Wiedergabe Bereitstellung bei 128 bis 768 Kbit/s.

Bei Verwendung von 5,1-Umschließungs audioaudiodaten, die auf 384 Kbit/s mit WMA 10 pro komprimiert sind, können die meisten Listener keine Unterschiede zwischen der komprimierten Musik und den ursprünglichen PCM-Dateien (Pulse Code Modulation) WMA Pro bietet auch dynamische Bereichs Steuerung mithilfe der maximalen und durchschnittlichen Audioverstärkung, die während des Codierungs Vorgangs berechnet werden. Mithilfe der Funktion für den stillen Modus in Windows Media Player 9 und höher können Benutzer entweder den vollständigen dynamischen Bereich, einen mittleren Differenz Bereich von bis zu 12 Dezimalstellen (DB) oberhalb des Durchschnitts oder einen geringfügigen Differenz Bereich von bis zu 6 dB über dem Durchschnitt hören.

Wenn ein Benutzer versucht, eine Datei wiederzugeben, die mit dem 5,1-Kanal codiert wurde, 24-Bit-, 96 kHz-samplingfunktionen, aber keine System-oder Soundkarte, die Multi-Channel-oder High-Resolution-Sound unterstützt, werden mehrere Kanäle in Stereo Audiodaten (z. b. 16-Bit, zwei Kanal-Audio) kombiniert, sodass Benutzer die beste Wiedergabe Funktionalität erhalten, die ihre Systeme bereitstellen können.

In der folgenden Tabelle wird WMA Pro mit konkurrierenden Komprimierungs Technologien verglichen.



| Audiodaten              | Branchen Komprimierung\*        | Windows-Medien\*            | Komprimierungs Einsparungen |
|-------------------------|-------------------------------|----------------------------|---------------------|
| 2 ch x 48 kHz x 16 Bits | Dolby Digital 2,0 bei 220 Kbit/s | WMA 10 pro mit 128 Kbit/s     | 1.7:1               |
| 6 ch x 48 kHz x 20 Bits | Dolby Digital 5,1 bei 384 Kbit/s | WMA 10 pro mit 192 – 256 KBit/s | 1.5 – 2:1             |
| 6 ch x 48 kHz x 24 Bits | DTS 5,1 bei 1.536 KBit/s         | WMA 10 pro mit 768 Kbit/s     | 2:1                 |



 

\* Inhalts abhängig

### <a name="windows-media-audio-9-lossless"></a>Windows Media Audio 9 verlustfreier

Die Audioqualität von Inhalten, die mit diesem Codec komprimiert werden, ist das Beste aus allen Windows Media Audio Codecs. Er erstellt ein Bit-für-Bit-Duplikat der ursprünglichen Audiodatei, sodass keine Daten verloren gehen, sodass es ideal für die Archivierung von Inhalts Mastern ist.

Abhängig von der Komplexität des Originals werden die Inhalte mit einem 2:1-oder 3:1-Verhältnis komprimiert. Obwohl dies niedriger ist als das Verhältnis, das mit anderen Codecs der Windows Media Audio 9-Serie erzielt wurde, bietet es dieselben Vorteile der Komprimierung, während die Daten intakt bleiben.

Wie Windows Media Audio 9 Professional bietet der Windows Media Audio 9 Verlust lose Codec auch dynamische Bereichs Steuerung mithilfe der maximalen und durchschnittlichen Audioverstärkung, die während des Codierungs Vorgangs berechnet werden. Mithilfe der Funktion für den stillen Modus in Windows Media Player 9 und höher können Benutzer den vollständigen dynamischen Bereich und einen mittleren Unterschied Bereich von bis zu 12 dB über dem Durchschnitt oder einen geringfügig großen Bereich von bis zu 6 dB über dem Durchschnitt hören.

### <a name="windows-media-audio-9-voice"></a>Windows Media Audio 9-Stimme

Dieser Low-Bit-Rate-Codec ist hauptsächlich für Sprachinhalte konzipiert, funktioniert aber sehr gut mit Inhalten im gemischten Modus, die Sprache und Musik enthalten. Im Sprachmodus nutzt der Codec den relativ weniger komplizierten und engeren Frequenzbereich der menschlichen Stimme, um die Komprimierung zu maximieren. Im Musik Modus verhält sich der Codec wie der Standard-Windows Media Audio 9-Codec. Codierter Inhalt kann so konfiguriert werden, dass der Sprach-und Musik Modus automatisch gewechselt wird.

Der Windows Media Audio 9 Voice-Codec bietet überlegene Qualität für Streamingszenarios mit geringem Bitrate (weniger als 20 kbit/s), z. b. Radiosendungen, Werbung, e-Books, Podcasts und Voiceovers. Der Voice-Codec kann Inhalte auch auf bis zu 4 Kbit/s bei 8 kHz komprimieren.

### <a name="compatibility"></a>Kompatibilität

In der folgenden Tabelle wird erläutert, was Ihre Zielgruppe bei der Wiedergabe Windows Media Audio 9-Serien Inhalts auf früheren Microsoft Windows-Betriebssystemen als Windows XP oder mit früheren Versionen von Windows Media Player hat. In dieser Tabelle werden auch die Kompatibilität für Apple Mac OS X und Windows CE – basierten Plattformen aufgeführt.



| Codec                              | Funktion                                       | Spieler-Abwärtskompatibilität                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Audio 9              | Codierung mit konstanter Bitrate (CBR)              | <dl> <dt>Windows Media Player 6,4 oder höher auf nicht tragbaren Geräten (unter Verwendung von Transcodierung bei Bedarf)</dt> <dt>Windows Media Player 9 für Mac OS X</dt> <dt>Windows Media Player 9-Serie und Windows Media Player 9,1 für \* Pocket PC</dt> <dt>Windows Media Player 9-Serie und Windows Media Player \* 9,1 für Smartphone</dt> </dl> |
|                                    | Variable-Bitrate-Codierung (VBR)              | Windows Media Player 7 oder höher auf allen Geräten, die den Player unterstützen (bei Bedarf mithilfe von Transcodierung)                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Media Audio 9 Professional | Allgemein                                       | <dl> <dt>Windows Media Player 7 oder</dt> höher <dt>Windows Media Player 9 für Mac OS X</dt> </dl>                                                                                                                                                                                                                                                                                                                          |
|                                    | Diskrete Kanal Wiedergabe (z.b. 5,1) | Erfordert Windows Media Player 9-Serie (oder SDK) oder höher, Windows XP und eine Multichannel-Audiokarte.                                                                                                                                                                                                                                                                                                                                                                                                                         |
|                                    | Hochauflösende Audiodaten (24-Bit, 96 kHz)        | Erfordert Windows Media Player 9-Serie (oder SDK) oder höher, Windows XP und eine hochauflösende Audiokarte.                                                                                                                                                                                                                                                                                                                                                                                                                      |
|                                    | Dynamisches Bereichs Steuerelement                         | Erfordert Windows Media Player 9-Serie (oder SDK) oder höher und Windows XP.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Windows Media Audio 9 verlustfreier     | Allgemein                                       | <dl> <dt>Windows Media Player 7 oder</dt> höher <dt>Windows Media Player 9 für Mac OS X</dt> </dl>                                                                                                                                                                                                                                                                                                                          |
|                                    | Diskrete Kanal Wiedergabe (z.b. 5,1) | Erfordert Windows Media Player 9-Serie (oder SDK) oder höher, Windows XP und eine Multichannel-Audiokarte.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Media Audio 9-Stimme        | Allgemein                                       | <dl> <dt>Windows Media Player 6,4 oder</dt> höher <dt>Windows Media Player 9 für Mac OS X</dt> <dt>Windows Media Player 9-Serie und Windows Media Player 9,1 für Pocket \* PC</dt> <dt>Windows Media Player 9-Serie und Windows Media Player 9,1 \* für Smartphone</dt> </dl>                                                       |



 

> [!Note]  
> \* Alle Versionen von Windows Media Player für Pocket PC und Smartphone werden als Teil des Betriebssystems Microsoft Windows Mobile ausgeliefert. Windows Media Player für Pocket PC und Windows Media Player für Smartphone können nicht von Microsoft heruntergeladen werden.

 

## <a name="windows-media-video-9-series-codecs"></a>Codecs der Windows Media Video 9-Serie

In 2006 veröffentlichte die Struktur der Motion Picture und TV Engineers (SMPTE) formal die endgültige Spezifikation für SMPTE 421m, auch bekannt als VC-1. Die formale Standardisierung von VC-1 repräsentiert die Dauer der technischen Überprüfung durch mehr als 75 Unternehmen, was zu einem Codec führt, der gut dokumentiert, äußerst stabil und leicht lizenzierbar ist und von der Branche akzeptiert wird. VC-1 unterstützt drei Profile: einfach, Main und erweitert. Die einfachen und Haupt Profile wurden seit einigen Jahren abgeschlossen, und vorhandene Implementierungen wie WMV 9 haben lange Unterstützung für die Erstellung und Wiedergabe von Inhalten mithilfe dieser Profile sowie eine frühe Implementierung des erweiterten Profils. Der Abschluss des erweiterten Profils und die anschließende Standardisierung aller Profile in VC-1 stellen den letzten Schritt in einer umfassenden Spezifikation dar, die hoch definierbare Inhalte bereitstellt – entweder über Schneid oder progressiv – über alle Mittel und bis hin zu jedem fähigen Gerät.

### <a name="windows-media-video-9"></a>Windows Media Video 9

Windows Media Video 9 ist die Microsoft-Implementierung des SMPTE-Standards VC-1. Es unterstützt einfache, zentrale und erweiterte Profile.

### <a name="simple-and-main-profiles"></a>Einfache und Haupt profile

Die Windows Media Video 9 Simple-und Main-Profile entsprechen vollständig dem SMPTE VC-1-Standard und bieten hochwertige Videos für das Streaming und das herunterladen. Diese Profile unterstützen eine Vielzahl von Bitraten, von einem hoch Definitions Inhalt von einem Drittel bis zu einem Drittel der Bitrate von MPEG-2 bis hin zu Low-Bitrate-Internet Videos, die über ein DFÜ-Modem geliefert werden. Dieser Codec unterstützt auch Videos mit professioneller Qualität mit zwei Pass-und variablen Bitraten (VBR-Codierung). Windows Media Video 9 wird bereits von einer Vielzahl von Playern und Geräten unterstützt.

### <a name="advanced-profile"></a>Erweitertes Profil

Das erweiterte Profil Windows Media Video 9 entspricht vollständig dem SMPTE VC-1-Standard, unterstützt Zeilen Sprung Inhalte und ist Transport unabhängig. Inhalts Ersteller können dieses Profil verwenden, um progressiv-oder Zeilen Sprung Inhalte zu Datensätzen zu liefern, die niedriger als ein Drittel des MPEG-2-Codecs – mit der gleichen Qualität wie MPEG-2.

In der Vergangenheit war der Zeilen Sprung Videoinhalt vor der Codierung mit dem Windows Media Video Codec immer deaktiviert. Jetzt kann das Codieren von Anwendungen wie Windows Media 9-Serien und Codierungs Lösungen von Drittanbietern die Komprimierung von Zeilen Sprung Inhalten unterstützen, ohne Sie zunächst in progressiven Inhalt umzuwandeln. Die Beibehaltung von Zeilen Sprung in einer codierten Datei ist wichtig, wenn der Inhalt jemals auf einer Zeilen Sprung Anzeige, z. b. einem Fernsehen, gerendert wird.

Die Transport Unabhängigkeit ermöglicht außerdem die Übermittlung von Windows Media Video 9 Advanced Profile über Systeme, die nicht auf Windows-Medien basieren, wie z. b. Standard basierte Broadcast Infrastrukturen (durch systemeigene MPEG-2-Transportdaten Ströme), drahtlos Infrastrukturen (über \[ RTP von RTP in Echtzeit \] ) oder sogar DVDs.

In der folgenden Tabelle wird Windows Media Video 9 Advanced Profile mit der konkurrierenden Komprimierungs Technologie verglichen.



| Video Daten                                                  | Branchen Komprimierung\* | Windows-Medien\*                                      | Komprimierungs Einsparungen |
|-------------------------------------------------------------|------------------------|------------------------------------------------------|---------------------|
| 480/24p 720x480 Pixel/Frame x 8 Bits pro Kanal x 24 fps  | MPEG-2 bei 4 – 6 MBit/s     | Windows Media Video 9 Advanced Profile bei 1,3 – 2 Mbit/s | 3:1                 |
| 480/30i 720x480 Pixel/Frame x 8 Bits pro Kanal x 30 fps  | MPEG-2 bei 6 – 8 Mbit/s     | Windows Media Video 9 Advanced Profile bei 2 – 4 Mbit/s   | 2 – 3:1               |
| 720/24p 1.280 x 720 Pixel/Frame x 8 Bits pro Kanal x 24 fps | MPEG-2 mit 19 Mbit/s      | Windows Media Video 9 Advanced Profile bei 5 – 8 Mbit/s   | 2.4 – 3.8:1           |



 

\*Inhalts abhängig

### <a name="windows-media-video-9-screen"></a>Windows Media Video 9-Bildschirm

Der Windows Media Video 9-Bildschirm Codec ist für das Komprimieren von sequenziellen Screenshots und hochgradig statischem Video optimiert, das von der Computer Anzeige erfasst wird, sodass es ideal für die Bereitstellung von Demos oder die Veranschaulichung der Computer Verwendung für Schulungen geeignet ist. Der Codec nutzt die typische Bild Einfachheit und den relativen Mangel an Bewegung, um ein sehr hohes Komprimierungs Verhältnis zu erzielen.

Während des Codierungs Prozesses wechselt der Codec abhängig von der Komplexität der Videodaten automatisch zwischen Verlust und verlustfreier Codierungs Modi. Bei komplexen Daten behält der Modus ohne Verlust eine exakte Kopie der Daten bei. Bei weniger komplexen Daten verwirft der Verlust Modus einige Daten, um ein höheres Komprimierungs Verhältnis zu erzielen. Durch automatisches Wechseln zwischen diesen beiden Modi behält der Codec die Videoqualität bei und maximiert gleichzeitig die Komprimierung.

Insgesamt bietet das Windows Media Video 9-Bildschirm Codec eine bessere Handhabung von Bitmapbildern und Bildschirm Bewegung, auch bei relativ gering fühenden CPUs. Es ist auch bis zu 100-mal effizienter als die häufig verwendete Lauflängen Codierung.

### <a name="windows-media-video-9-image-version-2"></a>Windows Media Video 9 Image Version 2

Das Windows Media Video 9-Abbild Version 2-Codec unterscheidet sich von anderen Video Codecs. Anstatt unkomprimierte Videos zu verarbeiten, werden Bilder mithilfe von schwenken, Zoom und übergreifenden Übergängen zwischen Clips immer noch in Videos transformiert, um eine unbegrenzte Anzahl von Effekten zu erzielen.

Die Ergebnisse können dann mit einer Daten Rate von bis zu 20 kbit pro Sekunde (Kbit/s) zugestellt werden. Diese Dateien werden entweder mit konstanter Bitrate (CBR) oder mit einpass-VBR-Modi (Variable Bitrate) komprimiert.

> [!Note]  
> Der Windows Media Video 9-Abbild Version 2-Codec ist nicht mit dem Windows Media Video 9-Bildcodec kompatibel.

 

### <a name="windows-media-video-9-vcm"></a>Windows Media Video 9 VCM

Mit der Video Compression Manager-Version (VCM) des Codecs der Windows Media Video 9-Serie können frühere Versionen von Codierungs-und Bearbeitungsanwendungen den Windows Media Video 9-Serie-Codec in Datei Containern wie Audio Video Interleaved (AVI) unterstützen. Mit diesem Codec-Paket können auch Windows Media Video (WMV)-Dateien, die auf der Serie Windows Media Format 9 basieren, in Windows Media Player 6,4 in den Dateien "ASF" und "AVI" abgespielt werden.

### <a name="compatibility"></a>Kompatibilität

In der folgenden Tabelle wird beschrieben, was Ihre Zielgruppe bei der Wiedergabe von Windows Media Video 9-Serien Inhalten unter früheren Microsoft Windows-Betriebssystemen oder früheren Versionen von Windows Media Player hat. In dieser Tabelle werden auch die Kompatibilität für Apple Mac OS X und Windows CE – basierten Plattformen aufgeführt.



| Codec                                  | Funktion             | Spieler-Abwärtskompatibilität                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Video 9                  | Allgemein             | <dl> <dt>Windows Media Player 6,4 oder</dt> höher <dt>Windows Media Player 9 für Mac OS X</dt> <dt>Windows Media Player 9-Serie und Windows Media Player 9,1 für Pocket \* PC</dt> <dt>Windows Media Player 9-Serie und Windows Media Player 9,1 \* für Smartphone</dt> </dl> |
|                                        | Frame Interpolation | Erfordert Windows Media Player 9-Serie (oder Software Development Kit) oder höher und Windows XP.                                                                                                                                                                                                                                                                                                                                                                           |
| Erweiterte profile Windows Media Video 9 | Allgemein             | Windows Media Player 7 oder höher                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Media Video 9-Bildschirm           | Allgemein             | Windows Media Player 7 oder höher                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Windows Media Video 9 Image Version 2  | Allgemein             | Windows Media Player 7 oder höher                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

> [!Note]  
> \*Alle Versionen von Windows Media Player für Pocket PC und Smartphone werden als Teil des Betriebssystems Microsoft Windows Mobile ausgeliefert. Windows Media Player für Pocket PC und Windows Media Player für Smartphone können nicht von Microsoft heruntergeladen werden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Media-Codecs](windows-media-codecs.md)
</dt> </dl>

 

 



