---
title: GetPendingStartServerList-Methode der Win32_RDSHServer-Klasse
description: Ruft eine Liste der Server ab, die auf den Start warten.
ms.assetid: 7af7a0e7-dc00-4e3a-8e0c-5987bd2bc3a2
ms.tgt_platform: multiple
keywords:
- GetPendingStartServerList-Methode Remotedesktopdienste
- GetPendingStartServerList-Methode Remotedesktopdienste , Win32_RDSHServer-Klasse
- Win32_RDSHServer-Klasse Remotedesktopdienste , GetPendingStartServerList-Methode
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
ms.openlocfilehash: 61bb46512414c7057d7ec9db5ff4b6fab859f8bb9e6aec5c537250b0baa24e9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422650"
---
# <a name="getpendingstartserverlist-method-of-the-win32_rdshserver-class"></a>GetPendingStartServerList-Methode der Win32 \_ RDSHServer-Klasse

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

*maxServers* \[ In\]
</dt> <dd>

Die maximale Anzahl von Servern, die in der Liste zurückgegeben werden sollen.

</dd> <dt>

*ServerFQDNs* \[ out\]
</dt> <dd>

Enthält bei Erfolg eine Sammlung vollqualifizierte Domänennamen der Server, die auf den Start warten.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Liste der Server wird nach jedem Aufruf zurückgesetzt, sodass der nächste Aufruf keinen doppelten Server erhält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | Root \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**Win32 \_ RDSHServer**](win32-rdshserver.md)
</dt> </dl>

 

 





