---
title: KeyValueCompareAndSet-Methode der Win32_RDSHCollection-Klasse
description: Vergleicht den angegebenen Schlüssel in der Auflistung mit einem compareand; Wenn sie übereinstimmen, wird der Schlüssel auf einen neuen Wert festgelegt. Wenn der Schlüssel nicht vorhanden ist, fügt die -Methode den Schlüssel in die Auflistung ein.
ms.assetid: ea6195b3-1a20-4d5b-b9a3-796976818b4f
ms.tgt_platform: multiple
keywords:
- KeyValueCompareAndSet-Methode Remotedesktopdienste
- KeyValueCompareAndSet-Methode Remotedesktopdienste , Win32_RDSHCollection-Klasse
- Win32_RDSHCollection-Klasse Remotedesktopdienste , KeyValueCompareAndSet-Methode
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
ms.openlocfilehash: 52e1aaaf90313c8c1434a65c4ffd1045933ad503245f0dacbf78c2b7e1ca054a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422710"
---
# <a name="keyvaluecompareandset-method-of-the-win32_rdshcollection-class"></a>KeyValueCompareAndSet-Methode der Win32 \_ RDSHCollection-Klasse

Vergleicht den angegebenen Schlüssel in der Auflistung mit einem compareand; Wenn sie übereinstimmen, wird der Schlüssel auf einen neuen Wert festgelegt. Wenn der Schlüssel nicht vorhanden ist, fügt die -Methode den Schlüssel in die Auflistung ein.

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

*Schlüssel* \[ In\]
</dt> <dd>

Der zu vergleichende Schlüssel.

</dd> <dt>

*NewValue* \[ In\]
</dt> <dd>

Der neue Wert.

</dd> <dt>

*Comparand* \[ In\]
</dt> <dd>

Die Zeichenfolge, mit der der Schlüssel verglichen werden soll.

</dd> <dt>

*InitialValue* \[ out\]
</dt> <dd>

Enthält bei Erfolg oder Fehler den Anfangswert des Schlüssels.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Beachten Sie, dass diese Methode den Wert des Schlüssels abrufen kann und daher die Funktionalität von [**KeyValueGet**](win32-rdshcollection-keyvalueget.md)kapselt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | Root \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**Win32 \_ RDSHCollection**](win32-rdshcollection.md)
</dt> </dl>

 

 





