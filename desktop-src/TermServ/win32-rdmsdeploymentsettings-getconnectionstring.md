---
title: GetConnectionString-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Ruft die Datenbank-Verbindungs Zeichenfolge auf Bereitstellungs Ebene ab.
ms.assetid: 91a90883-9b87-42e5-af52-90226f0344bf
ms.tgt_platform: multiple
keywords:
- GetConnectionString-Methode Remotedesktopdienste
- GetConnectionString-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, GetConnectionString-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6476c938f62e0cd0e1f9d034c89fded50994946
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477082"
---
# <a name="getconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a>GetConnectionString-Methode der Win32 \_ rdmsdeploymentsettings-Klasse

Ruft die Datenbank-Verbindungs Zeichenfolge auf Bereitstellungs Ebene ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetConnectionString(
  [out] string ConnectionString
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ConnectionString* \[ vorgenommen\]
</dt> <dd>

Die Verbindungs Zeichenfolge

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

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

[**Win32 \_ rdmsdeploymentsettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





