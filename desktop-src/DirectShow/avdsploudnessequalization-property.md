---
description: Aktiviert oder deaktiviert die Lautheitsgleichheit in einem Audiodecoder oder digitalen Signalprozessor (Digital Signal Processor, DSP).
ms.assetid: f02b187f-1bcb-47b3-8ac2-018ed30491c6
title: AVDSPLoudnessEqualization-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61696b51996d6fe57cf15372d511704e2dad482f0a5e99eb165795f56256656a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052830"
---
# <a name="avdsploudnessequalization-property"></a>AVDSPLoudnessEqualization-Eigenschaft

Aktiviert oder deaktiviert die Lautheitsgleichheit in einem Audiodecoder oder digitalen Signalprozessor (Digital Signal Processor, DSP).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVDSPLoudnessEqualization**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein Member der [**eAVDSPLoudnessEqualization-Enumeration.**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization)

## <a name="remarks"></a>Hinweise

Bei der Lautheitsgleichheit handelt es sich um einen DSP-Prozess, der eine konsistente Lautstärke beibehält, wenn sich der Audiostream ändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




