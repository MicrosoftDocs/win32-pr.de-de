---
title: Getjoinednodecount-Methode der Win32_RDMSJoinedNode-Klasse
description: Gibt die Anzahl der Server an, auf denen die angegebenen Rollen installiert sind.
ms.assetid: ed2ae0b5-5cbc-4c11-a2ad-065f88dd5842
ms.tgt_platform: multiple
keywords:
- Getjoinednodecount-Methode Remotedesktopdienste
- Getjoinednodecount-Methode Remotedesktopdienste, Win32_RDMSJoinedNode-Klasse
- Win32_RDMSJoinedNode-Klasse Remotedesktopdienste, getjoinednodecount-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.GetJoinedNodeCount
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ecc5c388814873aa690e9af5adda5081aad4d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337925"
---
# <a name="getjoinednodecount-method-of-the-win32_rdmsjoinednode-class"></a>Getjoinednodecount-Methode der Win32 \_ rdmsjoinednode-Klasse

Gibt die Anzahl der Server an, auf denen die angegebenen Rollen installiert sind.

## <a name="syntax"></a>Syntax


```mof
uint32 GetJoinedNodeCount(
  [in]  uint32 roleType,
  [out] uint32 Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RoleType* \[ in\]
</dt> <dd>

Ein Bitfeld, das die Rollen Typen angibt.

<dt>

0
</dt> <dd>

All

</dd> <dt>

1
</dt> <dd>

Remotedesktopverbindung Broker (RDCB)

</dd> <dt>

2
</dt> <dd>

Remotedesktop-Sitzungshost (RDSH)

</dd> <dt>

4
</dt> <dd>

Remotedesktop-Virtualisierungshost (RDVH)

</dd> </dl> </dd> <dt>

*Anzahl* \[ vorgenommen\]
</dt> <dd>

Bei Erfolg wird die Anzahl der Server mit den angegebenen installierten Rollen zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | Root \\ CIMv2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ rdmsjoinednode**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





