---
description: Gibt die Schutzebene für Videoinhalte an.
ms.assetid: 681c6ad9-cf55-47e4-bbb9-e7fdc499a709
title: D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS-Struktur (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1d1b76a6fea0dd6b966bd72001efb187a7a3a14e75b4d41d631e5a1ea163fe94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974709"
---
# <a name="d3dauthenticatedchannel_protection_flags-structure"></a>D3DAUTHENTICATEDCHANNEL \_ PROTECTION \_ FLAGS-Struktur

Gibt die Schutzebene für Videoinhalte an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS {
  union {
    struct {
      UINT ProtectionEnabled  :1;
      UINT OverlayOrFullscreenRequired  :1;
      UINT Reserved  :30;
    };
    UINT   Value;
  };
} D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS;
```



## <a name="members"></a>Member

<dl> <dt>

**ProtectionEnabled**
</dt> <dd>

Bei 1 ist der Schutz von Videoinhalten aktiviert.

</dd> <dt>

**OverlayOrFullscreenRequired**
</dt> <dd>

Bei 1 muss das Video für die Anwendung entweder über eine Hardwareüberlagerung oder im exklusiven Vollbildmodus angezeigt werden.

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert. Legen Sie alle Bits auf 0 (null) fest.

</dd> <dt>

**Wert**
</dt> <dd>

Verwenden Sie diesen Member, um auf alle Bits in der Union zuzugreifen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Videostrukturen](direct3d-video-structures.md)
</dt> </dl>

 

 




