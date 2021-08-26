---
title: SetStringProperty-Methode der Win32_RDSHCollection -Klasse (Certenroll.h)
description: Aktualisiert einen Zeichenfolgeneigenschaftswert eines Win32 \_ RDSHCollection-Objekts.
ms.assetid: 6981b47a-5480-44f5-90e3-f64d439fa2aa
ms.tgt_platform: multiple
keywords:
- SetStringProperty-Remotedesktopdienste
- SetStringProperty-Methode Remotedesktopdienste , Win32_RDSHCollection-Klasse
- Win32_RDSHCollection klasse Remotedesktopdienste , SetStringProperty-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87556f82f4004b6c7dbf194dfe38f47804d1fa07747ccb7e18d2b24a4a70f355
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987490"
---
# <a name="setstringproperty-method-of-the-win32_rdshcollection-class"></a>SetStringProperty-Methode der Win32 \_ RDSHCollection-Klasse

Aktualisiert einen Zeichenfolgeneigenschaftswert eines [**Win32 \_ RDSHCollection-Objekts.**](win32-rdshcollection.md)

## <a name="syntax"></a>Syntax


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ In\]
</dt> <dd>

Der Schlüssel, der die zu aktualisierende Eigenschaft identifiziert.

</dd> <dt>

*Wert* \[ In\]
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
| Namespace<br/>                | \\Stamm-CIMv2-Rdms \\<br/>                                                                |
| Header<br/>                   | <dl> <dt>Certenroll.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ RDSHCollection**](win32-rdshcollection.md)
</dt> </dl>

 

 





