---
title: GetInt32Property-Methode der Win32_RDSHCollection-Klasse (Microsoft. Diagnostics. appanalysis. h)
description: Ruft einen ganzzahligen Eigenschafts Wert eines Win32- \_ rdshcollection-Objekts ab.
ms.assetid: ab68f357-057d-4a36-ae39-f47198768a49
ms.tgt_platform: multiple
keywords:
- GetInt32Property-Methode Remotedesktopdienste
- GetInt32Property-Methode Remotedesktopdienste, Win32_RDSHCollection-Klasse
- Win32_RDSHCollection-Klasse Remotedesktopdienste, GetInt32Property-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5cc29234fe3bb1b92e68e728423931da965391f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740408"
---
# <a name="getint32property-method-of-the-win32_rdshcollection-class"></a>GetInt32Property-Methode der Win32 \_ rdshcollection-Klasse

Ruft einen ganzzahligen Eigenschafts Wert eines [**Win32- \_ rdshcollection**](win32-rdshcollection.md) -Objekts ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Der Schlüssel, der die abzurufende Eigenschaft identifiziert.

</dd> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Empfängt den abgerufenen Eigenschafts Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                                 |
| Namespace<br/>                | Root \\ CIMv2 \\ RDMs<br/>                                                                                   |
| Header<br/>                   | <dl> <dt>Microsoft. Diagnostics. appanalysis. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ rdshcollection**](win32-rdshcollection.md)
</dt> </dl>

 

 





