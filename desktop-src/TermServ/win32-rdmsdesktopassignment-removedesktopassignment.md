---
title: Removedesktopzuweisung-Methode der Win32_RDMSDesktopAssignment-Klasse
description: Entfernt eine Desktop Zuweisung.
ms.assetid: e1a8cf03-1d21-4bf4-a868-3da4d5bbf43b
ms.tgt_platform: multiple
keywords:
- Removedesktopzuweisung-Methode Remotedesktopdienste
- Removedesktopzuweisung-Methode Remotedesktopdienste, Win32_RDMSDesktopAssignment-Klasse
- Win32_RDMSDesktopAssignment-Klasse Remotedesktopdienste, removedesktopzuweisungs-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.RemoveDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6645a79efc970cf7c3288d0765e9aac8cac68a89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344503"
---
# <a name="removedesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a>Removedesktopzuweisung-Methode der Win32- \_ Klasse rdmsdesktopzuweisung

Entfernt eine Desktop Zuweisung.

## <a name="syntax"></a>Syntax


```mof
uint32 RemoveDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Collectionalias* \[ in\]
</dt> <dd>

Der sammlungsalias.

</dd> <dt>

*Desktopname* \[ in\]
</dt> <dd>

Der Name des Desktops.

</dd> <dt>

*Benutzer Domäne* \[ in\]
</dt> <dd>

Der Domänen Name des Benutzerkontos.

</dd> <dt>

*Benutzername* \[ in\]
</dt> <dd>

Der Name des Benutzerkontos.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | Root \\ CIMV2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ rdmsdesktopzuweisung**](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





