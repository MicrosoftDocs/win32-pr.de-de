---
description: Gibt an, ob der Codec versuchen soll, laute Rahmenränder zu erkennen und zu entfernen.
ms.assetid: fdb4f3a8-1447-4e1e-a208-0f9b717f7626
title: MFPKEY_NOISEEDGEREMOVAL-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 128ab89cd12c31186cf99e0c01454986bfe950a3d0a68b6196db6df205dea02a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242557"
---
# <a name="mfpkey_noiseedgeremoval-property"></a>MFPKEY \_ NOISEEDGEREMOVAL-Eigenschaft

Gibt an, ob der Codec versuchen soll, laute Rahmenränder zu erkennen und zu entfernen.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCNoiseEdgeRemoval

## <a name="data-type"></a>Datentyp

VT \_ BOOL

## <a name="default-value"></a>Standardwert

FALSE

## <a name="remarks"></a>Hinweise

Bei einem lauten Rahmenrand handelt es sich in der Regel um die Daten des vertikalen Leerungsintervalls (Vertical Blanking Interval, VBI) aus einem Frame von Fernsehsendungen. Die VBI ist die ersten 21 Scanzeilen des Fernsehrahmens. Diese Scanzeilen enthalten keine Videodaten– sie enthalten Daten über die Übertragung. Wenn ein Fernsehsignal von einer Erfassungskarte aufgezeichnet wird, wird die VBI in der Regel aus dem Frame entfernt. Die laute Edgeerkennung und -korrektur, die vom Codec durchgeführt wird, kann nur einen Rand korrigieren, der über drei oder weniger Rauschlinien verfügt. Wenn das erfasste Video mehr als drei laute Zeilen enthält, liegt ein Problem mit der Hardware vor, die zum Erfassen des Videos verwendet wird.

Wenn der Codec so festgelegt ist, dass verrauschte Kanten entfernt werden, dupliziert er Zeilen, die an den lauten Rand angrenzen, um den Rahmen auszufüllen.

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

 

 




