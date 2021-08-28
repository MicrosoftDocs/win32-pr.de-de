---
description: Gibt die anfängliche Ebene des Codierungspuffers in Bits an. Diese Eigenschaft gilt nur für Codierungsmodi mit konstanter Bitrate (CBR) und variabler Bitrate (VBR).
ms.assetid: 92ec9483-443e-4723-8795-9bf847c36131
title: AVEncCommonBufferInLevel-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e1e2b1d5b27d405d5b2a4c69cd9503d1c4f2815356e31c9a165f52d215e806d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873380"
---
# <a name="avenccommonbufferinlevel-property"></a>AVEncCommonBufferInLevel (Eigenschaft)

Gibt die anfängliche Ebene des Codierungspuffers in Bits an. Diese Eigenschaft gilt nur für Codierungsmodi mit konstanter Bitrate (CBR) und variabler Bitrate (VBR).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncCommonBufferInLevel**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft verfügt über einen linearen Wertebereich. Um den unterstützten Bereich zu erhalten, rufen [**Sie ICodecAPI::GetParameterRange auf.**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)

## <a name="remarks"></a>Hinweise

Für MPEG-Videos definiert diese Eigenschaft die ursprüngliche Fullness der Videopuffer-Verifizierer (VBV). Sie unterstützt die Verkettung von Streams während der Codierung.

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

 

 




