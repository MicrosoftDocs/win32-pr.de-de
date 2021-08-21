---
description: Gibt den Nachverarbeitungsmodus für den Decoder an.
ms.assetid: c6dab7f6-4a3e-45bb-b81c-5f4c39f9e954
title: MFPKEY_POSTPROCESSMODE-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce916d0b74c25ae2a57a43acde128ce8c45e7eb42860c3d7a2f129ea2d5b3c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973549"
---
# <a name="mfpkey_postprocessmode-property"></a>MFPKEY \_ POSTPROCESSMODE-Eigenschaft

Gibt den Nachverarbeitungsmodus für den Decoder an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

**g \_ wszWMVCForcePostProcessMode**

## <a name="data-type"></a>Datentyp

**VT \_ I4**

## <a name="remarks"></a>Hinweise

Legen Sie diese Eigenschaft auf einen der folgenden Werte fest.



| Wert | Bedeutung                                                                                |
|-------|----------------------------------------------------------------------------------------|
| -1    | Der Decoder legt den Nachverarbeitungsmodus basierend auf verfügbaren CPU-Ressourcen adaptive fest. |
| 0     | Der Decoder führt keine Nachbearbeitung durch.                                               |
| 1     | fDer Decoder führt eine schnelle Deblockierung durch.                                                 |
| 2     | Der Decoder führt die vollständige Deblockierung durch.                                                  |
| 3     | Der Decoder führt eine schnelle Deblockierung und Deblockierung durch.                                    |
| 4     | Der Decoder führt eine vollständige Deblockierung und Deblockierung durch.                                    |



 

Wenn der Wert dieser Eigenschaft von 0 auf 4 steigt, steigen die Decodierungskomplexität, die Nutzung von CPU-Ressourcen und die Qualität der Bilder.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista oder Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




