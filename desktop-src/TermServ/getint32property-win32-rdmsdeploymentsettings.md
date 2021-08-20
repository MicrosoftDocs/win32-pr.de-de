---
title: GetInt32Property-Methode der Win32_RDMSDeploymentSettings -Klasse (Microsoft.diagnostics.appanalysis.h)
description: Ruft eine ganzzahlige Eigenschaft für die Bereitstellungseinstellungen einer Sammlung virtueller Desktops ab.
ms.assetid: 6b8174bb-ffb7-4699-a3fb-d32ab0b202fc
ms.tgt_platform: multiple
keywords:
- GetInt32Property-Remotedesktopdienste
- GetInt32Property-Methode Remotedesktopdienste , Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings klasse Remotedesktopdienste , GetInt32Property-Methode
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
ms.openlocfilehash: 1ac79fdacf6b8f64d354158f964be1019692933a10409a8bf085109d9f5a9a31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130759"
---
# <a name="getint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a>GetInt32Property-Methode der Win32 \_ RDMSDeploymentSettings-Klasse

Ruft eine ganzzahlige Eigenschaft für die Bereitstellungseinstellungen einer Sammlung virtueller Desktops ab.

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

Der Alias für die Sammlung virtueller Desktops.

</dd> <dt>

*Wert* \[ out\]
</dt> <dd>

Eine ganze Zahl, die den abgerufenen Wert empfängt.

</dd> </dl>

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

[**Win32 \_ RDMSDeploymentSettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





