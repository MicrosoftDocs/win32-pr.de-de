---
description: Legt die maximale Echtzeiteingaberate von Videoframes fest, die an den Encoder gespeist werden.
ms.assetid: ACBE8799-A81C-44C3-B985-88ADFB1E51B4
title: CODECAPI_AVEncMaxFrameRate (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb4202dd2079cc013560947ef11581cdb24b92ad0aaaf544e12923d5e46b319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974929"
---
# <a name="codecapi_avencmaxframerate-property"></a>CODECAPI \_ AVEncMaxFrameRate (Eigenschaft)

Legt die maximale Echtzeiteingaberate von Videoframes fest, die an den Encoder gespeist werden.

## <a name="data-type"></a>Datentyp

**ULONGULONG** (VT \_ UI8)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncMaxFrameRate**

## <a name="remarks"></a>Hinweise

Mit dieser Eigenschaft kann der Aufrufer die maximale Echtzeiteingaberate von Videoframes angeben, die an den Encoder gespeist werden. Dadurch erhält der Encoder einen Hinweis auf die Rate, die er zum Verarbeiten der eingehenden Frames benötigt. Dies ist nützlich für Encoder, die sich basierend auf der Auflösung und Bildfrequenz des Quellvideos auf eine bestimmte Energiezustandskonfiguration festlegen.

Die Bildfrequenz wird als Verhältnis ausgedrückt. Die oberen 32 Bits des Attributwerts enthalten den Zähler, und die unteren 32 Bits enthalten den Nenner. Wenn die Bildfrequenz beispielsweise 30 Frames pro Sekunde (FPS) beträgt, beträgt das Verhältnis 30/1. Wenn die Bildfrequenz 29,97 fps beträgt, beträgt das Verhältnis 30.000/1001.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

