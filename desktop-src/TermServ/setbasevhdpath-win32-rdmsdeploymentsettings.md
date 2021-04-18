---
title: Setbasevhdpath-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Ruft den Basispfad zu dem Verzeichnis ab, in dem die VHDs der virtuellen Desktop Sammlung bereitgestellt werden. | Setbasevhdpath-Methode der Win32_RDMSDeploymentSettings-Klasse
ms.assetid: 1ea4cd93-ef17-4ec9-82f9-382c549f189c
ms.tgt_platform: multiple
keywords:
- Setbasevhdpath-Methode Remotedesktopdienste
- Setbasevhdpath-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, setbasevhdpath-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7907640a9641cff3c94475318bf499415b25184
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354299"
---
# <a name="setbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Setbasevhdpath-Methode der Win32 \_ rdmsdeploymentsettings-Klasse

Ruft den Basispfad zu dem Verzeichnis ab, in dem die VHDs der virtuellen Desktop Sammlung bereitgestellt werden.

## <a name="syntax"></a>Syntax


```mof
uint32 SetBaseVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Directoriypath* \[ in\]
</dt> <dd>

Der neue VHD-Bereitstellungs Pfad.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | Root \\ CIMv2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ rdmsdeploymentsettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





