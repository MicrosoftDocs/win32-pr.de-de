---
description: 'AVEncAudioDualMono-Eigenschaft: Gibt an, ob 2-Kanal-Audio als Stereo oder Dual Mono codiert wird.'
ms.assetid: 37f25590-69c2-43bd-a5d4-2262457cb39d
title: AVEncAudioDualMono-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58cbd901079d8f4dede1efae140791ae99c7fed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096578"
---
# <a name="avencaudiodualmono-property"></a>AVEncAudioDualMono (Eigenschaft)

Gibt an, ob 2-Kanal-Audio als Stereo oder Dual Mono codiert wird.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncAudioDualMono**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein Member der [**eAVEncAudioDualMono-Enumeration.**](/windows/win32/api/codecapi/ne-codecapi-eavencaudiodualmono)

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gilt nicht für MPEG-Audioencoder. Verwenden Sie für MPEG-Audio die [**EIGENSCHAFT AVEncMPACodingMode.**](avencmpacodingmode-property.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | UWP-Apps für Windows 2000 \[ \| Professional-Desktop-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

