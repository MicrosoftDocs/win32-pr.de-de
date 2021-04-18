---
title: Getexportpath-Methode der Win32_RDMSDeploymentSettings-Klasse
description: Ruft den Verzeichnispfad ab, in dem virtuelle Maschinen für eine Sammlung virtueller Desktops bereitgestellt werden.
ms.assetid: 8df79e31-b960-46ae-b49c-8052b356e1a8
ms.tgt_platform: multiple
keywords:
- Getexportpath-Methode Remotedesktopdienste
- Getexportpath-Methode Remotedesktopdienste, Win32_RDMSDeploymentSettings-Klasse
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, getexportpath-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetExportPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baf96d1d71554f1b8ea310759d36d0918a511cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340565"
---
# <a name="getexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Getexportpath-Methode der Win32 \_ rdmsdeploymentsettings-Klasse

Ruft den Verzeichnispfad ab, in dem virtuelle Maschinen für eine Sammlung virtueller Desktops bereitgestellt werden.

## <a name="syntax"></a>Syntax


```mof
uint32 GetExportPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Directoriypath* \[ vorgenommen\]
</dt> <dd>

Empfängt den Verzeichnispfad.

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

 

 





