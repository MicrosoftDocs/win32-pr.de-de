---
description: Medien Puffer
ms.assetid: 3ee073ea-7bac-4971-9167-93a4e541ab77
title: Medien Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87316ea64e24173dfa73f2cc2ff280a1281d50f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361769"
---
# <a name="media-buffers"></a>Medien Puffer

Ein Medien Puffer ist ein COM-Objekt, das einen Speicherblock verwaltet, der normalerweise Mediendaten enthält. Medien Puffer werden verwendet, um Daten von einer Pipeline Komponente in die nächste zu verschieben. Die meisten Anwendungen verwenden keine Medien Puffer direkt, da die Medien Sitzung den gesamten Datenfluss zwischen Pipeline Objekten verarbeitet. Sie müssen Medien Puffer verwenden, wenn Sie eine eigene Pipeline Komponente schreiben, oder wenn Sie eine Pipeline Komponente direkt ohne die Medien Sitzung verwenden.

Medien Puffer machen die [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) -Schnittstelle verfügbar. Diese Schnittstelle ist für das Lesen oder schreiben beliebiger Datentypen konzipiert. Nicht komprimierte Videorahmen erfordern eine besondere Behandlung, da Sie möglicherweise in Direct3D-Oberflächen gespeichert werden, die sich im Videospeicher befinden.

In diesem Abschnitt werden die folgenden Themen behandelt:



| Thema                                                        | BESCHREIBUNG                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [Arbeiten mit Medien Puffern](working-with-media-buffers.md) | Beschreibt das allgemeine Verhalten von Medien Puffern für alle Medientypen. |
| [Nicht komprimierte Video Puffer](uncompressed-video-buffers.md) | Arbeiten mit Medien Puffern, die nicht komprimierte Video Frames enthalten.  |
| [DirectX-Oberflächen Puffer](directx-surface-buffer.md)         | Beschreibt, wie eine Direct3D-Oberfläche in einem Medien Puffer gespeichert wird.         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation primitiver](media-foundation-primitives.md)
</dt> </dl>

 

 



