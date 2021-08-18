---
title: FileAssociations-Methode der Win32_TSApplicationFileExtensions Klasse
description: Überprüft die Registrierung, um die aktuellen Dateizuordnungen für eine Anwendung zu erhalten.
ms.assetid: d2c55b59-f3aa-401b-b176-b287c2e26192
ms.tgt_platform: multiple
keywords:
- FileAssociations-Remotedesktopdienste
- FileAssociations-Methode Remotedesktopdienste , Win32_TSApplicationFileExtensions-Klasse
- Win32_TSApplicationFileExtensions klasse Remotedesktopdienste , FileAssociations-Methode
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
ms.openlocfilehash: a45548d055d6adc90ac55e26b646abab80470297847d5daa898e63b29769dc4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737510"
---
# <a name="fileassociations-method-of-the-win32_tsapplicationfileextensions-class"></a>FileAssociations-Methode der Win32 \_ TSApplicationFileExtensions-Klasse

Überprüft die Registrierung, um die aktuellen Dateizuordnungen für eine Anwendung zu erhalten.

## <a name="syntax"></a>Syntax


```mof
uint32 FileAssociations(
  [in]  string                  AppPath,
  [out] Win32_RDFileAssociation FileAssociations[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AppPath* \[ In\]
</dt> <dd>

Gibt den Pfad zur Anwendung an.

</dd> <dt>

*FileAssociations* \[ out\]
</dt> <dd>

Enthält nach erfolgreichem Abschluss die Dateizuordnungen für diese Anwendung.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TsAllow.mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSApplicationFileExtensions**](win32-tsapplicationfileextensions.md)
</dt> <dt>

[**Win32 \_ RDFileAssociation**](win32-rdfileassociation.md)
</dt> </dl>

 

 





