---
title: GetInt32Property-Methode der Win32_RDSHCollection-Klasse (Microsoft.diagnostics.appanalysis.h)
description: Ruft einen ganzzahligen Eigenschaftswert eines Win32 \_ RDSHCollection-Objekts ab.
ms.assetid: ab68f357-057d-4a36-ae39-f47198768a49
ms.tgt_platform: multiple
keywords:
- GetInt32Property-Methode Remotedesktopdienste
- GetInt32Property-Methode Remotedesktopdienste , Win32_RDSHCollection-Klasse
- Win32_RDSHCollection-Klasse Remotedesktopdienste , GetInt32Property-Methode
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
ms.openlocfilehash: 61fb64c55a0b361ec4f3ca8528247f3884684b3321251c81594c3161c83a8c7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130715"
---
# <a name="getint32property-method-of-the-win32_rdshcollection-class"></a>GetInt32Property-Methode der Win32 \_ RDSHCollection-Klasse

Ruft einen ganzzahligen Eigenschaftswert eines [**Win32 \_ RDSHCollection-Objekts**](win32-rdshcollection.md) ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
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
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                                 |
| Namespace<br/>                | \\Stamm-CIMv2 \\ rdms<br/>                                                                                   |
| Header<br/>                   | <dl> <dt>Microsoft.diagnostics.appanalysis.h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ RDSHCollection**](win32-rdshcollection.md)
</dt> </dl>

 

 





