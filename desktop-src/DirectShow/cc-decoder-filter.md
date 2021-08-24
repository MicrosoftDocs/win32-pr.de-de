---
description: CC-Decoderfilter
ms.assetid: 57ef75f6-411c-4b1f-b0dc-ac293ebc0b9c
title: CC-Decoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5feab764883754407030f2b4f72f794d049f5a394efb107ac149b10125da8d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757400"
---
# <a name="cc-decoder-filter"></a>CC-Decoderfilter

> [!IMPORTANT]
> Diese Komponente wurde aus den Betriebssystemen Windows Vista und höher entfernt. Es ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.

 

Der CC-VBI-Decoder ist ein Streamklassenfilter im Kernelmodus. Sie wird in GraphEdit unter der Kategorie "WDM Streaming VBI Codecs" angezeigt. Sie akzeptiert Wellenformbeispiele, die von einem Erfassungsfilter bereitgestellt werden, und übermittelt decodierte Untertiteldaten an den [Line 21-Decoder und/oder](line-21-decoder-filter.md) an die interessierten Anwendungen.

Dieser Filter verfügt über zwei Eingabepins: VBI und HWCC. Der VBI-Pin wird für unformatierte VBI-Daten verwendet, und der HWCC-Pin wird verwendet, wenn die VBI-Decodierung auf Hardware durch den Erfassungsfilter ausgeführt wird. Wenn die Daten auf dem HWCC-Pin empfangen werden, arbeitet der CC-Decoder im Pass-Through-Modus und sendet die Daten direkt an den Line 21-Decoder, ohne sie in irgendeiner Weise zu verarbeiten. Wenn der Erfassungsfilter einen HWCC-Pin verfügbar macht, muss er direkt mit dem entsprechenden Pin im CC-Decoder verbunden werden. Die Pinkategorie ist **PINNAME \_ VIDEO CC \_ \_ CAPTURE.**

Der CC-Decoder verfügt über bis zu acht Ausgabepins, von denen jeder seine eigenen Zeilen und Unterstreams auswählen kann. Der erste Ausgabepin ist mit dem Line-21-Decoder verbunden.

Der Filter CC-Decoder wird in der Filterkategorie "WDM Streaming VBI Codecs"**(AM \_ KSCATEGORY \_ VBICODEC) angezeigt.**

Da es sich um einen Kernelmodusfilter handelt, können Anwendungen ihn nicht direkt mit **CoCreateInstance erstellen.** Verwenden Sie stattdessen den [Systemgeräte-Enumerator](system-device-enumerator.md). Weitere Informationen finden Sie unter [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Anzeigen von Untertiteln](viewing-closed-captions.md)
</dt> </dl>

 

 



