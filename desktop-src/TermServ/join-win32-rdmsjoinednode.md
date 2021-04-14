---
title: Joinmethode der Win32_RDMSJoinedNode-Klasse
description: Fügt Remotedesktop Verwaltungsdienste (RDMs) einen Knoten hinzu.
ms.assetid: 7451d12a-ace2-4564-bf6d-fb0169be967f
ms.tgt_platform: multiple
keywords:
- Joinmethode Remotedesktopdienste
- Joinmethode Remotedesktopdienste, Win32_RDMSJoinedNode-Klasse
- Win32_RDMSJoinedNode-Klasse Remotedesktopdienste, Join-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Join
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587e68758971453e8c4e307ccb37ce6cede262f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391660"
---
# <a name="join-method-of-the-win32_rdmsjoinednode-class"></a>Joinmethode der Win32 \_ rdmsjoinednode-Klasse

Fügt Remotedesktop Verwaltungsdienste (RDMs) einen Knoten hinzu.

## <a name="syntax"></a>Syntax


```mof
uint32 Join(
  [in] string NodeFQDN,
  [in] string NodeSID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Nodefqdn* \[ in\]
</dt> <dd>

Der voll qualifizierte Domänen Name des Knotens.

</dd> <dt>

*Nodesid* \[ in\]
</dt> <dd>

Die Sicherheits-ID (SID) des Knotens.

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

[**Win32 \_ rdmsjoinednode**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





