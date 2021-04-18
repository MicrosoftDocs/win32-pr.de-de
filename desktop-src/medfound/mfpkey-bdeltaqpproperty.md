---
description: Gibt die Delta Vergrößerung zwischen dem Bild quantifizer des Anker Rahmens und dem Bild quantifizer des B-Frames an.
ms.assetid: 8ab9401b-6fed-4178-955f-2e0bf950bf60
title: MFPKEY_BDELTAQP-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba1ca7d30e17841badeda0312f77471116a8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358423"
---
# <a name="mfpkey_bdeltaqp-property"></a>Mfpkey \_ bdelta taqp (Eigenschaft)

Gibt die Delta Vergrößerung zwischen dem Bild quantifizer des Anker Rahmens und dem Bild quantifizer des B-Frames an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcbdelta taqp

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Bemerkungen

Der Bild quantifiziererer (QP) ist ein Maß für die Komprimierung eines Frames. Höhere Werte stellen höhere Komprimierungs Verhältnisse dar. Der QP kann in Schritten von halb Punkten festgelegt werden. Ein B-Frame wird in der Regel mit einem QP identisch mit dem Wert oder 0,5, der höher ist als der QP des Anker Rahmens. Durch die Angabe eines b-Frame-QP-Deltas oberhalb von 0 ist es möglich, B-Frames mit einem noch höheren Komprimierungs Verhältnis zu komprimieren.

Der B-Frame-Delta-QP kann nur in ganz punktinkrementen festgelegt werden. Diese Eigenschaft muss auf einen ganzzahligen Wert zwischen 0 und 31 festgelegt werden. Der empfohlene Wert ist 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




