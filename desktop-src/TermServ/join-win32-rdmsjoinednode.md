---
title: Join-Methode der Win32_RDMSJoinedNode-Klasse
description: Fügt Remotedesktop Management Services (RDMS) einen Knoten hinzu.
ms.assetid: 7451d12a-ace2-4564-bf6d-fb0169be967f
ms.tgt_platform: multiple
keywords:
- Join-Methode Remotedesktopdienste
- Join-Methode Remotedesktopdienste , Win32_RDMSJoinedNode-Klasse
- Win32_RDMSJoinedNode Klasse Remotedesktopdienste , Join-Methode
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
ms.openlocfilehash: 204d83988f9a57d9fe0edf8daa6dc580676fc7395f98edcbece49674c0041aef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605423"
---
# <a name="join-method-of-the-win32_rdmsjoinednode-class"></a>Join-Methode der Win32 \_ RDMSJoinedNode-Klasse

Fügt Remotedesktop Management Services (RDMS) einen Knoten hinzu.

## <a name="syntax"></a>Syntax


```mof
uint32 Join(
  [in] string NodeFQDN,
  [in] string NodeSID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NodeFQDN* \[ In\]
</dt> <dd>

Der vollqualifizierte Domänenname des Knotens.

</dd> <dt>

*NodeSID* \[ In\]
</dt> <dd>

Die Sicherheits-ID (SID) des Knotens.

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

[**Win32 \_ RDMSJoinedNode**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





