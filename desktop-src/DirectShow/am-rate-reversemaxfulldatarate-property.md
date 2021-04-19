---
description: Gilt für Windows Vista und höher.
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: AM_RATE_ReverseMaxFullDataRate-Eigenschaft (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679e83038a74e64d7a39e8757a9ffaf61fc88c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369153"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a>In \_ Rate \_ reverl maxfulldatarate-Eigenschaft

Gilt für Windows Vista und höher.

Gibt die maximale umgekehrte Wiedergabe Rate des Decoders zurück. Der Wert der-Eigenschaft ist der absolute Wert der maximalen umgekehrten Geschwindigkeit x 10000. Wenn die maximale umgekehrte Geschwindigkeit beispielsweise-2,0 beträgt, ist der Wert dieser Eigenschaft 20000.

Der Datentyp für diese Eigenschaft ist " **am \_ maxfulldatarate**", der `typedef` für " **Long**" ist.

Diese Eigenschaft ist schreibgeschützt.



|                   |                                  |
|-------------------|----------------------------------|
| Eigenschaftensatz-GUID | AM \_ kspropltid \_    |
| Eigenschafts-ID       | Die \_ Rate \_ reverl maxfulldatarate |
| Datentyp         | **AM \_ maxfulldatarate**          |



 

## <a name="remarks"></a>Bemerkungen

Decoderer, die Smooth Reverse-Wiedergabe unterstützen, sollten diese Eigenschaft verfügbar machen. Weitere Informationen finden Sie unter [Verbesserungen der DVD-Wiedergabe in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften Satz für Raten Änderung**](rate-change-property-set.md)
</dt> </dl>

 

 




