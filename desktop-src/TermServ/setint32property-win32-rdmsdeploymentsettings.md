---
title: SetInt32Property-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Aktualisiert eine ganzzahlige Eigenschaft für die Bereitstellungseinstellungen einer Sammlung virtueller Desktops.
ms.assetid: c5e6dbd5-7db7-4409-bf53-c2680e4a5319
ms.tgt_platform: multiple
keywords:
- SetInt32Property-Methode Remotedesktopdienste
- SetInt32Property-Methode Remotedesktopdienste , Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste , SetInt32Property-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73fa8f9ad7560e4d0eeeb8708feb547da00a8e9804e242ceb94666da211b03a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865380"
---
# <a name="setint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a>SetInt32Property-Methode der Win32 \_ RDMSDeploymentSettings-Klasse

Aktualisiert eine ganzzahlige Eigenschaft für die Bereitstellungseinstellungen einer Sammlung virtueller Desktops.

## <a name="syntax"></a>Syntax


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ In\]
</dt> <dd>

Der Alias für die Sammlung virtueller Desktops.

</dd> <dt>

*Wert* \[ In\]
</dt> <dd>

Der neue Eigenschaftswert.

</dd> </dl>

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

 

 





