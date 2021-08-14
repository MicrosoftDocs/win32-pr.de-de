---
description: Eine Struktur, die den Host und die Quelldatei identifiziert, die ausgewertet werden sollen.
ms.assetid: 547EF59E-7DE5-45E4-948F-109547FAAEE7
title: WLDP_HOST_INFORMATION-Struktur (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_INFORMATION
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: cc1bed8fd104b4aa6abb83d3eb7e19faa37a0301429312c8f0799e256ce32ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404069"
---
# <a name="wldp_host_information-structure"></a>Struktur der \_ WLDP-HOSTINFORMATIONEN \_

Eine Struktur, die den Host und die Quelldatei identifiziert, die ausgewertet werden sollen.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WLDP_HOST_INFORMATION {
  DWORD        dwRevision;
  WLDP_HOST_ID dwHostId;
  PCWSTR       szSource;
  HANDLE       hSource;
} WLDP_HOST_INFORMATION, *PWLDP_HOST_INFORMATION;
```



## <a name="members"></a>Member

<dl> <dt>

**dwRevision**
</dt> <dd>

Muss **WLDP \_ HOST \_ INFORMATION \_ REVISION** sein.

</dd> <dt>

**dwHostId**
</dt> <dd>

Enumerationswert aus [**der WLDP-HOST-ID, \_ \_**](wldp-host-id.md) der die Host-ID beschreibt.

</dd> <dt>

**szSource**
</dt> <dd>

Vollständiger Pfad und Skriptname mit der Erweiterung. NULL für **WLDP \_ HOST ID \_ \_ GLOBAL** oder manuelle Skriptausführung.

</dd> <dt>

**hSource**
</dt> <dd>

Zusätzlich zum Namen kann der Aufrufer ein Handle für die Datei angeben, die für die Validierung verwendet wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wldp.h</dt> </dl> |



 

 




