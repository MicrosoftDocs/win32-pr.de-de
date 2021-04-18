---
description: Gibt die Kanal Matrix an, die verwendet wird, um die Quell Kanäle in die Ziel Kanäle zu konvertieren (z. b. um 5,1 in Stereo umzuwandeln).
ms.assetid: 2f2a82bd-f051-4b05-a9c8-37aa4403fab4
title: MFPKEY_WMRESAMP_CHANNELMTX-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e39f9a9344dd080362859592fcf1f71657ee8f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354623"
---
# <a name="mfpkey_wmresamp_channelmtx-property"></a>Mfpkey \_ wmresamp \_ channelmtx-Eigenschaft

Gibt die Kanal Matrix an, die verwendet wird, um die Quell Kanäle in die Ziel Kanäle zu konvertieren (z. b. um 5,1 in Stereo umzuwandeln).

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4 \| VT- \_ Array

## <a name="applies-to"></a>Gilt für

-   [Audioresampler-DSP](audioresampler.md)

## <a name="remarks"></a>Bemerkungen

Der Wert der-Eigenschaft ist eine Matrix aus NS x-Koeffizienten, wobei "NS" die Anzahl der Quell Kanäle und "ND" die Anzahl der Ziel Kanäle ist. Koeffizienten werden mithilfe der folgenden Formel in Dezibel angegeben:

wartenden (65536 \* 20 \* log10 (DB))

Die Matrix wird als Array in der Reihenfolge der Zeilen in der Reihenfolge gespeichert, in der die Zeilennummer der Quell Kanal und die Spaltennummer der Zielchannel ist.

Wenn die Matrix beispielsweise folgendermaßen lautet:

``` syntax
00       01       ...      0(Ns-1)
10       11       ...      1(Ns-1)
...      ...      ...      ...
(Nd-1)0 (Nd-1)1 ... (Nd-1)(Ns-1)
```

Anschließend geben Sie das Array wie folgt an:

``` syntax
[ 00, 01, ..., 0(Ns-1), 10, 11, ..., 1(Ns-1), ..., (Nd-1)0, (Nd-1)1, ..., (Nd-1)(Ns-1) ]
```

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

 

 
