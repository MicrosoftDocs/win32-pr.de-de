---
title: Getclientaccessname-Methode der Win32_RDMSEnvironment-Klasse
description: Ruft den Namen der Domain Name System (DNS) Resource Record (RR) der Remotedesktop Management Services (RDMs)-Umgebung ab.
ms.assetid: 16f9d00d-a398-4a73-a641-ac552ba6a9d3
ms.tgt_platform: multiple
keywords:
- Getclientaccessname-Methode Remotedesktopdienste
- Getclientaccessname-Methode Remotedesktopdienste, Win32_RDMSEnvironment-Klasse
- Win32_RDMSEnvironment-Klasse Remotedesktopdienste, getclientaccessname-Methode
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
ms.openlocfilehash: f54662cf1f27c53f3bf69398a203bfdfce1e53c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337294"
---
# <a name="getclientaccessname-method-of-the-win32_rdmsenvironment-class"></a>Getclientaccessname-Methode der Win32 \_ rdmsenvironment-Klasse

Ruft den Namen der Domain Name System (DNS) Resource Record (RR) der Remotedesktop Management Services (RDMs)-Umgebung ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetClientAccessName(
  [out] string ClientAccessName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Clientaccessname* \[ vorgenommen\]
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
| Namespace<br/>                | Root \\ CIMv2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ rdmsenvironment**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





