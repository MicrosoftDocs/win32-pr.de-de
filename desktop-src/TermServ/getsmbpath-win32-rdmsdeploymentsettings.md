---
title: Getsmbpath-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Ruft den UNC-Pfad zur SMB-Freigabe ab, auf der virtuelle Maschinen der virtuellen Desktop Sammlung bereitgestellt werden.
ms.assetid: 0a5d3c11-6a77-48f7-a3ea-6f82725ff01f
ms.tgt_platform: multiple
keywords:
- Getsmbpath-Methode Remotedesktopdienste
- Getsmbpath-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, getsmbpath-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSMBPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1738faf82a6405018495dd762ba9585daa3e1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392228"
---
# <a name="getsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Getsmbpath-Methode der Win32 \_ rdmsdeploymentsettings-Klasse

Ruft den UNC-Pfad zur SMB-Freigabe ab, auf der virtuelle Maschinen der virtuellen Desktop Sammlung bereitgestellt werden.

## <a name="syntax"></a>Syntax


```mof
uint32 GetSMBPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Directoriypath* \[ vorgenommen\]
</dt> <dd>

Empfängt einen UNC-formatierten Pfad zur SMB-Freigabe.

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

[**Win32 \_ rdmsdeploymentsettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





