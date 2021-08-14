---
description: Gibt an, ob der Kernencoder die &\# 0034; verwendet. Plus&\# 0034;-Feature.
ms.assetid: 1ace09da-7dee-469e-a533-63b40ac747ab
title: MFPKEY_ENHANCED_WMA-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab3fdcd3087773ea760615224b148bd497c1f89114c0f761a7d2f90fb0b5a8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738017"
---
# <a name="mfpkey_enhanced_wma-property"></a>MFPKEY \_ ENHANCED \_ WMA-Eigenschaft

Gibt an, ob der Kernencoder das Plusfeature verwendet.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mithilfe von [**IPropertyStore verfügbar.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Datentyp

**VT \_ UI4**

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist nur für Medienmedien Windows Verlustlos verfügbar.

Wenn Sie diese Eigenschaft beim Standardwert 0 be lassen oder auf 1 festlegen, entscheidet der Kernencoder, ob der "Plus"-Teil verwendet werden soll. Wenn Sie diese Eigenschaft auf 2 festlegen, verwendet der Kernencoder nicht das Feature "Plus".

Diese Eigenschaft ändert die aufzählten Medientypen. Wenn Sie sie also festlegen, müssen Sie dies tun, bevor Sie den Ausgabetyp festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista oder Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
