---
title: Rdvundovmberechtigungs-Methode der Win32_RdvhManagement-Klasse
description: Stellt die von rdvsetupvm-Berechtigungen festgelegten Berechtigungen auf dem angegebenen virtuellen Computer wieder her.
ms.assetid: 3331430e-7427-42f7-ab09-27fece8dc3ca
ms.tgt_platform: multiple
keywords:
- Rdvundovmberechtigungen-Methode Remotedesktopdienste
- Rdvundovmberechtigungs Methode Remotedesktopdienste, Win32_RdvhManagement-Klasse
- Win32_RdvhManagement-Klasse Remotedesktopdienste, rdvundovmberechtigungs Methode
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
ms.openlocfilehash: 7d1dc8892435522dcd2c7457fe4b74a0d9671740
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478867"
---
# <a name="rdvundovmpermissions-method-of-the-win32_rdvhmanagement-class"></a>Rdvundovmberechtigungs-Methode der Win32 \_ rdvhmanagement-Klasse

Stellt die von [**rdvsetupvm-Berechtigungen**](rdvsetupvmpermissions-win32-rdvhmanagement.md) festgelegten Berechtigungen auf dem angegebenen virtuellen Computer wieder her.

## <a name="syntax"></a>Syntax


```mof
uint32 RdvUndoVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VMName* \[ in\]
</dt> <dd>

Der Name des virtuellen Computers, für den Berechtigungen rückgängig gemacht werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>"Zvmhost. mof"</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ rdvhmanagement**](win32-rdvhmanagement.md)
</dt> </dl>

 

 





