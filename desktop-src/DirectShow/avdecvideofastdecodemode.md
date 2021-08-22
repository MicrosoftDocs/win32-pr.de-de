---
description: Ruft die Geschwindigkeit der Videodecodierung ab oder legt sie fest.
ms.assetid: 76F7013D-C172-4D31-93BC-EA3D186EB14C
title: AVDecVideoFastDecodeMode-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f36cd765754e73924caae401495e597ec69828ed62f08466884b10365517d17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503139"
---
# <a name="avdecvideofastdecodemode-property"></a>AVDecVideoFastDecodeMode-Eigenschaft

Ruft die Geschwindigkeit der Videodecodierung ab oder legt sie fest.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVDecVideoFastDecodeMode**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft kann zwischen 0 und 32 liegen, wobei 0 auf die normale Decodierung hinweist und 32 der schnellste Decodierungsmodus ist. Das genaue Verhalten hängt von der Decoderimplementierungen ab. Nicht jedes Inkrement zwischen 1 und 32 definiert notwendigerweise einen eindeutigen Modus.

Die [**eAVFastDecodeMode-Enumeration**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) enthält einige vordefinierte Modi für diese Eigenschaft.

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

 

 




