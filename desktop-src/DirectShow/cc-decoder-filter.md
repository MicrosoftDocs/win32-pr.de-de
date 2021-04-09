---
description: CC-Decoderfilter
ms.assetid: 57ef75f6-411c-4b1f-b0dc-ac293ebc0b9c
title: CC-Decoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93995207e4f1a397db28f743d1f972b871b0553
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957788"
---
# <a name="cc-decoder-filter"></a>CC-Decoderfilter

> [!IMPORTANT]
> Diese Komponente wurde aus Windows Vista und höheren Betriebssystemen entfernt. Es ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.

 

Der CC VBI-Decoder ist ein streamklassenfilter im Kernel Modus. Es wird in GraphEdit unter der Kategorie "WDM Streaming VBI Codecs" angezeigt. Er akzeptiert Beispiel Wellen Formulare, die von einem Erfassungs Filter bereitgestellt werden, und übermittelt decodierte, geschlossene Daten an den [Line 21-Decoder](line-21-decoder-filter.md) und/oder an interessierte Anwendungen.

Dieser Filter verfügt über zwei Eingabe Pins: VBI und HWCC. Die VBI-PIN wird für unformatierte VBI-Daten verwendet, und die HWCC-PIN wird verwendet, wenn die VBI-Decodierung mithilfe des Erfassungs Filters auf der Hardware ausgeführt wird. Wenn die Daten in der HWCC-Pin empfangen werden, wird der CC-Decoder im Pass-Through-Modus ausgeführt und sendet die Daten direkt an den "Line 21"-Decoder, ohne Sie zu verarbeiten. Wenn der Erfassungs Filter eine HWCC-Pin verfügbar macht, muss Sie direkt mit der entsprechenden PIN im CC-Decoder verbunden werden. Die PIN-Kategorie lautet **Pinname \_ Video \_ CC \_ Capture**.

Der CC-Decoder verfügt über bis zu acht Ausgabe Pins, von denen jeder ihre eigenen Zeilen und unter Ströme auswählen kann. Der erste Ausgabepin ist mit dem Line-21-Decoder verbunden.

Der CC-Decoderfilter wird in der Filterkategorie "WDM Streaming VBI Codecs" (**am \_ kscategory \_ vbicodec**) angezeigt.

Da es sich hierbei um einen Kernel Modus-Filter handelt, können Anwendungen ihn nicht direkt mithilfe von **cokreateinstance** erstellen. Verwenden Sie stattdessen den [Enumerator "System Geräte](system-device-enumerator.md)". Weitere Informationen finden Sie unter [Erstellen von Kernel-Mode filtern](creating-kernel-mode-filters.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Anzeigen von Untertiteln](viewing-closed-captions.md)
</dt> </dl>

 

 



