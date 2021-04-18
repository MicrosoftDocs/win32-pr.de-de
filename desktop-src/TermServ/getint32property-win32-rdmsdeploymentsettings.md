---
title: GetInt32Property-Methode der Win32_RDMSDeploymentSettings-Klasse (Microsoft. Diagnostics. appanalysis. h)
description: Ruft eine ganzzahlige Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops ab.
ms.assetid: 6b8174bb-ffb7-4699-a3fb-d32ab0b202fc
ms.tgt_platform: multiple
keywords:
- GetInt32Property-Methode Remotedesktopdienste
- GetInt32Property-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, GetInt32Property-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f96374c610084c8ef7973d4ac4db603d9c28cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344070"
---
# <a name="getint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a>GetInt32Property-Methode der Win32 \_ rdmsdeploymentsettings-Klasse

Ruft eine ganzzahlige Eigenschaft für die Bereitstellungs Einstellungen einer Sammlung virtueller Desktops ab.

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

Der Alias für die Sammlung virtueller Desktops.

</dd> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Eine ganze Zahl, die den abgerufenen Wert empfängt.

</dd> </dl>

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

[**Win32 \_ rdmsdeploymentsettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





