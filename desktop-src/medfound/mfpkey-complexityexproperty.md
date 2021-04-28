---
description: 'MFPKEY_COMPLEXITYEX-Eigenschaft: Gibt die Komplexität des Encoderalgorithmus an.'
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: MFPKEY_COMPLEXITYEX-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20579bcf7a06dc11f47cbef6a53629f3a36b48dc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087608"
---
# <a name="mfpkey_complexityex-property"></a>MFPKEY \_ COMPLEXITYEX-Eigenschaft

Gibt die Komplexität des Encoderalgorithmus an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCComplexityEx

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

Der Standardwert hängt von der Version des Videoencoder ab, wie in der folgenden Tabelle gezeigt.



| Encoderversion                 | Standardwert |
|---------------------------------|---------------|
| Windows Media Video 9-Encoder   | 3             |
| Windows Media Video 7/8-Encoder | 1             |



 

## <a name="possible-values"></a>Mögliche Werte

Die möglichen Werte hängen von der Version des Videoencoder ab, wie in der folgenden Tabelle gezeigt.



| Encoderversion                 | Mögliche Werte  |
|---------------------------------|------------------|
| Windows Media Video 9-Encoder   | 0, 1, 2, 3, 4, 5 |
| Windows Media Video 7/8-Encoder | 0, 1             |



 

## <a name="remarks"></a>Bemerkungen

Niedrigere Werte führen dazu, dass der Codec weniger komplizierte Codierungsalgorithmen verwendet. Obwohl die einfacheren Algorithmen eine Ausgabe mit geringerer Qualität erzeugen, ist der Codierungsprozess schneller und erfordert weniger Verarbeitungsleistung. Dies kann wichtig sein, wenn Inhalte aus einer Livequelle codiert werden, da der Encoder Eingaben schnell genug verarbeiten muss, um mit der Quelle Schritt zu halten.

Jeder dieser Eigenschaft zugewiesene Wert wird ignoriert, wenn die [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE-Eigenschaft](mfpkey-compressionoptimizationtypeproperty.md) auf 1 festgelegt ist. In diesem Fall wird MFPKEY \_ COMPLEXITYEX automatisch auf 3 festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




