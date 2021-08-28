---
title: GetVirtualDesktopAssignedToUser-Methode der Win32_RDMSVirtualDesktop-Klasse
description: Ruft den virtuellen Desktop ab, der dem angegebenen Benutzer zugewiesen ist.
ms.assetid: cbc22c45-4492-4651-b164-a6fd717c5ab4
ms.tgt_platform: multiple
keywords:
- GetVirtualDesktopAssignedToUser-Methode Remotedesktopdienste
- GetVirtualDesktopAssignedToUser-Methode Remotedesktopdienste , Win32_RDMSVirtualDesktop-Klasse
- Win32_RDMSVirtualDesktop Klasse Remotedesktopdienste , GetVirtualDesktopAssignedToUser-Methode
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
ms.openlocfilehash: fce30afea4a95ed462bfb1b456788fa54f045097c16c3d65070cdb343e928237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059548"
---
# <a name="getvirtualdesktopassignedtouser-method-of-the-win32_rdmsvirtualdesktop-class"></a>GetVirtualDesktopAssignedToUser-Methode der Win32 \_ RDMSVirtualDesktop-Klasse

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

*CollectionAlias* \[ In\]
</dt> <dd>

Der Alias der Sammlung virtueller Desktops, die den virtuellen Desktop enthalten.

</dd> <dt>

*UserName* \[ In\]
</dt> <dd>

Der Benutzername des Benutzers.

</dd> <dt>

*UserDomain* \[ In\]
</dt> <dd>

Der Domänenname des Benutzers.

</dd> <dt>

*VMName* \[ out\]
</dt> <dd>

Empfängt den Namen des virtuellen Computers des virtuellen Desktops.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\Stamm-CIMv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktop**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





