---
title: Getuserzuweisungs-Methode der Win32_RDMSVirtualDesktop-Klasse
description: Ruft den Benutzernamen und den Domänen Namen des Benutzers ab, der dem virtuellen Desktop zugewiesen ist.
ms.assetid: 1887c49d-85df-4fb4-9b40-42fb7763bf95
ms.tgt_platform: multiple
keywords:
- Getuserzuweisungs-Methode Remotedesktopdienste
- Getuserzuweisungs-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktop-Klasse
- Win32_RDMSVirtualDesktop-Klasse Remotedesktopdienste, getuserzuweisungs-Methode
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
ms.openlocfilehash: 87293a471bb4f69b3f4c57de0f964fa0daa043cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392033"
---
# <a name="getuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Getuserzuweisungs-Methode der Win32 \_ rdmsvirtualdesktop-Klasse

Ruft den Benutzernamen und den Domänen Namen des Benutzers ab, der dem virtuellen Desktop zugewiesen ist.

## <a name="syntax"></a>Syntax


```mof
uint32 GetUserAssignment(
  [out] string UserName,
  [out] string UserDomain
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Benutzername* \[ vorgenommen\]
</dt> <dd>

Empfängt den Benutzernamen.

</dd> <dt>

*Benutzer Domäne* \[ vorgenommen\]
</dt> <dd>

Empfängt den Domänen Namen.

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

 

 





