---
description: 'MFPKEY_COMPLEXITYEX-Eigenschaft: Gibt die Komplexität des Encoderalgorithmus an.'
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: MFPKEY_COMPLEXITYEX-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e658e438909677f326372caa9e4da533e350b7133cc647b8f56562d09ad949e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873537"
---
# <a name="mfpkey_complexityex-property"></a>MFPKEY \_ COMPLEXITYEX-Eigenschaft

Gibt die Komplexität des Encoderalgorithmus an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCComplexityEx

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

Der Standardwert hängt von der Version des Videoencoders ab, wie in der folgenden Tabelle gezeigt.



| Encoderversion                 | Standardwert |
|---------------------------------|---------------|
| Windows Media Video 9-Encoder   | 3             |
| Windows Media Video 7/8-Encoder | 1             |



 

## <a name="possible-values"></a>Mögliche Werte

Die möglichen Werte hängen von der Version des Videoencoders ab, wie in der folgenden Tabelle gezeigt.



| Encoderversion                 | Mögliche Werte  |
|---------------------------------|------------------|
| Windows Media Video 9-Encoder   | 0, 1, 2, 3, 4, 5 |
| Windows Media Video 7/8-Encoder | 0, 1             |



 

## <a name="remarks"></a>Hinweise

Niedrigere Werte bewirken, dass der Codec weniger komplizierte Codierungsalgorithmen verwendet. Obwohl die einfacheren Algorithmen eine Ausgabe von niedrigerer Qualität erzeugen, ist der Codierungsprozess schneller und erfordert weniger Verarbeitungsleistung. Dies kann beim Codieren von Inhalten aus einer Livequelle wichtig sein, da der Encoder Eingaben schnell genug verarbeiten muss, um mit der Quelle Schritt zu halten.

Jeder dieser Eigenschaft zugewiesene Wert wird ignoriert, wenn die [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE-Eigenschaft](mfpkey-compressionoptimizationtypeproperty.md) auf 1 festgelegt ist. In diesem Fall wird MFPKEY \_ COMPLEXITYEX automatisch auf 3 festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




