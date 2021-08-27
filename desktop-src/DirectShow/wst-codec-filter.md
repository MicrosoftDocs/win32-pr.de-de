---
description: WST-Codecfilter
ms.assetid: 0a06acbf-b842-4ab6-bcf9-d2d006301d83
title: WST-Codecfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e729e13500317711076f6cdbd39c9a6ab25bea77e8d378e12f917f2e20e4a561
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083450"
---
# <a name="wst-codec-filter"></a>WST-Codecfilter

> [!IMPORTANT]
> Diese Komponente wurde aus den Betriebssystemen Windows Vista und höher entfernt. Es ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.

 

Ab Windows Vista wird dieser Filter durch den VBICodec-Filter ersetzt, der in der Dokumentation zu Microsoft TV Technologies dokumentiert ist.

World Standard Teletext (WST) ist der europäische Standard für die Datenübertragung mit VBI auf analogen PAL-Fernsehsignalen. Sowohl Beschriftungs- als auch Datendienste werden mit diesem Standard bereitgestellt. Der WST-Codec ist ein Kernelmodusfilter, der unformatierte VBI-Beispiele und optional decodierte Teletext-Beispiele aus dem Erfassungsfilter über den [Filter Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md) empfängt. Dieser Codec decodiert und/oder dupliziert die decodierten und forward-error-korrigierten Teletext-Daten für den [WST-Decoderfilter.](wst-decoder-filter.md) Der WST-Codec entspricht dem CC-Decoderfilter für NTSC-Übertragungen. Der WST-Decoder entspricht dem [Line 21-Decoder](line-21-decoder-filter.md) für NTSC. Diese Filter erstellen die Bitmaps, die an die Overlay-Mixer oder den Renderer für das Mischen von Videos gesendet werden.

Dieser Filter verfügt über zwei Eingabepins: VBI und HWCC. Der VBI-Pin wird für unformatierte VBI-Daten verwendet, und der HWCC-Pin wird verwendet, wenn die VBI-Decodierung auf Hardware durch den Erfassungsfilter ausgeführt wird. Wenn die Daten auf dem HWCC-Pin empfangen werden, arbeitet der WST-Codec im Pass-Through-Modus und sendet die Daten direkt an den WST-Decoder, ohne sie in irgendeiner Weise zu verarbeiten. Wenn der Erfassungsfilter einen HWCC-Pin verfügbar macht, muss er direkt mit dem entsprechenden Pin im WST-Codec verbunden werden.

Der WST-Codecfilter wird in der Filterkategorie "WDM Streaming VBI Codecs"**(AM \_ KSCATEGORY \_ VBICODEC) angezeigt.**

Da es sich um einen Kernelmodusfilter handelt, können Anwendungen ihn nicht direkt mit **CoCreateInstance erstellen.** Verwenden Sie stattdessen den [Systemgeräte-Enumerator](system-device-enumerator.md). Weitere Informationen finden Sie unter [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Viewing World Standard Teletext](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



