---
description: Gibt an, ob ein AAC-Decoder standardmäßige MPEG-2/MPEG-4 Stereo-Downmixgleichungen oder einen nicht standardmäßigen Downmix verwendet.
ms.assetid: a384d24e-07e2-45e7-84b8-e791feb64a83
title: AVDecAACDownmixMode-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3fde61acdd5d29574f316e269d5b04a0a94649827777504fe31c33bbf79bd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641280"
---
# <a name="avdecaacdownmixmode-property"></a>AVDecAACDownmixMode-Eigenschaft

Gibt an, ob ein AAC-Decoder standardmäßige MPEG-2/MPEG-4 Stereo-Downmixgleichungen oder einen nicht standardmäßigen Downmix verwendet.

Ein Beispiel für ein nicht standardmäßiges Downmix ist das im ARIB-Dokument STD-B21 Version 4.4 definierte Downmix.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVDecAACDownmixMode**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein Member der [**eAVDecAACDownmixMode-Enumeration.**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode)

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

 

