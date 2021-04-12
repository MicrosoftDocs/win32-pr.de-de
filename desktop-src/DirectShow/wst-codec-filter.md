---
description: WST-Codec-Filter
ms.assetid: 0a06acbf-b842-4ab6-bcf9-d2d006301d83
title: WST-Codec-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338db987986a5f4706c144907d122eec3a0615a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349798"
---
# <a name="wst-codec-filter"></a>WST-Codec-Filter

> [!IMPORTANT]
> Diese Komponente wurde aus Windows Vista und höheren Betriebssystemen entfernt. Es ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.

 

Ab Windows Vista wird dieser Filter durch den vbicodec-Filter ersetzt, der in der Dokumentation zu Microsoft TV-Technologien dokumentiert ist.

Der Weltstandard-Teletext (WST) ist der Europäische Standard für die Datenübertragung mithilfe von VBI auf PAL-Analog Fernsehsignale. Untertitel und Datendienste werden mithilfe dieses Standards bereitgestellt. Der WST-Codec ist ein kernelmodusfilter, der unformatierte VBI-Beispiele und optional decodierte teletextbeispiele aus dem Erfassungs Filter über den [Tee/Sink-to-Sink-konverterfilter](tee-sink-to-sink-converter.md) empfängt. Dieser Codec decodiert und/oder dupliziert die von decodierten und vorwärts Fehler korrigierten Teletextdaten für den [WST-Decoderfilter](wst-decoder-filter.md) . Der WST-Codec entspricht dem CC-Decoderfilter für NTSC-Übertragungen. Der WST-Decoder entspricht dem " [Line 21](line-21-decoder-filter.md) "-Decoder für NTSC; Diese Filter erstellen die Bitmaps, die an den Overlay-Mixer oder den Video Mischungs-Renderer gesendet werden.

Dieser Filter verfügt über zwei Eingabe Pins: VBI und HWCC. Die VBI-PIN wird für unformatierte VBI-Daten verwendet, und die HWCC-PIN wird verwendet, wenn die VBI-Decodierung mithilfe des Erfassungs Filters auf der Hardware ausgeführt wird. Wenn die Daten in der HWCC-Pin empfangen werden, arbeitet der WST-Codec im Pass-Through-Modus und sendet die Daten direkt an den WST-Decoder, ohne ihn in irgendeiner Weise zu verarbeiten. Wenn der Erfassungs Filter eine HWCC-Pin verfügbar macht, muss Sie direkt mit der entsprechenden PIN auf dem WST-Codec verbunden werden.

Der WST-Codec-Filter wird in der Filterkategorie "WDM Streaming VBI Codecs" (**am \_ kscategory \_ vbicodec**) angezeigt.

Da es sich hierbei um einen Kernel Modus-Filter handelt, können Anwendungen ihn nicht direkt mithilfe von **cokreateinstance** erstellen. Verwenden Sie stattdessen den [Enumerator "System Geräte](system-device-enumerator.md)". Weitere Informationen finden Sie unter [Erstellen von Kernel-Mode filtern](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Anzeigen von World Standard-Teletext](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



