---
title: SetBaseVHDPath-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Ruft den Basispfad zu dem Verzeichnis ab, in dem VHDs der Sammlung virtueller Desktops bereitgestellt werden. | SetBaseVHDPath-Methode der Win32_RDMSDeploymentSettings Klasse
ms.assetid: 1ea4cd93-ef17-4ec9-82f9-382c549f189c
ms.tgt_platform: multiple
keywords:
- SetBaseVHDPath-Remotedesktopdienste
- SetBaseVHDPath-Methode Remotedesktopdienste , Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings klasse Remotedesktopdienste , SetBaseVHDPath-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6179c87e6566a18f2c47046007a17c6073a51e0afcdce4925b50d327adf528f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605117"
---
# <a name="setbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>SetBaseVHDPath-Methode der Win32 \_ RDMSDeploymentSettings-Klasse

Ruft den Basispfad zu dem Verzeichnis ab, in dem VHDs der Sammlung virtueller Desktops bereitgestellt werden.

## <a name="syntax"></a>Syntax


```mof
uint32 SetBaseVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DirectoryPath* \[ In\]
</dt> <dd>

Der neue VHD-Bereitstellungspfad.

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

[**Win32 \_ RDMSDeploymentSettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





