---
title: GetSecondaryConnectionString-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Ruft die sekundäre Verbindungszeichenfolge der Datenbank auf Bereitstellungsebene ab, die zur Unterstützung des Kennwortablaufs verwendet werden kann.
ms.assetid: 0de02752-6cbf-4c21-b752-a57ed58aeef1
ms.tgt_platform: multiple
keywords:
- GetSecondaryConnectionString-Methode Remotedesktopdienste
- GetSecondaryConnectionString-Methode Remotedesktopdienste , Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings klasse Remotedesktopdienste , GetSecondaryConnectionString-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSecondaryConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac54d0d5ce9207070d03028ba53175d964e93d77a93d51b28345089fcea99dcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868310"
---
# <a name="getsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a>GetSecondaryConnectionString-Methode der Win32 \_ RDMSDeploymentSettings-Klasse

Ruft die sekundäre Verbindungszeichenfolge der Datenbank auf Bereitstellungsebene ab, die zur Unterstützung des Kennwortablaufs verwendet werden kann.

## <a name="syntax"></a>Syntax


```mof
uint32 GetSecondaryConnectionString(
  [out] string SecondaryConnectionString
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SecondaryConnectionString* \[ out\]
</dt> <dd>

Die abzurufende Verbindungszeichenfolge

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

 

 





