---
title: System profile
description: System profile
ms.assetid: 5f687aae-cf9b-4b2d-a3aa-d130b443fbf3
keywords:
- Windows Media-Format-SDK, Systemprofile
- Advanced Systems Format (ASF), Systemprofile
- ASF (Advanced Systems Format), Systemprofile
- Windows Media-Format-SDK, Profil-IDs
- Advanced Systems Format (ASF), Profil-IDs
- ASF (Advanced Systems Format), Profil-IDs
- Systemprofile, Liste der
- Profil-IDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeca66023e6de6aba9c07a6bcb84a73756e316a8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723584"
---
# <a name="system-profiles"></a>System profile

Die folgende Tabelle enthält die vollständige Liste der unterstützten Systemprofile. Jedes aufgeführte Profil weist einen Namen und eine Profil-ID auf. Die Profil-ID ist eine Konstante, die auf den dem Systemprofil zugewiesenen GUID-Wert festgelegt ist. Um die Systemprofil-IDs in Ihrem Code zu verwenden, müssen Sie wmsysprf. h in Ihre Anwendung einschließen. Beispiele zum Laden von Systemprofilen finden [Sie unter So laden Sie ein Systemprofil](to-load-a-system-profile.md).

> [!IMPORTANT]
> Die unten aufgeführten Profile verwenden die Windows Media Audio und Windows Media Video Codecs der Version 8. Es sind keine vordefinierten Systemprofile vorhanden, die die Codecs der Windows Media 9-Serie verwenden. Sie können ein eigenes Windows Media 9-Serien Profil erstellen, indem Sie ein Profil der Version 8 als Ausgangspunkt verwenden. Weitere Informationen finden Sie unter [wieder verwenden von streamkonfigurationen](reusing-stream-configurations.md).

 



