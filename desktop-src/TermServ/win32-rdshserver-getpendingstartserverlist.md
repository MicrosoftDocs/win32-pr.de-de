---
title: Getpdingstartserverlist-Methode der Win32_RDSHServer-Klasse
description: Ruft eine Liste der Server ab, die auf den Start warten.
ms.assetid: 7af7a0e7-dc00-4e3a-8e0c-5987bd2bc3a2
ms.tgt_platform: multiple
keywords:
- Getpdingstartserverlist-Methode Remotedesktopdienste
- Getpdingstartserverlist-Methode Remotedesktopdienste, Win32_RDSHServer-Klasse
- Win32_RDSHServer-Klasse Remotedesktopdienste, getpdingstartserverlist-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetPendingStartServerList
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99b96453b33f931b18d89f13413513d3baf82bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391961"
---
# <a name="getpendingstartserverlist-method-of-the-win32_rdshserver-class"></a>Getpdingstartserverlist-Methode der Win32 \_ rdshserver-Klasse

Ruft eine Liste der Server ab, die auf den Start warten.

## <a name="syntax"></a>Syntax


```mof
uint32 GetPendingStartServerList(
  [in]  uint32 maxServers,
  [out] string ServerFQDNs[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*maxservers* \[ in\]
</dt> <dd>

Die maximale Anzahl von Servern, die in der Liste zurückgegeben werden sollen.

</dd> <dt>

*Serverfqdns* \[ vorgenommen\]
</dt> <dd>

Bei Erfolg enthält eine Auflistung der voll qualifizierten Domänen Namen der Server, die auf den Start warten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Liste der Server wird nach jedem-Rückruf zurückgesetzt, sodass der nächste-Rückruf keinen doppelten Server erhält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | Root \\ CIMV2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ rdshserver**](win32-rdshserver.md)
</dt> </dl>

 

 





