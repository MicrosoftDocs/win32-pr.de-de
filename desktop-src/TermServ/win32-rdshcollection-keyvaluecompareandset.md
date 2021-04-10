---
title: Keyvaluecompareandset-Methode der Win32_RDSHCollection-Klasse
description: Vergleicht den angegebenen Schlüssel in der Auflistung mit einem comparand. Stimmen Sie zu, wird der Schlüssel auf einen neuen Wert festgelegt. Wenn der Schlüssel nicht vorhanden ist, fügt die Methode den Schlüssel in die Auflistung ein.
ms.assetid: ea6195b3-1a20-4d5b-b9a3-796976818b4f
ms.tgt_platform: multiple
keywords:
- Keyvaluecompareandset-Methode Remotedesktopdienste
- Keyvaluecompareandset-Methode Remotedesktopdienste, Win32_RDSHCollection-Klasse
- Win32_RDSHCollection-Klasse Remotedesktopdienste, keyvaluecompareandset-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueCompareAndSet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b90d703b40cf76f59cc3caf5d8f197f387cfe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858805"
---
# <a name="keyvaluecompareandset-method-of-the-win32_rdshcollection-class"></a>Keyvaluecompareandset-Methode der Win32 \_ rdshcollection-Klasse

Vergleicht den angegebenen Schlüssel in der Auflistung mit einem comparand. Stimmen Sie zu, wird der Schlüssel auf einen neuen Wert festgelegt. Wenn der Schlüssel nicht vorhanden ist, fügt die Methode den Schlüssel in die Auflistung ein.

## <a name="syntax"></a>Syntax


```mof
uint32 KeyValueCompareAndSet(
  [in]  string Key,
  [in]  string NewValue,
  [in]  string Comparand,
  [out] string InitialValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Der zu vergleichende Schlüssel.

</dd> <dt>

*NewValue* \[ in\]
</dt> <dd>

Der neue Wert.

</dd> <dt>

*Comparand* \[ in\]
</dt> <dd>

Die Zeichenfolge, mit der der Schlüssel verglichen werden soll.

</dd> <dt>

*InitialValue* \[ vorgenommen\]
</dt> <dd>

Bei Erfolg oder Fehler enthält den Anfangswert des Schlüssels.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass diese Methode den Wert des Schlüssels abrufen kann und damit die Funktionalität von [**keyvalueget**](win32-rdshcollection-keyvalueget.md)kapselt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | Root \\ CIMV2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ rdshcollection**](win32-rdshcollection.md)
</dt> </dl>

 

 





