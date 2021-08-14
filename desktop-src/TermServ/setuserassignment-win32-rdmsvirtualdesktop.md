---
title: SetUserAssignment-Methode der Win32_RDMSVirtualDesktop-Klasse
description: Weist einem Benutzer einen virtuellen Desktop zu.
ms.assetid: 6a96ccb7-5d3d-4164-a0a3-286a700b414c
ms.tgt_platform: multiple
keywords:
- SetUserAssignment-Methode Remotedesktopdienste
- SetUserAssignment-Methode Remotedesktopdienste , Win32_RDMSVirtualDesktop-Klasse
- Win32_RDMSVirtualDesktop-Klasse Remotedesktopdienste , SetUserAssignment-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.SetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f38f87209ba8c8ebd82637f72cea2e798844e6081cd000f2161ee21681422e40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349411"
---
# <a name="setuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>SetUserAssignment-Methode der \_ Win32-RDMSVirtualDesktop-Klasse

Weist einem Benutzer einen virtuellen Desktop zu.

## <a name="syntax"></a>Syntax


```mof
uint32 SetUserAssignment(
  [in] string UserName,
  [in] string UserDomain
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*UserName* \[ In\]
</dt> <dd>

Der Benutzername des Benutzers.

</dd> <dt>

*UserDomain* \[ In\]
</dt> <dd>

Der Domänenname des Benutzers.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktop**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