| Profilname                                                                      | Profil-ID                     | BESCHREIBUNG                                                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Video 8 für Farb Pocket PCs (225 Kbit/s)                             | Wmprofile \_ V80 \_ 255 videopda    | Verwenden Sie dieses Profil beim Erstellen von Videodateien für die Wiedergabe auf schnelleren Farb Pocket PCs.                                                                                 |
| Windows Media Video 8 für Farb Pocket PCs (150 KBit/s)                             | Wmprofile \_ V80 \_ 150videopda    | Verwenden Sie dieses Profil beim Erstellen von Videodateien für die Wiedergabe auf den meisten Pocket PCs.                                                                                         |
| Windows Media Video 8 für Einwählmodems oder ISDN mit einem Kanal (28,8 bis 56 Kbit/s) | Wmprofile \_ V80 \_ 28856videombr  | Verwenden Sie dieses mehrbitrate-Profil für Zielgruppen mit DFÜ-Modems oder ISDN-Verbindungen mit einem Kanal (Bandbreite zwischen 28,8 Kbit/s und 56 Kbit/s).        |
| Windows Media Video 8 für LAN, Kabel Modem oder xDSL (100 bis 768 Kbit/s)             | Wmprofile \_ V80 \_ 100768videombr | Verwenden Sie dieses Multi-Bitrate-Profil für Zielgruppen mit Dual-Channel-ISDN, LAN, Kabelmodem oder xDSL-Verbindungen (Bandbreite zwischen 100 kbit/s und 500 KBit/s). |
| Windows Media Video 8 für Einwählmodems oder LAN (28,8 bis 100 kbit/s)                | Wmprofile \_ V80 \_ 288100videombr | Verwenden Sie dieses mehrbitrate-Profil für Zielgruppen mit DFÜ-Modem-, LAN-oder Dual-Channel-ISDN-Verbindungen (Bandbreite zwischen 28,8 und 100 kbit/s).         |
| Windows Media Video 8 für Einwählmodems (28,8 Kbit/s)                              | Wmprofile \_ V80 \_ 288-Video       | Verwenden Sie dieses Profil für die Low-Bit-audiobereitstellung über 28,8 Kbit/s mit DFÜ-Verbindungen.                                                                          |
| Windows Media Video 8 für Einwählmodems (56 Kbit/s)                                | Wmprofile \_ V80 \_ 56video        | Verwenden Sie dieses Profil für die Low-Bit-audiobereitstellung über 56 Kbit/s mit DFÜ-Verbindungen.                                                                            |
| Windows Media Video 8 für lokales Netzwerk (100 kbit/s)                           | Wmprofile \_ V80 \_ 100Video       | Verwenden Sie dieses Profil für die mittlere Bitrate-Übermittlung über Dual-Channel-ISDN-, LAN-oder Kabelmodem Verbindungen.                                                              |
| Windows Media Video 8 für lokales Netzwerk (256 KBit/s)                           | Wmprofile \_ V80 \_ 256-Video       | Verwenden Sie dieses Profil für hochwertige Audioinhalte und Videoinhalte, die für die lokale Wiedergabe oder für Download und Wiedergabe gedacht sind.                                                     |
| Windows Media Video 8 für lokales Netzwerk (384 Kbit/s)                           | Wmprofile \_ V80 \_ 384-Video       | Verwenden Sie dieses Profil für hochwertige Audioinhalte und Videoinhalte, die für die lokale Wiedergabe oder für Download und Wiedergabe gedacht sind.                                                     |
| Windows Media Video 8 für lokales Netzwerk (768 Kbit/s)                           | Wmprofile \_ V80 \_ 768-Video       | Verwenden Sie dieses Profil für hochwertige Audioinhalte und Videoinhalte, die für die lokale Wiedergabe oder für Download und Wiedergabe gedacht sind.                                                     |
| Windows Media Video 8 für Breitband (NTSC, 700 Kbit/s)                              | Wmprofile \_ V80 \_ 700 ntscvideo   | Verwenden Sie dieses Profil für hochwertige Audioinhalte und Videoinhalte, die für die lokale Wiedergabe oder Download und Wiedergabe gedacht sind.                                                         |
| Windows Media Video 8 für Breitband (NTSC, 1400 Kbit/s)                             | Wmprofile \_ V80 \_ 1400ntscvideo  | Verwenden Sie dieses Profil für hochwertige Audioinhalte und Videoinhalte, die für die lokale Wiedergabe oder für Download und Wiedergabe gedacht sind.                                                     |
| Windows Media Video 8 für Breitband (PAL, 384 Kbit/s)                               | Wmprofile \_ V80 \_ 384palvideo    | Verwenden Sie dieses Profil für hochwertige Audioinhalte und Videoinhalte, die für die lokale Wiedergabe oder für Download und Wiedergabe gedacht sind.                                                     |
| Windows Media Video 8 für Breitband (PAL, 700 Kbit/s)                               | Wmprofile \_ V80 \_ 700palvideo    | Verwenden Sie dieses Profil für hochwertige Audioinhalte und Videoinhalte, die für die lokale Wiedergabe oder für Download und Wiedergabe gedacht sind.                                                     |
| Windows Media Audio 8 für das Einwählmodem (Mono, 28,8 Kbit/s)                         | Wmprofile \_ V80 \_ 288monoaudiodatei   | Verwenden Sie dieses Profil für Radio-und Musikinhalte (nur Audiodaten).                                                                                                          |
| Windows Media Audio 8 für das Einwählmodem (FM Radio Stereo, 28,8 Kbit/s)              | Wmprofile \_ V80 \_ 288stereoaudiodatei | Verwenden Sie dieses Profil für Radio-und Musikinhalte (nur Audiodaten).                                                                                                          |
| Windows Media Audio 8 für das Einwählmodem (32 Kbit/s)                                 | Wmprofile \_ V80 \_ 32stereoaudiodatei  | Verwenden Sie dieses Profil für Radio-und Musikinhalte (nur Audiodaten).                                                                                                          |
| Windows Media Audio 8 für DFÜ-Modem (Near CD Quality, 48 Kbit/s)                | Wmprofile \_ V80 \_ 48stereoaudiodatei  | Verwendung für Radio-, Musik-und allgemeine Audioinhalte.                                                                                                            |
| Windows Media Audio 8 für DFÜ-Modem (CD-Qualität, 64 Kbit/s)                     | Wmprofile \_ V80 \_ 64stereoaudiodatei  | Verwenden Sie dieses Profil für Zielgruppen mit hoher Geschwindigkeit von Internet-oder LAN-Verbindungen.                                                                                  |
| Windows Media Audio 8 für ISDN (besser als CD-Qualität, 96 Kbit/s)                  | Wmprofile \_ V80 \_ 96stereoaudiodatei  | Verwenden Sie dieses Profil für Zielgruppen mit hoher Geschwindigkeit von Internet-oder LAN-Verbindungen.                                                                                  |
| Windows Media Audio 8 für ISDN (besser als CD-Qualität, 128 Kbit/s)                 | Wmprofile \_ V80 \_ 128 stereoaudiodatei | Verwenden Sie dieses Profil für Zielgruppen mit hoher Geschwindigkeit von Internet-oder LAN-Verbindungen.                                                                                  |
| Windows Media Video 8 für das Einwählmodem (keine Audiodaten, 28,8 Kbit/s)                     | Wmprofile \_ V80 \_ 288videoonly   | Verwenden Sie dieses Profil, wenn Sie nur-Video-Inhalte für Zielgruppen mit DFÜ-Modems erstellen.                                                                         |
| Windows Media Video 8 für das Einwählmodem (keine Audiodaten, 56 Kbit/s)                       | Wmprofile \_ V80 \_ 56videoonly    | Verwenden Sie dieses Profil, wenn Sie nur-Video-Inhalte für Zielgruppen mit DFÜ-Modems erstellen.                                                                         |
| Windows Media 8 Fair Quality based VBR for Breitband                              | Wmprofile \_ V80 \_ fairvbrvideo   | Auf hoher Qualität basierendes Profil für VBR-Inhalte, die mit eingeschränkter Qualität eingeschränkt sind.                                                                                     |
| Windows Media 8 High Quality based VBR for Breitband.                             | Wmprofile \_ V80 \_ highvbrvideo   | High-to-Quality-basiertes Profil für VBR-Inhalte, die mit eingeschränkter Qualität eingeschränkt sind.                                                                                     |
| Windows Media 8 Best Quality based VBR for Breitband.                             | Wmprofile \_ V80 \_ bestvbrvideo   | Bestes Qualitäts basiertes Profil für VBR-Inhalte, die mit eingeschränkter Qualität eingeschränkt sind.                                                                                             |



 

Die Systemprofile sind in anderen Sprachen als Englisch verfügbar. Weitere Informationen finden Sie unter [lokalisierte System profile](localized-system-profiles.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmprofilemanager:: loadprofilebyid**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)
</dt> <dt>

[**IWMProfileManager2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)
</dt> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> </dl>

 

 




