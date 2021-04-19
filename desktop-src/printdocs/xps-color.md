---
description: Eine-Struktur, die einen einzelnen Farbwert beschreibt.
ms.assetid: 710f3ef1-bbc3-416d-9faf-aa4a716007c2
title: XPS_COLOR (xpsobjectmodel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34c148c2a5452154bfe33b0c74d695fe78f0cdad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362662"
---
# <a name="xps_color"></a>XPS- \_ Farbe

Eine-Struktur, die einen einzelnen Farbwert beschreibt.

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

## <a name="remarks"></a>Bemerkungen

Das Format der Struktur hängt vom Wert von *ColorType* ab.

<dl>

[**XPS \_ - \_ Farbtyp \_ sRGB**](/previous-versions/windows/desktop/dd372944(v=vs.85))  
[**XPS \_ - \_ Farbtyp \_ ScRGB**](/previous-versions/windows/desktop/dd372943(v=vs.85))  
[**XPS \_ - \_ Farbtyp \_ Kontext**](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color)  
</dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]<br/> |
| Header<br/>                   | <dl> <dt>Xpsobjectmodel. h</dt> </dl>                                              |
| IDL<br/>                      | <dl> <dt>Xpsobjectmodel. idl</dt> </dl>                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

