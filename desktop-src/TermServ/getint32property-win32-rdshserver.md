---
title: GetInt32Property-Methode der Win32_RDSHServer -Klasse (Microsoft.diagnostics.appanalysis.h)
description: Ruft einen ganzzahligen Eigenschaftswert eines Win32 \_ RDSHServer-Objekts ab.
ms.assetid: 4601e9cb-927b-4af8-a12b-09a8ca44c2f7
ms.tgt_platform: multiple
keywords:
- GetInt32Property-Remotedesktopdienste
- GetInt32Property-Methode Remotedesktopdienste , Win32_RDSHServer-Klasse
- Win32_RDSHServer klasse Remotedesktopdienste , GetInt32Property-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba9114ca22a1052161000fcb05f38622ab9d210ec02b14715dad1bb85ce1365e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130671"
---
# <a name="getint32property-method-of-the-win32_rdshserver-class"></a>GetInt32Property-Methode der Win32 \_ RDSHServer-Klasse

Ruft einen ganzzahligen Eigenschaftswert eines [**Win32 \_ RDSHServer-Objekts**](win32-rdshserver.md) ab.

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

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                                 |
| Namespace<br/>                | \\Stamm-CIMv2-Rdms \\<br/>                                                                                   |
| Header<br/>                   | <dl> <dt>Microsoft.diagnostics.appanalysis.h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ RDSHServer**](win32-rdshserver.md)
</dt> </dl>

 

 





