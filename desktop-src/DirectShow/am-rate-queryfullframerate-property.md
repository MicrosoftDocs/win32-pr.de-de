---
description: Diese Eigenschaft fragt den Decoder nach der maximalen Vollbildrate ab, die der Decoder unterstützt. Der Datentyp für diese Eigenschaft ist eine AM \_ QueryRate-Struktur.
ms.assetid: 98808ed4-6d34-437b-9729-9cc805bc81f0
title: AM_RATE_QueryFullFrameRate-Eigenschaft (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70bc096e5b68737ca877a037571223d673284dab
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910278"
---
# <a name="am_rate_queryfullframerate-property"></a>AM \_ RATE \_ QueryFullFrameRate-Eigenschaft

Diese Eigenschaft fragt den Decoder nach der maximalen Vollbildrate ab, die der Decoder unterstützt. Der Datentyp für diese Eigenschaft ist eine **AM \_ QueryRate-Struktur.**

Diese Eigenschaft ist für Version 1.1 dieses Eigenschaftensatzes definiert. siehe [**AM \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md).



| Bezeichnung | Wert |
|-------------------|---------------------------------------|
| Eigenschaftensatz-GUID | AM \_ KSPROPSETID \_ TSRateChange         |
| Eigenschafts-ID       | AM \_ RATE \_ QueryFullFrameRate-Eigenschaft |
| Datentyp         | [**AM \_ QueryRate**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_queryrate) |



 

## <a name="remarks"></a>Bemerkungen

Wenn die Wiedergaberate die maximale Rate des Decoders überschreitet, sendet der Quellfilter Gruppen kontinuierlicher Stichproben, die durch Diskontinuitäten getrennt sind. Die Zeitstempel springen über die Diskontinuitäten. Der Quellfilter kann dies auch dann tun, wenn die Wiedergaberate innerhalb der maximalen Rate des Decoders liegt, da es möglicherweise andere Faktoren gibt, z. B. Datenträger-E/A, die die vollständige Wiedergaberate einschränken.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ratenänderungseigenschaftensatz**](rate-change-property-set.md)
</dt> </dl>

 

 




