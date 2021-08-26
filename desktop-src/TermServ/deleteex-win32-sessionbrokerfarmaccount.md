---
title: DeleteEx-Methode der Win32_SessionBrokerFarmAccount Klasse
description: Die Win32 \_ SessionBrokerFarmAccount-Klasse ist ab diesem Windows Server 2012. | DeleteEx-Methode der Win32_SessionBrokerFarmAccount Klasse
ms.assetid: d30c5d3e-f63c-4b21-85ae-a0b8d5868d64
ms.tgt_platform: multiple
keywords:
- DeleteEx-Remotedesktopdienste
- DeleteEx-methode Remotedesktopdienste , Win32_SessionBrokerFarmAccount-Klasse
- Win32_SessionBrokerFarmAccount klasse Remotedesktopdienste , DeleteEx-Methode
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
ms.openlocfilehash: aa891c874c9592ed11b2aa0840913e67daa7226a93f6f746cf74c45a0454a476
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080220"
---
# <a name="deleteex-method-of-the-win32_sessionbrokerfarmaccount-class"></a>DeleteEx-Methode der Win32 \_ SessionBrokerFarmAccount-Klasse

\[Die [**Win32 \_ SessionBrokerFarmAccount-Klasse**](win32-sessionbrokerfarmaccount.md) ist ab diesem Windows Server 2012.\]

Löscht das Farmkonto.

## <a name="syntax"></a>Syntax


```mof
uint32 DeleteEx(
  [in] boolean DeleteComputerObject
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DeleteComputerObject* \[ In\]
</dt> <dd>

Gibt an, ob das der Farm zugeordnete Computerobjekt aus Active Directory entfernt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Remotedesktopdienste finden Sie unter [Fehlercodes](terminal-services-wmi-provider-error-codes.md) für WMI-Anbieter.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                      |
| Ende des Supports (Client)<br/>    | Nicht unterstützt<br/>                                                              |
| Ende des Supports (Server)<br/>    | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ SessionBrokerFarmAccount**](win32-sessionbrokerfarmaccount.md)
</dt> </dl>

 

 





