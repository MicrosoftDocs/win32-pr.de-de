---
title: Getsecondaryconnectionstring-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Ruft die sekundäre Daten bankverbindungs Zeichenfolge auf Bereitstellungs Ebene ab, die zur Unterstützung des Kenn Wort Ablaufs verwendet werden kann.
ms.assetid: 0de02752-6cbf-4c21-b752-a57ed58aeef1
ms.tgt_platform: multiple
keywords:
- Getsecondaryconnectionstring-Methode Remotedesktopdienste
- Getsecondaryconnectionstring-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, getsecondaryconnectionstring-Methode
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
ms.openlocfilehash: d2c09f4fcacabbe928fcda00447e252077bd8a51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340638"
---
# <a name="getsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a>Getsecondaryconnectionstring-Methode der Win32 \_ rdmsdeploymentsettings-Klasse

Ruft die sekundäre Daten bankverbindungs Zeichenfolge auf Bereitstellungs Ebene ab, die zur Unterstützung des Kenn Wort Ablaufs verwendet werden kann.

## <a name="syntax"></a>Syntax


```mof
uint32 GetSecondaryConnectionString(
  [out] string SecondaryConnectionString
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Secondaryconnectionstring* \[ vorgenommen\]
</dt> <dd>

Abzurufende Verbindungs Zeichenfolge

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

 

 





