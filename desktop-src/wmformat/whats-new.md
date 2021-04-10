---
title: Neuigkeiten (Windows Media-Format 11 SDK)
description: Neuerungen
ms.assetid: af04b99a-4653-4c82-944a-7005cf1181fe
keywords:
- Windows Media-Format-SDK, Neuerungen
- Windows Media-Format-SDK, Features
- Windows Media-Format-SDK, neue Funktionen
- Windows Media-Format-SDK, erweiterte Client-APIs
- Windows Media-Format-SDK, DRM-Updates
- Windows Media-Format-SDK, Codec-Updates
- Windows Media-Format-SDK, Miniaturbilder
- Digital Rights Management (DRM), neue Features
- DRM (Digital Rights Management), neue Features
- Miniaturansichtsbilder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63d85f00f89f940ab22754d1f6f458430868d7c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739504"
---
# <a name="whats-new-windows-media-format-11-sdk"></a>Neuigkeiten (Windows Media-Format 11 SDK)

Das SDK für Windows Media-Format 11 führt neue Features für Digital Rights Management (DRM) ein. Die folgenden Änderungen wurden seit der Version 9,5 an dem SDK vorgenommen.

## <a name="windows-media-drm-client-extended-apis"></a>Erweiterte APIs für den Windows Media DRM-Client

Das SDK für Windows Media-Format 11 ist mit einem neuen Satz von DRM-APIs ausgeliefert. Diese APIs werden in ihrer eigenen Bibliothek implementiert. Viele der DRM-Features, die von den Objekten des Windows Media Format SDK unterstützt werden, werden auch von den erweiterten APIs des Windows Media DRM-Clients unterstützt. Der Hauptunterschied zwischen den neuen APIs besteht darin, dass Sie sich nicht darauf verlassen, dass eine ASF-Datei funktioniert. Stattdessen befassen sich die neuen APIs direkt mit dem lokalen Lizenz Speicher, wobei häufig die Schlüssel-ID zur Identifizierung von Lizenzen verwendet wird.

Weitere Informationen finden Sie in der Dokumentation zu [erweiterten APIs für den Windows Media DRM-Client](windows-media-drm-client-extended-apis.md) .

## <a name="updated-codecs"></a>Aktualisierte Codecs

Der erweiterte profilcodec von Windows Media Video 9 wurde aktualisiert, um einen komprimierten Bitstream zu erstellen, der mit dem veröffentlichten SMPTE VC-1-Standard kompatibel ist.

Der Windows Media Audio 10 Professional-Codec ist auch in dieser Version des SDK enthalten. Der neue Audiocodec bietet verbesserte Qualität bei niedrigeren Bitraten.

## <a name="thumbnail-right"></a>Miniaturansicht rechts

Anwendungen können eine neue DRM-Aktion zum Lesen aus dem Video anfordern, um ein Miniaturbild zu erstellen. Dadurch können Anwendungen Miniaturbilder für Videodateien erstellen und anzeigen, ohne die Datei für die Wiedergabe zu öffnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Windows Media-Format-SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




