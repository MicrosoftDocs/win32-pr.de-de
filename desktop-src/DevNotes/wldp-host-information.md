---
description: Eine-Struktur, die den zu bewertenden Host und die Quelldatei identifiziert.
ms.assetid: 547EF59E-7DE5-45E4-948F-109547FAAEE7
title: WLDP_HOST_INFORMATION Struktur (wldp. h)
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
ms.openlocfilehash: ad20be7fa5887e42c09248d04e14f5ff8cffcd54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041341"
---
# <a name="wldp_host_information-structure"></a>Wldp- \_ Host \_ Informationsstruktur

Eine-Struktur, die den zu bewertenden Host und die Quelldatei identifiziert.

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

**dwrevision**
</dt> <dd>

Muss eine **wldp- \_ Host \_ Informations \_ Revision** sein.

</dd> <dt>

**dwhostid**
</dt> <dd>

Enumerationswert aus der [**wldp- \_ Host- \_ ID**](wldp-host-id.md) , die die Host-ID beschreibt.

</dd> <dt>

**szsource**
</dt> <dd>

Vollständiger Pfad-und Skript Name mit der Erweiterung. NULL für die **globale wldp- \_ Host- \_ ID \_** oder die manuelle Skriptausführung.

</dd> <dt>

**hsource**
</dt> <dd>

Zusätzlich zum Namen kann der Aufrufer ein Handle für die Datei angeben, die für die Validierung verwendet wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wldp. h</dt> </dl> |



 

 




