---
title: Averagelevel
description: Das averagelevel-Attribut enthält einen 16-Bit-Amplitude-Wert, der die durchschnittliche Volumeebene von Audioinhalten festlegt.
ms.assetid: e6270ac8-5de3-4dee-824c-ba25fdd272c8
keywords:
- Averagelevel-Windows Media-Format
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 632379e42fa6c64e44018173b9d40340add4ee61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037963"
---
# <a name="averagelevel"></a>Averagelevel

Das **averagelevel** -Attribut enthält einen 16-Bit-Amplitude-Wert, der die durchschnittliche Volumeebene von Audioinhalten festlegt. Mit " [**Peer Value**](peakvalue.md)" wird dieses Attribut für die Normalisierung verwendet. Normalisierung ist der Prozess, bei dem die Wiedergabe Volume-Ebene von Audiodateien angepasst wird, sodass die laugsten Teile der Dateien wiedergegeben werden, die auf derselben Ebene wiedergegeben werden, und das durchschnittliche Volume.

## <a name="global-constant"></a>Globale Konstante

g \_ wszaveragelevel

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ DWORD**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird durch das Writer-Objekt auf der Grundlage von Informationen aus dem Codec festgelegt. Nur mit einem der Windows Media Audio Codecs komprimierte Streams haben einen automatisch festgelegten Wert.

**Averagelevel** ist nicht schreibgeschützt. Wenn die Datei jedoch vom Windows-Media Player abgespielt wird, sollten Sie diesen Wert nicht ändern. Der Windows-Media Player verwendet diese, um die Ebenen von Dateien in einer Wiedergabeliste zu normalisieren.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




