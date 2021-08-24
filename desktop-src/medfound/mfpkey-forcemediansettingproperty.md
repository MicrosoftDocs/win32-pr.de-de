---
description: Gibt an, ob der Codec median filtering während der Codierung verwenden soll.
ms.assetid: adfca033-4679-4f36-a802-6dd5df7100c8
title: MFPKEY_FORCEMEDIANSETTING-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 722fca2f73f2114cf17664f228e00a12f46e5a399f54b8dc6990940f5c18d979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953950"
---
# <a name="mfpkey_forcemediansetting-property"></a>MFPKEY \_ FORCEMEDIANSETTING-Eigenschaft

Gibt an, ob der Codec median filtering während der Codierung verwenden soll.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCForceMedianSetting

## <a name="data-type"></a>Datentyp

VT \_ BOOL

## <a name="default-value"></a>Standardwert

FALSE

## <a name="remarks"></a>Hinweise

Die Medianfilterung weist den Codec an, beim Berechnen der Bewegung zwischen Frames Rauschen und Grain zu ignorieren. Dies kann die Qualität von sehr lauten Videos verbessern, kann aber zu Bewegungspfaden (auch als nachfolgende Artefakte bezeichnet) führen, wenn sie auf bereinigte Quellvideos angewendet werden.

Standardmäßig verwendet der Codec interne Logik, um zu bestimmen, ob die Medianfilterung verwendet werden soll. Wenn Sie diese Eigenschaft festlegen, wird diese Logik überschrieben.

> [!Note]  
> Dieser Filter ist nicht identisch mit medianen Weichzeichnerfiltern, die in vielen Anwendungen zur Videobearbeitung und Nachbearbeitung gefunden werden.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




