---
description: Gibt an, ob der Encoder eine bevorzugte Frame Größe in der Anzahl von Stichproben pro Frame verwenden soll.
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: MFPKEY_REQUESTING_A_FRAMESIZE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3355e84318ba4ad7995ac5ad0f002f4d70767b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370946"
---
# <a name="mfpkey_requesting_a_framesize-property"></a>Mfpkey- \_ Anforderung \_ einer \_ frameSize-Eigenschaft

Gibt an, ob der Encoder eine bevorzugte Frame Größe in der Anzahl von Stichproben pro Frame verwenden soll.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

**VT \_ bool**

## <a name="remarks"></a>Bemerkungen

Um eine bevorzugte Frame Größe festzulegen, legen Sie die folgenden Eigenschaften fest.

-   Legen Sie **mfpkey fest, um \_ \_ einen \_ frameSize** -Wert auf Variant \_ true anzufordern.
-   Legen Sie die [**\_ gewünschte \_ frameSize von mfpkey**](mfpkey-preferred-framesizeproperty.md) auf die gewünschte Anzahl von Stichproben in jedem Frame fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista oder Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
