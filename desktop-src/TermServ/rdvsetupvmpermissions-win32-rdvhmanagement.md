---
title: RdvSetupVMPermissions-Methode der Win32_RdvhManagement-Klasse
description: Legt die Berechtigungen für einen virtuellen Computer für den aktuellen Benutzer fest.
ms.assetid: 6ac45983-d468-4a3b-875f-48717ba23ed0
ms.tgt_platform: multiple
keywords:
- RdvSetupVMPermissions-Remotedesktopdienste
- RdvSetupVMPermissions-Methode Remotedesktopdienste , Win32_RdvhManagement-Klasse
- Win32_RdvhManagement klasse Remotedesktopdienste , RdvSetupVMPermissions-Methode
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvSetupVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6628e3ac1660c1f0c505e3d5349dd481c7c48b09a77aaedeac1352ecbaf4562
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988810"
---
# <a name="rdvsetupvmpermissions-method-of-the-win32_rdvhmanagement-class"></a>RdvSetupVMPermissions-Methode der Win32 \_ RdvhManagement-Klasse

Legt die Berechtigungen für einen virtuellen Computer für den aktuellen Benutzer fest.

## <a name="syntax"></a>Syntax


```mof
uint32 RdvSetupVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VmName* \[ In\]
</dt> <dd>

Der Name des virtuellen Computers, für den Berechtigungen festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Remotedesktopdienste finden Sie unter [Fehlercodes](terminal-services-wmi-provider-error-codes.md) für WMI-Anbieter.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ RdvhManagement**](win32-rdvhmanagement.md)
</dt> </dl>

 

 





