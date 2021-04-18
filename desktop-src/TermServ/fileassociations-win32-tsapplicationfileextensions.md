---
title: Fileassociations-Methode der Win32_TSApplicationFileExtensions-Klasse
description: Scannt die Registrierung, um die aktuellen Dateizuordnungen für eine Anwendung zu erhalten.
ms.assetid: d2c55b59-f3aa-401b-b176-b287c2e26192
ms.tgt_platform: multiple
keywords:
- Fileassociations-Methode Remotedesktopdienste
- Fileassociations-Methode Remotedesktopdienste, Win32_TSApplicationFileExtensions-Klasse
- Win32_TSApplicationFileExtensions-Klasse Remotedesktopdienste, fileassociations-Methode
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileAssociations
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ee60033344c0c448d82680bdcacfc24cb4f214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340005"
---
# <a name="fileassociations-method-of-the-win32_tsapplicationfileextensions-class"></a>Filezuzuordnungen-Methode der Win32-Klasse "-Klasse". \_

Scannt die Registrierung, um die aktuellen Dateizuordnungen für eine Anwendung zu erhalten.

## <a name="syntax"></a>Syntax


```mof
uint32 FileAssociations(
  [in]  string                  AppPath,
  [out] Win32_RDFileAssociation FileAssociations[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Apppath* \[ in\]
</dt> <dd>

Gibt den Pfad zur Anwendung an.

</dd> <dt>

*Dateizuordnungen* \[ vorgenommen\]
</dt> <dd>

Nach erfolgreichem Abschluss enthält die Dateizuordnungen für diese Anwendung.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow. MOF</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ applicationfileextensions**](win32-tsapplicationfileextensions.md)
</dt> <dt>

[**Win32 \_ rdfileassociation**](win32-rdfileassociation.md)
</dt> </dl>

 

 





