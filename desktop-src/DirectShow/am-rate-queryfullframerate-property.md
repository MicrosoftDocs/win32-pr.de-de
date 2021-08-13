---
description: Diese Eigenschaft fragt den Decoder nach der maximalen Vollbildrate ab, die der Decoder unterstützt. Der Datentyp für diese Eigenschaft ist eine AM \_ QueryRate-Struktur.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: AM_RATE_QueryFullFrameRate-Eigenschaft (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899ceb938ac3fd0ea5f7f58b340f4b57fd6a722650cd3225702cbb74b1644045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664108"
---
# <a name="am_rate_queryfullframerate-property"></a>AM \_ RATE \_ QueryFullFrameRate-Eigenschaft

Diese Eigenschaft fragt den Decoder nach der maximalen Vollbildrate ab, die der Decoder unterstützt. Der Datentyp für diese Eigenschaft ist eine **AM \_ QueryRate-Struktur.**

Diese Eigenschaft wird für Version 1.1 dieses Eigenschaftensets definiert. siehe [**AM \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md).



| Bezeichnung | Wert |
|-------------------|---------------------------------------|
| Eigenschaftensatz-GUID | AM \_ KSPROPSETID \_ TSRateChange         |
| Eigenschafts-ID       | AM \_ RATE \_ QueryFullFrameRate-Eigenschaft |
| Datentyp         | [**AM \_ QueryRate**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a>Hinweise

Wenn die Wiedergaberate die maximale Rate des Decoders überschreitet, sendet der Quellfilter Gruppen kontinuierlicher Stichproben getrennt durch Diskontinuitäten. Die Zeitstempel springen über die Diskontinuitäten. Der Quellfilter kann dies auch dann tun, wenn die Wiedergaberate innerhalb der maximalen Rate des Decoders liegt, da es möglicherweise andere Faktoren wie Datenträger-E/A gibt, die die vollständige Wiedergaberate einschränken.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Rate Change Property Set**](rate-change-property-set.md)
</dt> </dl>

 

 




