---
description: Ruft die Größe des decodierten Bilds in Pixel ab.
ms.assetid: 2F0DD10F-CF7A-4A6F-91A9-E3828DF2B947
title: AVDecVideoImageSize-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4c059dfb1b2aebad4da10e54a3ecc1224a00d9cffcdb13dc7c87f4e29d4e83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000190"
---
# <a name="avdecvideoimagesize-property"></a>AVDecVideoImageSize (Eigenschaft)

Ruft die Größe des decodierten Bilds in Pixel ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVDecVideoImageSize**

## <a name="property-value"></a>Eigenschaftswert

Die hohen 16 Bits enthalten die Breite, und die unteren 16 Bits enthalten die Höhe.

## <a name="remarks"></a>Hinweise

Die Anzahl der Kanäle schließt den LFE-Kanal (Low Frequency Effect) ein, falls vorhanden.

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

 

 




