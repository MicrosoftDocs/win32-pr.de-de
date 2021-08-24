---
title: AddDesktopAssignment-Methode der Win32_RDMSDesktopAssignment-Klasse
description: Fügen Sie eine Desktopzuweisung hinzu.
ms.assetid: 3690f70e-d0c3-444a-a0b7-cec6994eb3b8
ms.tgt_platform: multiple
keywords:
- AddDesktopAssignment-Remotedesktopdienste
- AddDesktopAssignment-Methode Remotedesktopdienste , Win32_RDMSDesktopAssignment-Klasse
- Win32_RDMSDesktopAssignment klasse Remotedesktopdienste , AddDesktopAssignment-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.AddDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0d8145318cfd749772d2dcf417b71c6a1862ee31ec363957554e06b3aa6257
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868220"
---
# <a name="adddesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a>AddDesktopAssignment-Methode der Win32 \_ RDMSDesktopAssignment-Klasse

Hinzufügen einer Desktopzuweisung

## <a name="syntax"></a>Syntax


```mof
uint32 AddDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CollectionAlias* \[ In\]
</dt> <dd>

Der Auflistungsalias.

</dd> <dt>

*DesktopName* \[ In\]
</dt> <dd>

Der Name des Desktops.

</dd> <dt>

*UserDomain* \[ In\]
</dt> <dd>

Der Domänenname des Benutzerkontos.

</dd> <dt>

*UserName* \[ In\]
</dt> <dd>

Der Benutzername.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | Root \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ RDMSDesktopAssignment**](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





