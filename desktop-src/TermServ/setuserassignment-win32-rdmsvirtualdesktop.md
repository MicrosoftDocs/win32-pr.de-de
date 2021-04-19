---
title: Setuserzuweisungs-Methode der Win32_RDMSVirtualDesktop-Klasse
description: Weist einem Benutzer einen virtuellen Desktop zu.
ms.assetid: 6a96ccb7-5d3d-4164-a0a3-286a700b414c
ms.tgt_platform: multiple
keywords:
- Setuserzuweisung-Methode Remotedesktopdienste
- Setuserzuweisungs-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktop-Klasse
- Win32_RDMSVirtualDesktop-Klasse Remotedesktopdienste, setuserzuweisungs-Methode
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
ms.openlocfilehash: 5f02e1cc935e344edd6a9c52016052e082e08d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345926"
---
# <a name="setuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Setuserzuweisungs-Methode der Win32 \_ -Klasse rdmsvirtualdesktop

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

*Benutzername* \[ in\]
</dt> <dd>

Der Benutzername des Benutzers.

</dd> <dt>

*Benutzer Domäne* \[ in\]
</dt> <dd>

Der Domänen Name des Benutzers.

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

 

 





