---
title: GetUserAssignment-Methode der Win32_RDMSVirtualDesktop Klasse
description: Ruft den Benutzernamen und domänennamen des Benutzers ab, der dem virtuellen Desktop zugewiesen ist.
ms.assetid: 1887c49d-85df-4fb4-9b40-42fb7763bf95
ms.tgt_platform: multiple
keywords:
- GetUserAssignment-Remotedesktopdienste
- GetUserAssignment-Methode Remotedesktopdienste , Win32_RDMSVirtualDesktop-Klasse
- Win32_RDMSVirtualDesktop klasse Remotedesktopdienste , GetUserAssignment-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff3d63179ec68c38ada5738390979e4844ff2950f91decf82245a6b164dbab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059558"
---
# <a name="getuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>GetUserAssignment-Methode der Win32 \_ RDMSVirtualDesktop-Klasse

Ruft den Benutzernamen und domänennamen des Benutzers ab, der dem virtuellen Desktop zugewiesen ist.

## <a name="syntax"></a>Syntax


```mof
uint32 GetUserAssignment(
  [out] string UserName,
  [out] string UserDomain
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*UserName* \[ out\]
</dt> <dd>

Empfängt den Benutzernamen.

</dd> <dt>

*UserDomain* \[ out\]
</dt> <dd>

Empfängt den Domänennamen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\Stamm-CIMv2-Rdms \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktop**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





