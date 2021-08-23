---
title: OptimalBitrate
description: Das OptimalBitrate-Attribut enthält die Bitrate, mit der die Datei am besten abgespielt werden kann.
ms.assetid: cd13b9b5-34d2-4ebb-9f10-3bf42dd9de81
keywords:
- OptimalBitrate-Windows-Medienformat
topic_type:
- apiref
api_name:
- OptimalBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f670c2acd2f2190a5ee2bfd76994c219c6f967dbbd933520a8d4627236a0d36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930630"
---
# <a name="optimalbitrate"></a>OptimalBitrate

Das **OptimalBitrate-Attribut** enthält die Bitrate, mit der die Datei am besten abgespielt werden kann.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMOptimalBitrate

## <a name="data-type"></a>Datentyp

**WMT \_ TYPE \_ DWORD**

## <a name="remarks"></a>Hinweise

Dies ist ein codiertes Attribut.

Bei Dateien, die VBR-Datenströme (Variable Bit Rate) enthalten, ist dieser Wert die Spitzenbitrate für die Streams in der Datei. Bei Dateien ohne VBR ist dieser Wert mit [**bitrate identisch.**](bit-rate.md)

Dieses Attribut kann nicht auf Dateiebene dupliziert werden. Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und vermittelt den Objekten des Windows Media Format SDK nicht seine normale Bedeutung.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




