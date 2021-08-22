---
title: AverageLevel
description: Das AverageLevel-Attribut enthält einen 16-Bit-Amplitudenwert, der die durchschnittliche Lautstärke des Audioinhalts bezeichnet.
ms.assetid: e6270ac8-5de3-4dee-824c-ba25fdd272c8
keywords:
- AverageLevel-Windows-Medienformat
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd8745c5983eca67a02506b6cdeeabaca0a61a4c3f8b2a6993a73359d87adba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028158"
---
# <a name="averagelevel"></a>AverageLevel

Das **AverageLevel-Attribut** enthält einen 16-Bit-Amplitudenwert, der die durchschnittliche Lautstärke des Audioinhalts bezeichnet. Mit [**PeakValue**](peakvalue.md)wird dieses Attribut für die Normalisierung verwendet. Bei der Normalisierung wird die Wiedergabevolumenebene von Audiodateien so angepasst, dass die lautesten Teile der Dateien auf der gleichen Ebene und die durchschnittliche Lautstärke für jede Datei identisch sind.

## <a name="global-constant"></a>Globale Konstante

g \_ wszAverageLevel

## <a name="data-type"></a>Datentyp

**WMT \_ TYPE \_ DWORD**

## <a name="remarks"></a>Hinweise

Dieses Attribut wird vom Writer-Objekt basierend auf Informationen aus dem Codec festgelegt. Nur Streams, die mit einem der Windows Medienaudiocodecs komprimiert sind, verfügen über einen automatisch festgelegten Wert.

**AverageLevel** ist nicht schreibgeschützt. Wenn die Datei jedoch vom -Windows Media Player abgespielt wird, sollten Sie diesen Wert nicht ändern. Die Windows Media Player verwendet diese zum Normalisieren der Ebenen von Dateien in einer Wiedergabeliste.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




