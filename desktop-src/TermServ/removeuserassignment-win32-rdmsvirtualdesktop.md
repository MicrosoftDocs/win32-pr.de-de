---
title: RemoveUserAssignment-Methode der Win32_RDMSVirtualDesktop-Klasse
description: Entfernt die Benutzerzuweisung vom virtuellen Desktop.
ms.assetid: 7ebb34b4-94f6-4a00-87a9-44ad28d103cb
ms.tgt_platform: multiple
keywords:
- RemoveUserAssignment-Methode Remotedesktopdienste
- RemoveUserAssignment-Methode Remotedesktopdienste , Win32_RDMSVirtualDesktop-Klasse
- Win32_RDMSVirtualDesktop Klasse Remotedesktopdienste , RemoveUserAssignment-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.RemoveUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58fa11b22ec089d555fd1e769c71b3fc9d53dbf038ff8b22fb3df559cce59c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988450"
---
# <a name="removeuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>RemoveUserAssignment-Methode der \_ Win32-RDMSVirtualDesktop-Klasse

Entfernt die Benutzerzuweisung vom virtuellen Desktop.

## <a name="syntax"></a>Syntax


```mof
uint32 RemoveUserAssignment(
  [in] string VMName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VMName* \[ In\]
</dt> <dd>

Der Name des virtuellen Computers des virtuellen Desktops.

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

 

 





