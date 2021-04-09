---
description: Gibt an, ob der Codec die Optimierung der Video Skalierung verwendet.
ms.assetid: a21d0100-e020-4e74-b8e3-bb7071194828
title: MFPKEY_VIDEOSCALING-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555cec22533b7817c509d5419391039b10c92576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863983"
---
# <a name="mfpkey_videoscaling-property"></a>Mfpkey- \_ videosc-Eigenschaft

Gibt an, ob der Codec die Optimierung der Video Skalierung verwendet.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcvideosc.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Bemerkungen

Die Video Skalierung ist eine Art von perzeptueller Optimierung, die die visuelle Qualität von Videos verbessert, die zu niedrigen Bitraten codiert sind. Die Video Skalierungs Optimierung reduziert ausgeprägte Artefakte, kann aber auch Bilddetails Opfern. Diese Optimierung wirkt sich auf den Luma-Bereich des codierten Videos aus, wie unten beschrieben, wirkt sich jedoch nicht auf die physische Auflösung des Ausgabevideos aus.

Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.



| Wert | BESCHREIBUNG                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------|
| 0     | Die Video Skalierung wird nicht verwendet.                                                                                       |
| 1     | Der Encoder verwendet die konservative Video Skalierungs Optimierung. Der Bereich "Luma" wird von 0... 255 auf 26... 229 skaliert. |
| 2     | Der Encoder verwendet die aggressive Optimierung der Video Skalierung. Der Bereich "Luma" wird von 0... 255 bis 31... 224 skaliert.   |



 

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

 

 




