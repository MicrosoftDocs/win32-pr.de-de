---
description: Gibt die bevorzugte Anzahl von Stichproben pro Frame an.
ms.assetid: ad629dbd-49d8-43d0-95a8-03f2043e397e
title: MFPKEY_PREFERRED_FRAMESIZE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe04ad37c6cd684e3179cbd16328346fd6f11dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362136"
---
# <a name="mfpkey_preferred_framesize-property"></a>Von mfpkey \_ bevorzugte \_ frameSize-Eigenschaft

Gibt die bevorzugte Anzahl von Stichproben pro Frame an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

**VT \_ UI4**

## <a name="remarks"></a>Bemerkungen

Um eine bevorzugte Frame Größe festzulegen, legen Sie die folgenden Eigenschaften fest.

-   Legen Sie [**mfpkey fest, um \_ \_ einen \_ frameSize**](mfpkey-requesting-a-framesizeproperty.md) -Wert auf **Variant \_ true** anzufordern.
-   Legen Sie die **\_ gewünschte \_ frameSize von mfpkey** auf die gewünschte Anzahl von Stichproben in jedem Frame fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista oder Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
