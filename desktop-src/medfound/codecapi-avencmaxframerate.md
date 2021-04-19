---
description: Legt die maximale echt Zeiteingabe Rate der Video Frames fest, die an den Encoder ausgegeben werden.
ms.assetid: ACBE8799-A81C-44C3-B985-88ADFB1E51B4
title: CODECAPI_AVEncMaxFrameRate-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c04d1fd1297f299db133cd98bd493c968fcc29c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344236"
---
# <a name="codecapi_avencmaxframerate-property"></a>Codecapi- \_ Eigenschaft "avencmaxframerate"

Legt die maximale echt Zeiteingabe Rate der Video Frames fest, die an den Encoder ausgegeben werden.

## <a name="data-type"></a>Datentyp

**Ulongulong** (VT \_ UI8)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencmaxframerate**

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ermöglicht es dem Aufrufer, die maximale echt Zeiteingabe Rate der Video Frames anzugeben, die an den Encoder übergeben werden. Dadurch erhält der Encoder einen Hinweis auf die Geschwindigkeit, mit der die eingehenden Frames verarbeitet werden müssen. Dies ist hilfreich bei Encodern, die sich auf Grundlage der Auflösung und der Framerate des Quellvideos in einer bestimmten Energie Zustands Konfiguration befinden.

Die Framerate wird als Verhältnis ausgedrückt. Die oberen 32 Bits des Attribut Werts enthalten den Zähler, und die unteren 32 Bits enthalten den Nenner. Wenn die Framerate z. b. 30 Frames pro Sekunde (fps) ist, ist das Verhältnis 30/1. Wenn die Framerate 29,97 fps beträgt, ist das Verhältnis 30.000/1001.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**Icodecapi**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

