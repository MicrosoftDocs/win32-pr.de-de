---
title: SetSecondaryConnectionString-Methode der Win32_RDMSDeploymentSettings Klasse
description: Legt die sekundäre Verbindungszeichenfolge der Datenbank auf Bereitstellungsebene fest.
ms.assetid: 154c495e-564e-4d90-a4ff-de683d41aa73
ms.tgt_platform: multiple
keywords:
- SetSecondaryConnectionString-Remotedesktopdienste
- SetSecondaryConnectionString-Methode Remotedesktopdienste , Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings der Remotedesktopdienste , SetSecondaryConnectionString-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetSecondaryConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeb43f0317f4a31733cf0c0f7b5b578234e14b50dc8976df096e5b9b0b3426d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868250"
---
# <a name="setsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a>SetSecondaryConnectionString-Methode der Win32 \_ RDMSDeploymentSettings-Klasse

Legt die sekundäre Verbindungszeichenfolge der Datenbank auf Bereitstellungsebene fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetSecondaryConnectionString(
  [in] string SecondaryConnectionString
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SecondaryConnectionString* \[ In\]
</dt> <dd>

Die verbindungszeichenfolge, die festgelegt werden soll

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | Root \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ RDMSDeploymentSettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





