---
title: Removeuserzuweisungs-Methode der Win32_RDMSVirtualDesktop-Klasse
description: Entfernt die Benutzer Zuweisung vom virtuellen Desktop.
ms.assetid: 7ebb34b4-94f6-4a00-87a9-44ad28d103cb
ms.tgt_platform: multiple
keywords:
- Removeuserzuweisungs-Methode Remotedesktopdienste
- Removeuserzuweisungs-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktop-Klasse
- Win32_RDMSVirtualDesktop-Klasse Remotedesktopdienste, removeuserzuweisungs-Methode
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
ms.openlocfilehash: 01675c777603f0eab2d22c0136b1ef6cc3522b7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345903"
---
# <a name="removeuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Removeuserzuweisungs-Methode der Win32 \_ rdmsvirtualdesktop-Klasse

Entfernt die Benutzer Zuweisung vom virtuellen Desktop.

## <a name="syntax"></a>Syntax


```mof
uint32 RemoveUserAssignment(
  [in] string VMName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VMName* \[ in\]
</dt> <dd>

Der Name des virtuellen Computers des virtuellen Desktops.

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

 

 





