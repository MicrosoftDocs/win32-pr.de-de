---
description: Gibt die Schutz Ebene für Videoinhalte an.
ms.assetid: 681c6ad9-cf55-47e4-bbb9-e7fdc499a709
title: D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS-Struktur (D3d9types. h)
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
ms.openlocfilehash: 2d3111d01f178be3128dcb79f65d2155195c2e4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346255"
---
# <a name="d3dauthenticatedchannel_protection_flags-structure"></a>D3DAUTHENTICATEDCHANNEL \_ \_ Schutzflags-Struktur

Gibt die Schutz Ebene für Videoinhalte an.

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

**Schutz aktiviert**
</dt> <dd>

Wenn der Wert 1 ist, ist der Schutz von Videoinhalten aktiviert.

</dd> <dt>

**Overlayorfullscreenrequired**
</dt> <dd>

Wenn 1, erfordert die Anwendung, dass Videos entweder mithilfe eines Hardware Überlagerungs-oder Vollbildmodus angezeigt werden.

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert. Legen Sie alle Bits auf 0 fest.

</dd> <dt>

**Wert**
</dt> <dd>

Verwenden Sie diesen Member für den Zugriff auf alle Bits in der Union.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Video Strukturen](direct3d-video-structures.md)
</dt> </dl>

 

 




