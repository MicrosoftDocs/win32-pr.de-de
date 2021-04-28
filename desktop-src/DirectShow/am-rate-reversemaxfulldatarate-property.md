---
description: 'AM_RATE_ReverseMaxFullDataRate-Eigenschaft: Gilt für Windows Vista und höher.'
ms.assetid: 4f170736-516d-4420-a215-e0e414f036cd
title: AM_RATE_ReverseMaxFullDataRate-Eigenschaft (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6e70a330433c8ea6e8116db944d8fb3d2ffff4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099968"
---
# <a name="am_rate_reversemaxfulldatarate-property"></a>AM \_ RATE \_ ReverseMaxFullDataRate-Eigenschaft

Gilt für Windows Vista und höher.

Gibt die maximale umgekehrte Wiedergaberate des Decoders zurück. Der Wert der -Eigenschaft ist der absolute Wert der maximalen Umgekehrtgeschwindigkeit x 10000. Wenn die maximale Umgekehrtgeschwindigkeit beispielsweise -2,0 beträgt, ist der Wert dieser Eigenschaft 20000.

Der Datentyp für diese Eigenschaft ist **AM \_ MaxFullDataRate**, bei dem es sich um einen `typedef` für **LONG** handelt.

Diese Eigenschaft ist schreibgeschützt.



| Bezeichnung | Wert |
|-------------------|----------------------------------|
| Eigenschaftensatz-GUID | AM \_ KSPROPSETID \_ TSRateChange    |
| Eigenschafts-ID       | AM \_ RATE \_ ReverseMaxFullDataRate |
| Datentyp         | **AM \_ MaxFullDataRate**          |



 

## <a name="remarks"></a>Bemerkungen

Decoder, die eine reibungslose umgekehrte Wiedergabe unterstützen, sollten diese Eigenschaft verfügbar machen. Weitere Informationen finden Sie unter [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Ratenänderungseigenschaftensatz**](rate-change-property-set.md)
</dt> </dl>

 

 




