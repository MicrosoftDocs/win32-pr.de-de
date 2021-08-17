---
description: Gibt die Kanalmatrix an, die verwendet wird, um die Quellkanäle in die Zielkanäle zu konvertieren (z. B. um 5.1 in Stereo zu konvertieren).
ms.assetid: 2f2a82bd-f051-4b05-a9c8-37aa4403fab4
title: MFPKEY_WMRESAMP_CHANNELMTX-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a326cfe27632204f2975ac8b7c3a605c666464f8f62846a5c622a469f2f6e104
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689254"
---
# <a name="mfpkey_wmresamp_channelmtx-property"></a>MFPKEY \_ WMRESAMP \_ CHANNELMTX-Eigenschaft

Gibt die Kanalmatrix an, die verwendet wird, um die Quellkanäle in die Zielkanäle zu konvertieren (z. B. um 5.1 in Stereo zu konvertieren).

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4 \| VT \_ ARRAY

## <a name="applies-to"></a>Gilt für

-   [Audio-Resampler-DSP](audioresampler.md)

## <a name="remarks"></a>Hinweise

Der Wert der -Eigenschaft ist eine Matrix von Ns x Nd-Koeffizienten, wobei Ns die Anzahl der Quellkanäle und Nd die Anzahl der Zielkanäle ist. Koeffizienten werden mithilfe der folgenden Formel in Decibeln angegeben:

(int) (65536 \* 20 \* log10(dB))

Die Matrix wird als Array in Zeilenhauptreihenfolge gespeichert, wobei die Zeilennummer der Quellkanal und die Spaltennummer der Zielkanal ist.

Wenn die Matrix also wie folgt lautet:

``` syntax
00       01       ...      0(Ns-1)
10       11       ...      1(Ns-1)
...      ...      ...      ...
(Nd-1)0 (Nd-1)1 ... (Nd-1)(Ns-1)
```

dann würden Sie das Array wie die folgende angeben:

``` syntax
[ 00, 01, ..., 0(Ns-1), 10, 11, ..., 1(Ns-1), ..., (Nd-1)0, (Nd-1)1, ..., (Nd-1)(Ns-1) ]
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
