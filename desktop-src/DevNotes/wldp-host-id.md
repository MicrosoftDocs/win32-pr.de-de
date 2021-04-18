---
description: Identifiziert den Hosttyp des wldp-Aufrufers.
ms.assetid: E8E603CC-9CB2-4C3B-9F06-9B06C7B5D752
title: WLDP_HOST_ID-Enumeration (wldp. h)
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
ms.openlocfilehash: 8914f93ff5936451b71b855473a09cb1d06584b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522923"
---
# <a name="wldp_host_id-enumeration"></a>Wldp- \_ Host- \_ ID-Enumeration

Identifiziert den Hosttyp des wldp-Aufrufers.

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

<span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span>**Wldp \_ Host- \_ ID \_ unbekannt** 
</dt> <dd>

Der Hosttyp ist unbekannt.

</dd> <dt>

<span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span>**Wldp \_ Host- \_ ID \_ Global**
</dt> <dd>

Der Hosttyp ist eine globale Richtlinie.

</dd> <dt>

<span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**wldp- \_ Host- \_ ID \_ VBA**
</dt> <dd>

Der Hosttyp ist "VBScript".

</dd> <dt>

<span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span>**Wldp \_ Host- \_ ID \_ WSH**
</dt> <dd>

Der Hosttyp ist "Windows Script Host".

</dd> <dt>

<span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span>**Wldp \_ Host- \_ ID \_ PowerShell**
</dt> <dd>

Der Hosttyp ist Windows PowerShell.

</dd> <dt>

<span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span>**Wldp \_ Host- \_ ID \_ IE**
</dt> <dd>

Der Hosttyp ist "Internet Explorer".

</dd> <dt>

<span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span>**Wldp \_ Host- \_ ID- \_ MSI**
</dt> <dd>

Der Hosttyp ist der Microsoft Windows Installer.

</dd> <dt>

<span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span>**Wldp \_ Host- \_ ID \_ Max** 
</dt> <dd>

Der maximale Enumerationswert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Wldp. h</dt> </dl> |



 

 




