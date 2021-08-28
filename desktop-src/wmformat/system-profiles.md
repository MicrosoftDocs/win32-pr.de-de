---
title: Systemprofile
description: Systemprofile
ms.assetid: 5f687aae-cf9b-4b2d-a3aa-d130b443fbf3
keywords:
- Windows Medienformat-SDK, Systemprofile
- Advanced Systems Format (ASF), Systemprofile
- ASF (Advanced Systems Format), Systemprofile
- Windows Medienformat-SDK, Profil-IDs
- Advanced Systems Format (ASF), Profil-IDs
- ASF (Advanced Systems Format), Profil-IDs
- Systemprofile, Liste der
- Profil-IDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6389f82e93a0b27c079bd75ded9eb7d35d78a380ab72d244c5443c07f4c9ed5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807740"
---
# <a name="system-profiles"></a>Systemprofile

Die folgende Tabelle enthält die vollständige Liste der unterstützten Systemprofile. Jedes aufgelistete Profil verfügt über einen Namen und eine Profil-ID. Die Profil-ID ist eine Konstante, die auf den GUID-Wert festgelegt ist, der dem Systemprofil zugewiesen ist. Um die Systemprofil-IDs in Ihrem Code zu verwenden, müssen Sie wmsysprf.h in Ihre Anwendung einschließen. Beispiele zum Laden eines Systemprofils finden Sie unter [So laden Sie ein Systemprofil.](to-load-a-system-profile.md)

> [!IMPORTANT]
> Die unten aufgeführten Profile verwenden alle die Version 8 Windows Medienaudio- und Windows Media Video-Codecs. Es gibt keine vordefinierten Systemprofile, die die Codecs der Windows Media 9-Serie verwenden. Sie können ein eigenes Profil Windows Media 9-Serie erstellen, indem Sie ein Profil der Version 8 als Ausgangspunkt verwenden. Weitere Informationen finden Sie unter [Wiederverwenden von Streamkonfigurationen.](reusing-stream-configurations.md)

 



