---
description: Legt den Schwellenwert fest, bei dem der Encoder ein Videofeld redundant betrachtet.
ms.assetid: db6c2f0e-f451-4d2d-984f-b507083e8358
title: AVEncVideoInverseTelecineThreshold-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 297dae601c5112714272a2d1c2e0b1a7ebeee5faa3aa2fabebc32e79c1745c9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119275179"
---
# <a name="avencvideoinversetelecinethreshold-property"></a>AVEncVideoInverseTelecineThreshold (Eigenschaft)

Legt den Schwellenwert fest, bei dem der Encoder ein Videofeld redundant betrachtet.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncVideoInverseTelecineThreshold**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft hat den folgenden Bereich.



| Wert | BESCHREIBUNG                                                    |
|-------|----------------------------------------------------------------|
| 0     | Der Encoder betrachtet Videofelder weniger wahrscheinlich als redundant. |
| 100   | Der Encoder betrachtet Videofelder eher als redundant. |



 

## <a name="remarks"></a>Hinweise

Legen Sie diese Eigenschaft fest, wenn der Encoder eine umgekehrte Telecine mit einer analogen Videoquelle vorsteuert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




