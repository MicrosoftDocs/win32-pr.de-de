---
description: Auswählen eines Audiocodecs
ms.assetid: 37f3582c-c718-42ae-b887-d7d31ee853e9
title: Auswählen eines Audiocodecs (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b16dc0c6e65356f7d7e74b85b0671c2b41369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214340"
---
# <a name="choosing-an-audio-codec-microsoft-media-foundation"></a>Auswählen eines Audiocodecs (Microsoft Media Foundation)

Der [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md) bietet drei Kategorien von Audiocodierung, wie in der folgenden Tabelle gezeigt.



| Category                         | Zweck                                                    |
|----------------------------------|------------------------------------------------------------|
| Standard Windows Media Audio     | Allgemeine Komprimierung von Audiodaten.                      |
| Windows Media Audio Professional | Komprimieren von Multi-Channel-und High-Definition-Audiodaten.       |
| Verlust von Windows Media Audio Verlust     | Komprimieren von Audiodaten, ohne dass die ursprünglichen Daten verloren gehen. |



 

Die Kategorie Standard bietet allgemeine Audiocodierung, die für eine Vielzahl von Wiedergabe Szenarios geeignet ist. Beispielsweise kann die Audiogeschwindigkeit in eine niedrige Bitrate für das Streaming über ein Netzwerk mit eingeschränkter Bandbreite oder für das Rendern auf tragbaren Geräten komprimiert werden. Am anderen Ende der Skala können komprimierte Audioinhalte für die Wiedergabe mit hoher Qualität erzeugt werden. Der Schwerpunkt der Standard Codierungs Algorithmen liegt auf Musik, Sie sind jedoch auch für andere komplexe Audioinhalte geeignet. Die Standard Kategorie sollte der Standardwert für Audioinhalte sein. Die Kategorien "Professional" und "Lossless" sollten verwendet werden, um bestimmte Anforderungen zu erfüllen.

Ein separater Encoder, der [**Windows Media Voice Encoder**](windowsmediaaudiovoiceencoder.md), bietet eine Komprimierung der Sprache.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Audiodaten](workingwithaudio.md)
</dt> </dl>

 

 



