---
description: Identifiziert den Hosttyp des WLDP-Aufrufers.
ms.assetid: E8E603CC-9CB2-4C3B-9F06-9B06C7B5D752
title: WLDP_HOST_ID -Enumeration (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_ID
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: fa52bc6259c75d5bb0929cb25610beb2b143515e2874b09bf04c454397a909e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758380"
---
# <a name="wldp_host_id-enumeration"></a>\_ \_ WLDP-HOST-ID-Enumeration

Identifiziert den Hosttyp des WLDP-Aufrufers.

## <a name="syntax"></a>Syntax


```C++
typedef enum _WLDP_HOST_ID { 
   WLDP_HOST_ID_UNKNOWN     = 0,
   WLDP_HOST_ID_GLOBAL      = 1,
  WLDP_HOST_ID_VBA          = 2,
   WLDP_HOST_ID_WSH         = 3,
   WLDP_HOST_ID_POWERSHELL  = 4,
   WLDP_HOST_ID_IE          = 5,
   WLDP_HOST_ID_MSI         = 6,
   WLDP_HOST_ID_MAX         = 7
} WLDP_HOST_ID, *PWLDP_HOST_ID;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span>**WLDP \_ \_HOST-ID \_ UNBEKANNT** 
</dt> <dd>

Der Hosttyp ist unbekannt.

</dd> <dt>

<span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span>**WLDP \_ \_HOST-ID \_ GLOBAL**
</dt> <dd>

Der Hosttyp ist eine globale Richtlinie.

</dd> <dt>

<span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**WLDP \_ HOST \_ ID \_ VBA**
</dt> <dd>

Der Hosttyp ist VBScript.

</dd> <dt>

<span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span>**WLDP \_ \_HOST-ID \_ WSH**
</dt> <dd>

Der Hosttyp ist Windows Skripthost.

</dd> <dt>

<span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span>**WLDP \_ \_HOST-ID \_ POWERSHELL**
</dt> <dd>

Der Hosttyp ist Windows PowerShell.

</dd> <dt>

<span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span>**WLDP \_ \_ \_ HOST-ID-IE**
</dt> <dd>

Der Hosttyp ist Internet Explorer.

</dd> <dt>

<span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span>**WLDP \_ \_HOST-ID \_ MSI**
</dt> <dd>

Der Hosttyp ist der Microsoft Windows Installer.

</dd> <dt>

<span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span>**WLDP \_ \_HOST-ID \_ MAX** 
</dt> <dd>

Der maximale Enumerationswert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wldp.h</dt> </dl> |



 

 




