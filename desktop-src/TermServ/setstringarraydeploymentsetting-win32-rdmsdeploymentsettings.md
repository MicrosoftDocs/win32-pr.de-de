---
title: Setstringarraydeploymentsetting-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Aktualisiert die Bereitstellungs Einstellungen für eine Sammlung virtueller Desktops.
ms.assetid: 386594bd-a793-4e5d-ad2c-217951bee9f6
ms.tgt_platform: multiple
keywords:
- Setstringarraydeploymentsetting-Methode Remotedesktopdienste
- Setstringarraydeploymentsetting-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, setstringarraydeploymentsetting-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetStringArrayDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb5ecc6d1238b739f8fe19d02e96ba427ed09b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743489"
---
# <a name="setstringarraydeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a>Setstringarraydeploymentsetting-Methode der Win32 \_ rdmsdeploymentsettings-Klasse

Aktualisiert die Bereitstellungs Einstellungen für eine Sammlung virtueller Desktops.

## <a name="syntax"></a>Syntax


```mof
uint32 SetStringArrayDeploymentSetting(
  [in] string Key,
  [in] string Value[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Der Alias der Sammlung virtueller Desktops.

</dd> <dt>

*Wert* \[ in\]
</dt> <dd>

Ein Array von Zeichen folgen, das die neuen Bereitstellungs Einstellungen enthält.

</dd> </dl>

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

 

 





