---
description: Aktiviert oder deaktiviert den Miniaturansichtsgenerierungsmodus in einem Videodecoder.
ms.assetid: c640d915-585b-481d-aa49-0d4a559d291c
title: AVDecVideoThumbnailGenerationMode-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eb10b4996a88c8d2e62180edcbfaba8f71b6738d7dc7e3019a0b8ee4b44462d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159991"
---
# <a name="avdecvideothumbnailgenerationmode-property"></a>AVDecVideoThumbnailGenerationMode (Eigenschaft)

Aktiviert oder deaktiviert den Miniaturansichtsgenerierungsmodus in einem Videodecoder.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVDecVideoThumbnailGenerationMode**

## <a name="remarks"></a>Hinweise

Wenn der Wert **VARIANT \_ TRUE ist,** verwendet der Decoder eine Einstellung, die für die schnelle Generierung von Miniaturbildern optimiert ist. (Es kann z. B. B- oder P-Frames überspringen.) Andernfalls verwendet der Decoder seine normalen Decodierungseinstellungen, wenn der Wert **VARIANT \_ FALSE** ist.

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

 

 




