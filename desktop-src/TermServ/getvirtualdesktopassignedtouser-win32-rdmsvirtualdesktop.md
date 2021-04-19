---
title: Getvirtualdesktopassignetdtouser-Methode der Win32_RDMSVirtualDesktop-Klasse
description: Ruft den virtuellen Desktop ab, der dem angegebenen Benutzer zugewiesen ist.
ms.assetid: cbc22c45-4492-4651-b164-a6fd717c5ab4
ms.tgt_platform: multiple
keywords:
- Getvirtualdesktopassignetdtouser-Methode Remotedesktopdienste
- Getvirtualdesktopassignetdtouser-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktop-Klasse
- Win32_RDMSVirtualDesktop-Klasse Remotedesktopdienste, getvirtualdesktopassignetdtouser-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopAssignedToUser
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcbbbed20b6b571e8867689ac901344af8e23b93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339540"
---
# <a name="getvirtualdesktopassignedtouser-method-of-the-win32_rdmsvirtualdesktop-class"></a>Getvirtualdesktopassignetdtouser-Methode der Win32 \_ rdmsvirtualdesktop-Klasse

Ruft den virtuellen Desktop ab, der dem angegebenen Benutzer zugewiesen ist.

## <a name="syntax"></a>Syntax


```mof
uint32 GetVirtualDesktopAssignedToUser(
  [in]  string CollectionAlias,
  [in]  string UserName,
  [in]  string UserDomain,
  [out] string VMName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Collectionalias* \[ in\]
</dt> <dd>

Der Alias der Sammlung virtueller Desktops, die den virtuellen Desktop enthält.

</dd> <dt>

*Benutzername* \[ in\]
</dt> <dd>

Der Benutzername des Benutzers.

</dd> <dt>

*Benutzer Domäne* \[ in\]
</dt> <dd>

Der Domänen Name des Benutzers.

</dd> <dt>

*VMName* \[ vorgenommen\]
</dt> <dd>

Empfängt den Namen des virtuellen Computers des virtuellen Desktops.

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

[**Win32 \_ rdmsvirtualdesktop**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





