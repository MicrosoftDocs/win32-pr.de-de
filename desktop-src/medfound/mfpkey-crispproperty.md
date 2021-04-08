---
description: Gibt eine numerische Darstellung der Kompromisse zwischen Bewegungs Glätte und Bildqualität der Codec-Ausgabe an.
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: MFPKEY_CRISP-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ff20b37bcedf3995ec3e16178b823c40b352ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755488"
---
# <a name="mfpkey_crisp-property"></a>Mfpkey- \_ Eigenschaft (Crisp)

Gibt eine numerische Darstellung der Kompromisse zwischen Bewegungs Glätte und Bildqualität der Codec-Ausgabe an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvccrisp

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

75

## <a name="remarks"></a>Bemerkungen

Dieser ganzzahlige Wert kann zwischen 0 und 100 liegen. Je höher der Wert ist, desto mehr wird der Codec die Codierung für die Bildqualität einzelner Frames optimieren, was normalerweise die Bewegungs Glätte reduziert.

Diese Eigenschaft sollte nur für die CBR-Codierung (Constant-Bit-Rate) festgelegt werden. Die Optimierungen für die Codierung variabler Bitrate (VBR) funktionieren anders.

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

 

 




