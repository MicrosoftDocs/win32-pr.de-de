---
description: Gibt die letzte Ebene des Codierungspuffers in Bits am Ende des Codierungsprozesses an. Diese Eigenschaft gilt nur für die Codierungsmodi Constant Bit Rate (CBR) und Variable Bit Rate (VBR).
ms.assetid: d5bcdf54-061a-436b-8b1a-61ef7d7c90bf
title: AVEncCommonBufferOutLevel-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77159af0f328dcc6003c21bfa91544070d121e9aad4f8f42caf02853c218926e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103500"
---
# <a name="avenccommonbufferoutlevel-property"></a>AVEncCommonBufferOutLevel (Eigenschaft)

Gibt die letzte Ebene des Codierungspuffers in Bits am Ende des Codierungsprozesses an. Diese Eigenschaft gilt nur für die Codierungsmodi Constant Bit Rate (CBR) und Variable Bit Rate (VBR).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncCommonBufferOutLevel**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft verfügt über einen linearen Wertebereich. Um den unterstützten Bereich zu erhalten, rufen [**Sie ICodecAPI::GetParameterRange auf.**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)

## <a name="remarks"></a>Hinweise

Die -Eigenschaft ist nur verfügbar, wenn die Codierungsdauer im Voraus mithilfe der [**AVEncVideoNoOfFieldsToEncode-Eigenschaft**](avencvideonooffieldstoencode-property.md) oder der [**AVEncAudioIntervalToEncode-Eigenschaft definiert**](avencaudiointervaltoencode-property.md) wird.

Für MPEG-Videos definiert diese Eigenschaft die Vollheit der Videopuffer-Verifizierer (VBV) am Ende des Codierungsprozesses. Sie unterstützt die Verkettung von Streams während der Codierung.

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

 

 




