---
description: Gibt an, ob der Kern Encoder den &\# 0034; Plus&\# 0034; Feature.
ms.assetid: 1ace09da-7dee-469e-a533-63b40ac747ab
title: MFPKEY_ENHANCED_WMA-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df1c7ddc0e7bfb6d62d51e535f10b257eac6f2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369290"
---
# <a name="mfpkey_enhanced_wma-property"></a>Mfpkey \_ Enhanced \_ WMA-Eigenschaft

Gibt an, ob der Kern Encoder die Funktion "Plus" verwendet.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

**VT \_ UI4**

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist nur für Windows Media Audio Verlust lose verfügbar.

Wenn Sie für diese Eigenschaft den Standardwert 0 (null) belassen, oder wenn Sie den Wert auf 1 festlegen, entscheidet der Kern Encoder, ob der "Plus"-Teil verwendet werden soll. Wenn Sie diese Eigenschaft auf 2 festlegen, wird das Feature "Plus" vom Kern Encoder nicht verwendet.

Diese Eigenschaft ändert die aufgelisteten Medientypen. Wenn Sie Sie also festlegen, müssen Sie dies tun, bevor Sie den Ausgabetyp festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista oder Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