| Profilname                                                                      | Profil-ID                     | Beschreibung                                                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Video 8 für Color Pocket PCs (225 KBit/s)                             | WMProfile \_ V80 \_ 255VideoPDA    | Verwenden Sie dieses Profil, wenn Sie Videodateien für die Wiedergabe auf schnelleren Color Pocket-PCs erstellen.                                                                                 |
| Windows Media Video 8 für Color Pocket PCs (150 KBit/s)                             | WMProfile \_ V80 \_ 150VideoPDA    | Verwenden Sie dieses Profil, wenn Sie Videodateien für die Wiedergabe auf den meisten Pocket-PCs erstellen.                                                                                         |
| Windows Media Video 8 für Dial-up Modems oder Single-Channel ISDN (28,8 bis 56 KBit/s) | WMProfile \_ V80 \_ 28856VideoMBR  | Verwenden Sie dieses Profil mit mehreren Bitraten für Zielgruppen mit DFÜ-Modems oder ISDN-Verbindungen mit einem Kanal (Bandbreite zwischen 28,8 KBit/s und 56 KBit/s).        |
| Windows Media Video 8 für LAN, Kabelmodem oder xDSL (100 bis 768 KBit/s)             | WMProfile \_ V80 \_ 100768VideoMBR | Verwenden Sie dieses Profil mit mehreren Bitraten für Zielgruppen mit DUAL-Channel-ISDN-, LAN-, Kabelmodem- oder xDSL-Verbindungen (Bandbreite zwischen 100 KBit/s und 500 KBit/s). |
| Windows Media Video 8 für DFÜ-Modems oder LAN (28,8 bis 100 KBit/s)                | WMProfile \_ V80 \_ 288100VideoMBR | Verwenden Sie dieses Profil mit mehreren Bitraten für Zielgruppen mit DFÜ-Modem-, LAN- oder DUAL-Channel-ISDN-Verbindungen (Bandbreite zwischen 28,8 und 100 KBit/s).         |
| Windows Media Video 8 für DFÜ-Modems (28,8 KBit/s)                              | WMProfile \_ V80 \_ 288Video       | Verwenden Sie dieses Profil für die Audio-/Videoübermittlung mit niedriger Bitrate über DFÜ-Verbindungen mit 28,8 KBit/s.                                                                          |
| Windows Media Video 8 für DFÜ-Modems (56 KBit/s)                                | WMProfile \_ V80 \_ 56Video        | Verwenden Sie dieses Profil für die Audio-/Videoübermittlung mit niedriger Bitrate über DFÜ-Verbindungen mit 56 KBit/s.                                                                            |
| Windows Media Video 8 for Local Area Network (100 KBit/s)                           | WMProfile \_ V80 \_ 100Video       | Verwenden Sie dieses Profil für die Übermittlung mittlerer Bitraten über DUAL-Channel-ISDN-, LAN- oder Kabelmodemverbindungen.                                                              |
| Windows Media Video 8 for Local Area Network (256 KBit/s)                           | WMProfile \_ V80 \_ 256Video       | Verwenden Sie dieses Profil für qualitativ hochwertige Audio-/Videoinhalte, die für die lokale Wiedergabe oder zum Herunterladen und Wiedergeben vorgesehen sind.                                                     |
| Windows Media Video 8 for Local Area Network (384 KBit/s)                           | WMProfile \_ V80 \_ 384Video       | Verwenden Sie dieses Profil für qualitativ hochwertige Audio-/Videoinhalte, die für die lokale Wiedergabe oder zum Herunterladen und Wiedergeben vorgesehen sind.                                                     |
| Windows Media Video 8 für lokales Netzwerk (768 KBit/s)                           | WMProfile \_ V80 \_ 768Video       | Verwenden Sie dieses Profil für qualitativ hochwertige Audio-/Videoinhalte, die für die lokale Wiedergabe oder zum Herunterladen und Wiedergeben vorgesehen sind.                                                     |
| Windows Media Video 8 für Breitband (NTSC, 700 KBit/s)                              | WMProfile \_ V80 \_ 700NTSCVideo   | Verwenden Sie dieses Profil für qualitativ hochwertige Audio-/Videoinhalte, die für die lokale Wiedergabe oder das Herunterladen und Wiedergeben vorgesehen sind.                                                         |
| Windows Media Video 8 für Breitband (NTSC, 1400 KBit/s)                             | WMProfile \_ V80 \_ 1400NTSCVideo  | Verwenden Sie dieses Profil für qualitativ hochwertige Audio-/Videoinhalte, die für die lokale Wiedergabe oder zum Herunterladen und Wiedergeben vorgesehen sind.                                                     |
| Windows Media Video 8 für Breitband (PAL, 384 KBit/s)                               | WMProfile \_ V80 \_ 384PALVideo    | Verwenden Sie dieses Profil für qualitativ hochwertige Audio-/Videoinhalte, die für die lokale Wiedergabe oder zum Herunterladen und Wiedergeben vorgesehen sind.                                                     |
| Windows Media Video 8 für Breitband (PAL, 700 KBit/s)                               | WMProfile \_ V80 \_ 700PALVideo    | Verwenden Sie dieses Profil für qualitativ hochwertige Audio-/Videoinhalte, die für die lokale Wiedergabe oder zum Herunterladen und Wiedergeben vorgesehen sind.                                                     |
| Windows Medienaudio 8 für Einwählmodem (Mono, 28,8 KBit/s)                         | WMProfile \_ V80 \_ 288MonoAudio   | Verwenden Sie dieses Profil für Radio- und Musikinhalte (nur Audio).                                                                                                          |
| Windows Medienaudio 8 für DFÜ-Modem (FM Radio Stereo, 28,8 KBit/s)              | WMProfile \_ V80 \_ 288StereoAudio | Verwenden Sie dieses Profil für Radio- und Musikinhalte (nur Audio).                                                                                                          |
| Windows Medienaudio 8 für DFÜ-Modem (32 KBit/s)                                 | WMProfile \_ V80 \_ 32StereoAudio  | Verwenden Sie dieses Profil für Radio- und Musikinhalte (nur Audio).                                                                                                          |
| Windows Medienaudio 8 für DFÜ-Modem (Nahezu CD-Qualität, 48 KBit/s)                | WMProfile \_ V80 \_ 48StereoAudio  | Wird für Radio-, Musik- und allgemeine Audioinhalte verwendet.                                                                                                            |
| Windows Medienaudio 8 für DFÜ-Modem (CD-Qualität, 64 KBit/s)                     | WMProfile \_ V80 \_ 64StereoAudio  | Verwenden Sie dieses Profil für Zielgruppen mit Hochgeschwindigkeits-Internet- oder LAN-Verbindungen.                                                                                  |
| Windows Medienaudio 8 für ISDN (besser als CD-Qualität, 96 KBit/s)                  | WMProfile \_ V80 \_ 96StereoAudio  | Verwenden Sie dieses Profil für Zielgruppen mit Hochgeschwindigkeits-Internet- oder LAN-Verbindungen.                                                                                  |
| Windows Medienaudio 8 für ISDN (besser als CD-Qualität, 128 KBit/s)                 | WMProfile \_ V80 \_ 128StereoAudio | Verwenden Sie dieses Profil für Zielgruppen mit Hochgeschwindigkeits-Internet- oder LAN-Verbindungen.                                                                                  |
| Windows Media Video 8 für Dial-up Modem (No audio, 28,8 KBit/s)                     | WMProfile \_ V80 \_ 288VideoOnly   | Verwenden Sie dieses Profil, wenn Sie Nur-Video-Inhalte für Zielgruppen mit DFÜ-Modems erstellen.                                                                         |
| Windows Media Video 8 for Dial-up Modem (No audio, 56 KBit/s)                       | WMProfile \_ V80 \_ 56VideoOnly    | Verwenden Sie dieses Profil, wenn Sie Nur-Video-Inhalte für Zielgruppen mit DFÜ-Modems erstellen.                                                                         |
| Windows Media 8 Fair Quality-basierte VBR für Breitband                              | WMProfile \_ V80 \_ FAIRVBRVideo   | Faires bis qualitativ hochwertiges Profil für VBR-Inhalte, die von der Qualität eingeschränkt sind.                                                                                     |
| Windows Media 8 High Quality based VBR for Broadband.                             | WMProfile \_ V80 \_ HIGHVBRVideo   | Auf hoher bis optimaler Qualität basierendes Profil für VBR-Inhalte mit eingeschränkter Qualität.                                                                                     |
| Windows Media 8 Best Quality-basierte VBR für Breitband.                             | WMProfile \_ V80 \_ BESTVBRVideo   | Bestes qualitätsbasiertes Profil für VBR-Inhalte mit eingeschränkter Qualität.                                                                                             |



 

Die Systemprofile sind für andere Sprachen als Englisch lokalisiert verfügbar. Weitere Informationen finden Sie unter [Lokalisierte Systemprofile.](localized-system-profiles.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)
</dt> <dt>

[**IWMProfileManager2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)
</dt> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> </dl>

 

 




