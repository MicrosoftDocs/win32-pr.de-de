---
description: Medienpuffer
ms.assetid: 3ee073ea-7bac-4971-9167-93a4e541ab77
title: Medienpuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ef02570ab994f0a15a9b53f2df8a0ac0b96a91a3bf3f260c1bcc5f866ade87e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827510"
---
# <a name="media-buffers"></a>Medienpuffer

Ein Medienpuffer ist ein COM-Objekt, das einen Speicherblock verwaltet, in der Regel zum Speichern von Mediendaten. Medienpuffer werden verwendet, um Daten von einer Pipelinekomponente zur nächsten zu verschieben. Die meisten Anwendungen verwenden Medienpuffer nicht direkt, da die Mediensitzung den gesamten Datenfluss zwischen Pipelineobjekten verarbeitet. Sie müssen Medienpuffer verwenden, wenn Sie Eine eigene Pipelinekomponente schreiben, oder wenn Sie eine Pipelinekomponente direkt ohne die Mediensitzung verwenden.

Medienpuffer machen die [**INTERFACESMediaBuffer-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) verfügbar. Diese Schnittstelle ist für das Lesen oder Schreiben beliebiger Datentypen konzipiert. Unkomprimierte Videoframes erfordern eine besondere Verarbeitung, da sie möglicherweise in Direct3D-Oberflächen im Videospeicher gespeichert werden.

In diesem Abschnitt werden die folgenden Themen behandelt:



| Thema                                                        | BESCHREIBUNG                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [Arbeiten mit Medienpuffern](working-with-media-buffers.md) | Beschreibt das allgemeine Verhalten von Medienpuffern für alle Medientypen. |
| [Nicht komprimierte Videopuffer](uncompressed-video-buffers.md) | Arbeiten mit Medienpuffern, die nicht komprimierte Videoframes enthalten  |
| [DirectX-Oberflächenpuffer](directx-surface-buffer.md)         | Beschreibt, wie eine Direct3D-Oberfläche in einem Medienpuffer gespeichert wird.         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Primitive](media-foundation-primitives.md)
</dt> </dl>

 

 



