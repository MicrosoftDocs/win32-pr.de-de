---
description: Gibt an, ob der Decoder Intraframes mit fehlenden Verweisframes löscht.
ms.assetid: 9007d5a8-f498-4394-a4e6-02a7616f3e2a
title: AVDecVideoDropPicWithMissingRef-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ac5e8c02c63c977d8d5a8e47bb5d6f878c538364ac2fe5b65c1e691c84ca23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000320"
---
# <a name="avdecvideodroppicwithmissingref-property"></a>AVDecVideoDropPicWithMissingRef (Eigenschaft)

Gibt an, ob der Decoder Intraframes mit fehlenden Verweisframes löscht.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVDecVideoDropPicWithMissingRef**

## <a name="remarks"></a>Hinweise

Wenn der Bitstream beschädigt ist, fehlen in einem Frame möglicherweise Verweisframes. Wenn der Wert dieser Eigenschaft **VARIANT \_ TRUE ist,** löscht der Decoder den Frame. Wenn der Wert **VARIANT \_ FALSE** ist, versucht der Decoder, den Frame zu decodieren, indem mindestens ein Frame in der Nähe als Referenzframes verwendet wird. Der resultierende decodierte Frame hat blockierende Artefakte.

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

 

 




