---
description: Gibt die Komplexität des Codierungs Algorithmus an.
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: MFPKEY_COMPLEXITYEX-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b935f41ce14a77a135d0bbc8ad6dec2933b570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215528"
---
# <a name="mfpkey_complexityex-property"></a>\_Complexityex-Eigenschaft für mfpkey

Gibt die Komplexität des Codierungs Algorithmus an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvccomplexityex

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

Der Standardwert hängt von der Version des Video Encoders ab, wie in der folgenden Tabelle dargestellt.



| Codierungs Version                 | Standardwert |
|---------------------------------|---------------|
| Windows Media Video 9-Encoder   | 3             |
| Windows Media Video 7/8-Encoder | 1             |



 

## <a name="possible-values"></a>Mögliche Werte

Die möglichen Werte hängen von der Version des Video Encoders ab, wie in der folgenden Tabelle gezeigt.



| Codierungs Version                 | Mögliche Werte  |
|---------------------------------|------------------|
| Windows Media Video 9-Encoder   | 0, 1, 2, 3, 4, 5 |
| Windows Media Video 7/8-Encoder | 0, 1             |



 

## <a name="remarks"></a>Bemerkungen

Niedrigere Werte bewirken, dass der Codec weniger komplizierte Codierungs Algorithmen verwendet. Obwohl die einfacheren Algorithmen eine Ausgabe mit geringerer Qualität verursachen, ist der Codierungsprozess schneller und erfordert weniger Verarbeitungsleistung. Dies kann beim Codieren von Inhalten aus einer Live Quelle von Bedeutung sein, da der Encoder Eingaben schnell genug verarbeiten muss, um mit der Quelle zu bleiben.

Jeder Wert, der dieser Eigenschaft zugewiesen ist, wird ignoriert, wenn die Eigenschaft [ \_ compressionoptimizationtype von mfpkey](mfpkey-compressionoptimizationtypeproperty.md) auf 1 festgelegt ist. In diesem Fall wird mfpkey \_ complexityex automatisch auf 3 festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




