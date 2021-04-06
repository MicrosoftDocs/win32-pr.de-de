---
title: Adddesktopzuweisung-Methode der Win32_RDMSDesktopAssignment-Klasse
description: Fügen Sie eine Desktop Zuweisung hinzu.
ms.assetid: 3690f70e-d0c3-444a-a0b7-cec6994eb3b8
ms.tgt_platform: multiple
keywords:
- Adddesktopzuweisung-Methode Remotedesktopdienste
- Adddesktopzuweisung-Methode Remotedesktopdienste, Win32_RDMSDesktopAssignment-Klasse
- Win32_RDMSDesktopAssignment-Klasse Remotedesktopdienste, adddesktopzuweisungs-Methode
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
ms.openlocfilehash: 571273e76b0bb45b748f1587e5a831fcf1e36b0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858807"
---
# <a name="adddesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a>Adddesktopzuweisung-Methode der Win32- \_ Klasse rdmsdesktopzuweisung

Hinzufügen einer Desktop Zuweisung

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

 

 





