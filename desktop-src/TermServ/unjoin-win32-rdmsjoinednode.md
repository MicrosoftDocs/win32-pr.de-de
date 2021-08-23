---
title: Unjoin-Methode der Win32_RDMSJoinedNode-Klasse
description: Entfernt einen Knoten aus Remotedesktop Management Services (RDMS).
ms.assetid: 37c462f4-a19d-4b85-8fac-2735deb7c04f
ms.tgt_platform: multiple
keywords:
- Unjoin-Remotedesktopdienste
- Unjoin-methode Remotedesktopdienste , Win32_RDMSJoinedNode-Klasse
- Win32_RDMSJoinedNode klasse Remotedesktopdienste , Unjoin-Methode
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
ms.openlocfilehash: f5d2fae16ecb31326ae16bc08efd1fbc56ae2585140d63ce360783226101d4a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424100"
---
# <a name="unjoin-method-of-the-win32_rdmsjoinednode-class"></a>Unjoin-Methode der Win32 \_ RDMSJoinedNode-Klasse

Entfernt einen Knoten aus Remotedesktop Management Services (RDMS).

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
| Namespace<br/>                | \\Stamm-CIMv2-Rdms \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ RDMSJoinedNode**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





