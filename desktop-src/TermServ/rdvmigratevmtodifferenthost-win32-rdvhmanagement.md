---
title: RdvMigrateVmToDifferentHost-Methode der Win32_RdvhManagement Klasse
description: Initiiert eine Livemigration eines virtuellen Computers zu einem angegebenen Host.
ms.assetid: aa4b1e57-a97c-410b-9b9d-423a1c77de70
ms.tgt_platform: multiple
keywords:
- RdvMigrateVmToDifferentHost-Remotedesktopdienste
- RdvMigrateVmToDifferentHost-Methode Remotedesktopdienste , Win32_RdvhManagement-Klasse
- Win32_RdvhManagement klasse Remotedesktopdienste , RdvMigrateVmToDifferentHost-Methode
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvMigrateVmToDifferentHost
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a84171bc6db6a39cff5a2d55ca7e453bf9b963636ea765480fe87b16fd8da92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756242"
---
# <a name="rdvmigratevmtodifferenthost-method-of-the-win32_rdvhmanagement-class"></a>RdvMigrateVmToDifferentHost-Methode der Win32 \_ RdvhManagement-Klasse

Initiiert eine Livemigration eines virtuellen Computers zu einem angegebenen Host.

## <a name="syntax"></a>Syntax


```mof
uint32 RdvMigrateVmToDifferentHost(
  [in] string VmName,
  [in] string DestinationHost
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VmName* \[ In\]
</dt> <dd>

Name des zu migrierenden virtuellen Computers.

</dd> <dt>

*DestinationHost* \[ In\]
</dt> <dd>

Name des Zielhosts.

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

 

 





