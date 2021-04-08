---
title: SetInt32Property-Methode der Win32_RDSHServer-Klasse
description: Aktualisiert einen ganzzahligen Eigenschafts Wert eines Win32- \_ rdshserver-Objekts.
ms.assetid: fa8df023-120d-4174-adc1-868f08fdce56
ms.tgt_platform: multiple
keywords:
- SetInt32Property-Methode Remotedesktopdienste
- SetInt32Property-Methode Remotedesktopdienste, Win32_RDSHServer-Klasse
- Win32_RDSHServer-Klasse Remotedesktopdienste, SetInt32Property-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHServer.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66c22c8da9c046e0a42a6ec41f6ad5b3073c8d1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741297"
---
# <a name="setint32property-method-of-the-win32_rdshserver-class"></a>SetInt32Property-Methode der Win32 \_ rdshserver-Klasse

Aktualisiert einen ganzzahligen Eigenschafts Wert eines [**Win32- \_ rdshserver**](win32-rdshserver.md) -Objekts.

## <a name="syntax"></a>Syntax


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Der Schlüssel, der die zu Aktualisier enswerte Eigenschaft identifiziert.

</dd> <dt>

*Wert* \[ in\]
</dt> <dd>

Der neue Eigenschaftswert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

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

[**Win32- \_ rdshserver**](win32-rdshserver.md)
</dt> </dl>

 

 





