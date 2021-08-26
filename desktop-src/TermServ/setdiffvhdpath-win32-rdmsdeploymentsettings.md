---
title: SetDiffVHDPath-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Aktualisiert den Verzeichnispfad, in dem die differenzierenden Datenträger für eine Sammlung virtueller Desktops bereitgestellt werden.
ms.assetid: 665ffbf9-0250-4956-9bce-f5a6714b47e4
ms.tgt_platform: multiple
keywords:
- SetDiffVHDPath-Methode Remotedesktopdienste
- SetDiffVHDPath-Methode Remotedesktopdienste , Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings Klasse Remotedesktopdienste , SetDiffVHDPath-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d275f848bb29c9cac4930f738a9a123cc6aa3a8e80a77b746f2495d44f68cf96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988040"
---
# <a name="setdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>SetDiffVHDPath-Methode der Win32 \_ RDMSDeploymentSettings-Klasse

Aktualisiert den Verzeichnispfad, in dem die differenzierenden Datenträger für eine Sammlung virtueller Desktops bereitgestellt werden.

## <a name="syntax"></a>Syntax


```mof
uint32 SetDiffVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DirectoryPath* \[ In\]
</dt> <dd>

Der neue differenzierende Datenträgerpfad.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\Stamm-CIMv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ RDMSDeploymentSettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





