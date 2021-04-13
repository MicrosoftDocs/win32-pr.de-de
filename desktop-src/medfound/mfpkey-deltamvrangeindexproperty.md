---
description: Gibt die Methode an, die zum Codieren der Bewegungsvektor Informationen verwendet wird.
ms.assetid: 22ffdb77-9266-42e5-be41-fc7457141bba
title: MFPKEY_DELTAMVRANGEINDEX-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d923659e64c9a0dcab40811e31d7752924700
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528676"
---
# <a name="mfpkey_deltamvrangeindex-property"></a>Mfpkey- \_ Eigenschaft "Delta-vrangeindex"

Gibt die Methode an, die zum Codieren der Bewegungsvektor Informationen verwendet wird.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcdelta tamvrangeindex

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft festgelegt ist, vergrößert der Encoder den Delta Bewegungsvektor Bereich in Feldern. Bewegungsvektor Informationen sind nur für Zeilen Sprung Felder gültig.

Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden:



| Wert | BESCHREIBUNG                                                                          |
|-------|--------------------------------------------------------------------------------------|
| 0     | Verwenden Sie den vorhandenen Delta Bewegungsvektor Bereich.                                          |
| 1     | Verdoppelt den Delta Bewegungsvektor Bereich in horizontaler Richtung.                    |
| 2     | Verdoppelt den Delta Bewegungsvektor Bereich in vertikaler Richtung.                      |
| 3     | Verdoppeln Sie den Vektor Bereich der Delta Bewegung sowohl in horizontaler als auch in vertikaler Richtung. |



 

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

 

 




