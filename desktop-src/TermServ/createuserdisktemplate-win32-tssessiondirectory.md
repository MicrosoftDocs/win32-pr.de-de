---
title: CreateUserDiskTemplate-Methode der Win32_TSSessionDirectory Klasse
description: Erstellt eine Benutzerdatenträgervorlage.
ms.assetid: 4036a418-b082-4376-a400-16f48b98f071
ms.tgt_platform: multiple
keywords:
- CreateUserDiskTemplate-Remotedesktopdienste
- CreateUserDiskTemplate-Methode Remotedesktopdienste , Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory klasse Remotedesktopdienste , CreateUserDiskTemplate-Methode
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
ms.openlocfilehash: cdc16d293f901efb6fc684d03ec7b47aa7496120c462a32414c747d15c02810a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010230"
---
# <a name="createuserdisktemplate-method-of-the-win32_tssessiondirectory-class"></a>CreateUserDiskTemplate-Methode der Win32 \_ TSSessionDirectory-Klasse

Erstellt eine Benutzerdatenträgervorlage.

## <a name="syntax"></a>Syntax


```mof
uint32 CreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*UserDisksStorageUrl* \[ In\]
</dt> <dd>

Der Speicherort der Freigabe, in der alle Benutzerdatenträger gespeichert werden.

</dd> <dt>

*UserDiskMaxSizeInGB* \[ In\]
</dt> <dd>

Die maximale Größe in Gigabyte für alle Benutzerdatenträger.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

 





