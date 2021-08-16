---
description: Eine -Struktur, die einen einzelnen Farbwert beschreibt.
ms.assetid: 710f3ef1-bbc3-416d-9faf-aa4a716007c2
title: XPS_COLOR (Xpsobjectmodel.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f771bcbb516352b2ef689060c11003808d434be8059d16af78fe8db646c97000
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971149"
---
# <a name="xps_color"></a>XPS \_ COLOR

Eine -Struktur, die einen einzelnen Farbwert beschreibt.

``` syntax
typedef union switch (XPS_COLOR_TYPE colorType) value
{
    case XPS_COLOR_TYPE_SRGB:
        struct {
            byte alpha, red, green, blue;
        } sRGB;
    case XPS_COLOR_TYPE_SCRGB:
        struct {
            FLOAT alpha, red, green, blue;
        } scRGB;
    case XPS_COLOR_TYPE_CONTEXT:
        struct {
            byte channelCount;
            FLOAT channels[9];
        } context;
} XPS_COLOR;
```

## <a name="remarks"></a>Hinweise

Das Format der Struktur hängt vom Wert von *colorType* ab.

<dl>

[**XPS \_ COLOR \_ TYPE \_ SRGB**](/previous-versions/windows/desktop/dd372944(v=vs.85))  
[**XPS \_ COLOR \_ TYPE \_ SCRGB**](/previous-versions/windows/desktop/dd372943(v=vs.85))  
[**\_ \_ XPS-FARBTYPKONTEXT \_**](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color)  
</dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7, Windows Vista mit SP2 und Plattformupdate für UWP-Apps für Windows \[ \| Vista-Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Plattformupdate für Windows Server \[ 2008-Desktop-Apps \| UWP-Apps\]<br/> |
| Header<br/>                   | <dl> <dt>Xpsobjectmodel.h</dt> </dl>                                              |
| Idl<br/>                      | <dl> <dt>XpsObjectModel.idl</dt> </dl>                                            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

