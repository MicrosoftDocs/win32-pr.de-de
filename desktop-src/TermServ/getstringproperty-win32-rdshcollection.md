---
title: GetStringProperty-Methode der Win32_RDSHCollection-Klasse
description: Ruft einen Zeichenfolgeneigenschaftswert eines Win32 \_ RDSHCollection-Objekts ab.
ms.assetid: 8e97cd91-0e45-4d87-acfb-ee7d70376ce0
ms.tgt_platform: multiple
keywords:
- GetStringProperty-Methode Remotedesktopdienste
- GetStringProperty-Methode Remotedesktopdienste , Win32_RDSHCollection-Klasse
- Win32_RDSHCollection Klasse Remotedesktopdienste , GetStringProperty-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81aa383e339bda2620c4accf42f3cd810d867ae6f1e9c0d2716ed688583a1972
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771830"
---
# <a name="getstringproperty-method-of-the-win32_rdshcollection-class"></a>GetStringProperty-Methode der Win32 \_ RDSHCollection-Klasse

Ruft einen Zeichenfolgeneigenschaftswert eines [**Win32 \_ RDSHCollection-Objekts**](win32-rdshcollection.md) ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ In\]
</dt> <dd>

Der Schlüssel, der die abzurufende Eigenschaft identifiziert.

</dd> <dt>

*Wert* \[ out\]
</dt> <dd>

Empfängt den abgerufenen Eigenschaftswert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\Stamm-CIMv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ RDSHCollection**](win32-rdshcollection.md)
</dt> </dl>

 

 





