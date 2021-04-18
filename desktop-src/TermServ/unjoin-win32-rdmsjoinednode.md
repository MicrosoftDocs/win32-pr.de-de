---
title: Unjoin-Methode der Win32_RDMSJoinedNode-Klasse
description: Entfernt einen Knoten aus Remotedesktop Verwaltungsdienste (RDMs).
ms.assetid: 37c462f4-a19d-4b85-8fac-2735deb7c04f
ms.tgt_platform: multiple
keywords:
- Unjoin-Methode Remotedesktopdienste
- Unjoin-Methode Remotedesktopdienste, Win32_RDMSJoinedNode-Klasse
- Win32_RDMSJoinedNode-Klasse Remotedesktopdienste, unjoin-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Unjoin
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234f7cc3ad8a797fff51661528f4545ed9fea3a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340340"
---
# <a name="unjoin-method-of-the-win32_rdmsjoinednode-class"></a>Unjoin-Methode der Win32 \_ rdmsjoinednode-Klasse

Entfernt einen Knoten aus Remotedesktop Verwaltungsdienste (RDMs).

## <a name="syntax"></a>Syntax


```mof
uint32 Unjoin();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

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

[**Win32 \_ rdmsjoinednode**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





