---
title: PeakValue
description: Das PeakValue-Attribut enthält einen 16-Bit-Amplitudenwert, der die Spitzenlautstärke von Audioinhalten ansteuert.
ms.assetid: 885f6d4c-661a-4681-96b6-c1a282c8bf18
keywords:
- PeakValue windows Media Format
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3089ac6d4b789d740f256a5c44c1911eb3501bc654c3b94d0006d405616572
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110260"
---
# <a name="peakvalue"></a>PeakValue

Das **PeakValue-Attribut** enthält einen 16-Bit-Amplitudenwert, der die Spitzenlautstärke von Audioinhalten ansteuert. Mit [**AverageLevel**](averagelevel.md)wird dieses Attribut für die Normalisierung verwendet. Normalisierung ist der Prozess der Anpassung der Wiedergabelautstärke von Audiodateien, sodass die lautesten Teile der Dateien, die auf der gleichen Ebene wiedergegeben werden, und die durchschnittliche Lautstärke für jede identisch sind.

## <a name="global-constant"></a>Globale Konstante

g \_ wszPeakValue

## <a name="data-type"></a>Datentyp

**\_WMT-TYP \_ DWORD**

## <a name="remarks"></a>Hinweise

Dieses Attribut wird vom Writer-Objekt basierend auf Denkinformationen des Codecs festgelegt. Nur Streams, die mit einem der Windows Media Audio-Codecs komprimiert sind, verfügen über einen automatisch festgelegten Wert.

**PeakValue** ist nicht schreibgeschützt. Wenn die Datei jedoch vom Windows Media Player wiedergegeben wird, sollten Sie diesen Wert nicht ändern. Die Windows Media Player verwendet diese zum Normalisieren der Ebenen von Dateien in einer Wiedergabeliste.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




