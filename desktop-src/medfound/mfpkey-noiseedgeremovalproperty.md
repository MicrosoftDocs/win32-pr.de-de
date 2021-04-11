---
description: Gibt an, ob der Codec versuchen soll, laute Rahmen Ränder zu erkennen und zu entfernen.
ms.assetid: fdb4f3a8-1447-4e1e-a208-0f9b717f7626
title: MFPKEY_NOISEEDGEREMOVAL-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30acd92bae7693d0714e42d6b4f832a521557bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215508"
---
# <a name="mfpkey_noiseedgeremoval-property"></a>Mfpkey \_ noiseedgeremuval-Eigenschaft

Gibt an, ob der Codec versuchen soll, laute Rahmen Ränder zu erkennen und zu entfernen.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcnoiseedgeremuval

## <a name="data-type"></a>Datentyp

VT \_ bool

## <a name="default-value"></a>Standardwert

false

## <a name="remarks"></a>Bemerkungen

Eine laute Rahmen Kante ist normalerweise die VBI-Daten (Vertical Blank Interval) aus einem Broadcast-TV-Rahmen. VBI stellt die ersten 21 Überprüfungs Linien des Fernseh Rahmens dar. Diese Scan Zeilen enthalten keine Videodaten – Sie enthalten Daten über den Broadcast. Wenn ein Fernsehsignal von einer aufzeichnungskarte aufgezeichnet wird, wird die VBI normalerweise aus dem Frame entfernt. Die vom Codec ausgeführte Erkennung und Korrektur von Noisy Edge kann nur einen Rand korrigieren, der drei oder weniger Rauschen enthält. Wenn das erfasste Video mehr als drei Laute Zeilen enthält, besteht ein Problem mit der Hardware, die zum Erfassen des Videos verwendet wird.

Wenn der Codec darauf festgelegt ist, laute Ränder zu entfernen, werden die Linien, die sich neben dem lärmenden Rand befinden, zum Auffüllen des Frames dupliziert.

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

 

 




