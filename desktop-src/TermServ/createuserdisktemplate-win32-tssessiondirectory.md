---
title: Methode "kreateuserdisktemplate" der Win32_TSSessionDirectory-Klasse
description: Erstellt eine Vorlage für Benutzer Datenträger.
ms.assetid: 4036a418-b082-4376-a400-16f48b98f071
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "kreateuserdisktemplate"
- Methode Remotedesktopdienste der Methode "kreateuserdisktemplate", Win32_TSSessionDirectory Klasse
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste, Methode "kreateuserdisktemplate"
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.CreateUserDiskTemplate
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c142834b4501639499cd0bcf102dadcc1b07d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103098"
---
# <a name="createuserdisktemplate-method-of-the-win32_tssessiondirectory-class"></a>Methode "| ateuserdisktemplate" der Win32- \_ Klasse "tssessiondirectory"

Erstellt eine Vorlage für Benutzer Datenträger.

## <a name="syntax"></a>Syntax


```mof
uint32 CreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Userdisksstorageurl* \[ in\]
</dt> <dd>

Der Speicherort der Freigabe, auf der alle Benutzer Datenträger gespeichert werden.

</dd> <dt>

*Userdiskmaxsizzugb* \[ in\]
</dt> <dd>

Die maximale Größe in Gigabyte für alle Benutzer Datenträger.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ tssessiondirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

 





