---
description: Gibt an, ob der Codec die Median Filterung während der Codierung verwenden soll.
ms.assetid: adfca033-4679-4f36-a802-6dd5df7100c8
title: MFPKEY_FORCEMEDIANSETTING-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38d0aa154798e2ed42a7373a6e85a4b46f8eeb7b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869555"
---
# <a name="mfpkey_forcemediansetting-property"></a>Mfpkey \_ forcemediansetting (Eigenschaft)

Gibt an, ob der Codec die Median Filterung während der Codierung verwenden soll.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcforcemediansetting

## <a name="data-type"></a>Datentyp

VT \_ bool

## <a name="default-value"></a>Standardwert

false

## <a name="remarks"></a>Bemerkungen

Die Median Filterung weist den Codec an, Rauschen und Körner beim Berechnen der Bewegung zwischen Frames zu ignorieren. Dies kann die Qualität des Videos mit sehr lauter Qualität verbessern, kann jedoch zu Bewegungs Pfaden (auch als nachfolgende Artefakte bezeichnet) führen, wenn diese auf das saubere Quellvideo angewendet werden.

Standardmäßig verwendet der Codec interne Logik, um zu bestimmen, ob die Median Filterung verwendet werden soll. Wenn Sie diese Eigenschaft festlegen, wird diese Logik überschrieben.

> [!Note]  
> Dieser Filter ist nicht mit den in vielen Video Bearbeitungs-und nachträglich verarbeiteten Anwendungen gefundenen Median weich Filtern identisch.

 

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

 

 




