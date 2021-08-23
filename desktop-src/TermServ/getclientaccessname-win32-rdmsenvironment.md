---
title: GetClientAccessName-Methode der Win32_RDMSEnvironment-Klasse
description: Ruft den namen Domain Name System (DNS) der RDMS-Umgebung (Remotedesktop Management Services) ab.
ms.assetid: 16f9d00d-a398-4a73-a641-ac552ba6a9d3
ms.tgt_platform: multiple
keywords:
- GetClientAccessName-Remotedesktopdienste
- GetClientAccessName-Methode Remotedesktopdienste , Win32_RDMSEnvironment-Klasse
- Win32_RDMSEnvironment klasse Remotedesktopdienste , GetClientAccessName-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 206ef89765bd18a73559c98d70a614664d076099214bd20f7b97ca9c29e94bc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139003"
---
# <a name="getclientaccessname-method-of-the-win32_rdmsenvironment-class"></a>GetClientAccessName-Methode der Win32 \_ RDMSEnvironment-Klasse

Ruft den namen Domain Name System (DNS) der RDMS-Umgebung (Remotedesktop Management Services) ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetClientAccessName(
  [out] string ClientAccessName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ClientAccessName* \[ out\]
</dt> <dd>

Empfängt den abgerufenen RR-Namen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\Stamm-CIMv2-Rdms \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ RDMSUmgebung**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





