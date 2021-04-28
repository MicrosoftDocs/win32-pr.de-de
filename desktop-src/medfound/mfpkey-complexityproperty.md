---
description: 'MFPKEY_COMPLEXITY-Eigenschaft: Gibt die Komplexität des Encoderalgorithmus an.'
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: MFPKEY_COMPLEXITY-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042e3158b43efb5a4a82542f000d137fa0c195e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092938"
---
# <a name="mfpkey_complexity-property"></a>MFPKEY \_ COMPLEXITY-Eigenschaft

\[[**MFPKEY \_ COMPLEXITY**](mfpkey-complexityexproperty.md) ist für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen **MFPKEY \_ COMPLEXITYEX**.\]

Gibt die Komplexität des Encoderalgorithmus an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCComplexityMode

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

Der Standardwert hängt von der Version des Videoencoder ab, wie in der folgenden Tabelle gezeigt.



| Encoderversion                 | Standardwert |
|---------------------------------|---------------|
| Windows Media Video 9-Encoder   | 3             |
| Windows Media Video 7/8-Encoder | 1             |



 

## <a name="remarks"></a>Bemerkungen

Dieser ganzzahlige Wert liegt zwischen 0 und 3. Niedrigere Werte führen dazu, dass der Codec weniger komplizierte Codierungsalgorithmen verwendet. Obwohl die einfacheren Algorithmen eine Ausgabe mit geringerer Qualität erzeugen, ist der Codierungsprozess schneller und erfordert weniger Verarbeitungsleistung.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




