---
title: What es New (Windows Media Format 11 SDK)
description: Neuerungen
ms.assetid: af04b99a-4653-4c82-944a-7005cf1181fe
keywords:
- Windows Medienformat-SDK, Neues
- Windows Medienformat-SDK, Features
- Windows Medienformat-SDK, neue Features
- Windows Medienformat-SDK, Erweiterte Client-APIs
- Windows Medienformat-SDK, DRM-Updates
- Windows Medienformat-SDK, Codecupdates
- Windows Medienformat-SDK, Miniaturansichten
- Digital Rights Management (DRM), neue Features
- DRM (Digital Rights Management), neue Features
- Miniaturansichtsbilder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1174078ce6fde94794cff32f4384de4a6c7b774dec2943fa91f2ec279d9d718e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963889"
---
# <a name="whats-new-windows-media-format-11-sdk"></a>What es New (Windows Media Format 11 SDK)

Das Windows Media Format 11 SDK führt neue DRM-Features (Digital Rights Management) ein. Seit release 9.5 wurden die folgenden Änderungen am SDK vorgenommen.

## <a name="windows-media-drm-client-extended-apis"></a>Windows Erweiterte APIs des Media DRM-Clients

Das Windows Media Format 11 SDK wird mit einem neuen Satz von DRM-APIs bereitgestellt. Diese APIs werden in ihrer eigenen Bibliothek implementiert. Viele der DRM-Features, die von den Objekten des Windows Media Format SDK unterstützt werden, werden auch von den erweiterten APIs des Windows Media DRM-Clients unterstützt. Der Hauptunterschied bei den neuen APIs ist, dass sie nicht darauf angewiesen sind, dass eine ASF-Datei funktioniert. Stattdessen befassen sich die neuen APIs direkt mit dem lokalen Lizenzspeicher und verwenden häufig die Schlüssel-ID, um Lizenzen zu identifizieren.

Weitere Informationen finden Sie in der Dokumentation Windows Media DRM Client Extended APIs (Erweiterte [APIs des Media DRM-Clients).](windows-media-drm-client-extended-apis.md)

## <a name="updated-codecs"></a>Aktualisierte Codecs

Der Windows Media Video 9 Advanced Profile-Codec wurde aktualisiert, um einen komprimierten Bitstream zu erzeugen, der mit dem veröffentlichten SMPTE VC-1-Standard kompatibel ist.

Der Windows Media Audio 10 Professional codec ist ebenfalls in dieser Version des SDK enthalten. Der neue Audiocodec bietet eine verbesserte Qualität mit niedrigeren Bitraten.

## <a name="thumbnail-right"></a>Miniaturansicht rechts

Anwendungen können eine neue DRM-Aktion anfordern, um aus Dem Video zu lesen und ein Miniaturbild zu erstellen. Dadurch können Anwendungen Miniaturbilder für Videodateien erstellen und anzeigen, ohne die Datei für die Wiedergabe zu öffnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




