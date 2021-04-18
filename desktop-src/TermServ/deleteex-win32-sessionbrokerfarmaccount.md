---
title: DeleteEx-Methode der Win32_SessionBrokerFarmAccount-Klasse
description: Die Win32- \_ Klasse "sessionbrokerfarmaccount" ist nicht mehr für die Verwendung ab Windows Server 2012 verfügbar. | DeleteEx-Methode der Win32_SessionBrokerFarmAccount-Klasse
ms.assetid: d30c5d3e-f63c-4b21-85ae-a0b8d5868d64
ms.tgt_platform: multiple
keywords:
- DeleteEx-Methode Remotedesktopdienste
- DeleteEx-Methode Remotedesktopdienste, Win32_SessionBrokerFarmAccount-Klasse
- Win32_SessionBrokerFarmAccount-Klasse Remotedesktopdienste, DeleteEx-Methode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount.DeleteEx
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdad7b1c7af85337ace59690bb44f4309254eb76
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354936"
---
# <a name="deleteex-method-of-the-win32_sessionbrokerfarmaccount-class"></a>DeleteEx-Methode der Win32- \_ Klasse "sessionbrokerfarmaccount"

\[Die Win32-Klasse " [**\_ sessionbrokerfarmaccount**](win32-sessionbrokerfarmaccount.md) " ist nicht mehr für die Verwendung ab Windows Server 2012 verfügbar.\]

Löscht das Farmkonto.

## <a name="syntax"></a>Syntax


```mof
uint32 DeleteEx(
  [in] boolean DeleteComputerObject
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Deletecomputerobject* \[ in\]
</dt> <dd>

Gibt an, ob das der Farm zugeordnete Computer Objekt aus Active Directory entfernt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                      |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                              |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>"Tssdwmi. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ sessionbrokerfarmaccount**](win32-sessionbrokerfarmaccount.md)
</dt> </dl>

 

 





