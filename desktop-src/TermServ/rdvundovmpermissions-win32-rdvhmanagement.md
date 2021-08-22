---
title: RdvUndoVMPermissions-Methode der Win32_RdvhManagement-Klasse
description: Setzt die von RdvSetupVMPermissions festgelegten Berechtigungen auf dem angegebenen virtuellen Computer zurück.
ms.assetid: 3331430e-7427-42f7-ab09-27fece8dc3ca
ms.tgt_platform: multiple
keywords:
- RdvUndoVMPermissions-Methode Remotedesktopdienste
- RdvUndoVMPermissions-Methode Remotedesktopdienste , Win32_RdvhManagement-Klasse
- Win32_RdvhManagement-Klasse Remotedesktopdienste , RdvUndoVMPermissions-Methode
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvUndoVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6826fdfef6d3c6b6f043c59f7d08a7cf23ab8bef64f12c72cd70eea84b6b998a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118852191"
---
# <a name="rdvundovmpermissions-method-of-the-win32_rdvhmanagement-class"></a>RdvUndoVMPermissions-Methode der Win32 \_ RdvhManagement-Klasse

Setzt die von [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md) festgelegten Berechtigungen auf dem angegebenen virtuellen Computer zurück.

## <a name="syntax"></a>Syntax


```mof
uint32 RdvUndoVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VmName* \[ In\]
</dt> <dd>

Name des virtuellen Computers, für den Berechtigungen rückgängig machen werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ RdvhManagement**](win32-rdvhmanagement.md)
</dt> </dl>

 

 





