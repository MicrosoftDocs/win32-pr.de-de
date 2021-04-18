---
title: Die Methode "stexportpath" der Win32_RDMSDeploymentSettings-Klasse
description: Aktualisiert den Verzeichnispfad, in dem virtuelle Maschinen für eine Sammlung virtueller Desktops bereitgestellt werden.
ms.assetid: e52b79c8-6724-4264-93d5-4a2a14c89b6b
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "stexportpath"
- Methode Remotedesktopdienste der Methode "Win32_RDMSDeploymentSettings"
- Win32_RDMSDeploymentSettings-Klasse Remotedesktopdienste, Methode "abtexportpath"
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetExportPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32dbc844aecf86d4c62fada6c5cd68d514a69272
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340581"
---
# <a name="setexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Die Methode "stexportpath" der Win32- \_ Klasse "rdmsdeploymentsettings"

Aktualisiert den Verzeichnispfad, in dem virtuelle Maschinen für eine Sammlung virtueller Desktops bereitgestellt werden.

## <a name="syntax"></a>Syntax


```mof
uint32 SetExportPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Directoriypath* \[ in\]
</dt> <dd>

Der neue Verzeichnispfad.

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

 

 





