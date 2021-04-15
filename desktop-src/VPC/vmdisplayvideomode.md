---
title: Vmdisplayvideomode-Enumeration (vpccominterfaces. h)
description: Gibt den Videomodus für die Anzeige an.
ms.assetid: 9ffd1bb5-115d-4554-92c6-5dcf86f904a5
keywords:
- Vmdisplayvideomode-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMDisplayVideoMode
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b159a8c251c83643ae9897842b313ea9be567e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476545"
---
# <a name="vmdisplayvideomode-enumeration"></a>Vmdisplayvideomode-Enumeration

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Gibt den Videomodus für die Anzeige an.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmVideoMode_TextMode  = 0,
  vmVideoMode_CGAMode   = 1,
  vmVideoMode_VGAMode   = 2,
  vmVideoMode_SVGAMode  = 3
} VMDisplayVideoMode;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="vmVideoMode_TextMode"></span><span id="vmvideomode_textmode"></span><span id="VMVIDEOMODE_TEXTMODE"></span>**vmvideomode- \_ TextMode**
</dt> <dd>

Textmodus.

</dd> <dt>

<span id="vmVideoMode_CGAMode"></span><span id="vmvideomode_cgamode"></span><span id="VMVIDEOMODE_CGAMODE"></span>**vmvideomode \_ cgamode**
</dt> <dd>

CGA-Modus.

</dd> <dt>

<span id="vmVideoMode_VGAMode"></span><span id="vmvideomode_vgamode"></span><span id="VMVIDEOMODE_VGAMODE"></span>**vmvideomode \_ vgamode**
</dt> <dd>

Der VGA-Modus.

</dd> <dt>

<span id="vmVideoMode_SVGAMode"></span><span id="vmvideomode_svgamode"></span><span id="VMVIDEOMODE_SVGAMODE"></span>**vmvideomode \_ svgamode**
</dt> <dd>

SVGA-Modus.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmdisplay:: videomode**](ivmdisplay-videomode.md)
</dt> </dl>

 

