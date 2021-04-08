---
title: Connections-Struktur (napforcementclient. h)
description: Enthält Informationen über die Liste der Verbindungen, die von einem-Enforcer verwaltet werden.
ms.assetid: 79466099-b567-4268-b9bf-d5e57f4d4900
keywords:
- Verbindungs Struktur-NAP
topic_type:
- apiref
api_name:
- Connections
api_location:
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e79add74830dfa8ca77fa24a5d3233542a7e553
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957233"
---
# <a name="connections-structure"></a>Verbindungs Struktur

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **Connections** -Struktur enthält Informationen über die Liste der Verbindungen, die von einem-Enforcer verwaltet werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagConnections {
  UINT16                          count;
  INapEnforcementClientConnection **connections;
} Connections;
```



## <a name="members"></a>Member

<dl> <dt>

**count**
</dt> <dd>

Die Anzahl der aktiven Verbindungen, die zurzeit von einem-Enforcer innerhalb des Bereichs 0 (null) bis [**maxconnectionzähltperenforcer**](nap-type-constants.md)verwaltet werden.

</dd> <dt>

**connections**
</dt> <dd>

Ein com-Zeiger auf eine Liste von [**inapenforcementclientconnection**](inapenforcementclientconnection.md) -Schnittstellen, die Clientverbindungen darstellen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Napforcementclient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napforcementclient. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NAP-Referenz](nap-reference.md)
</dt> <dt>

[NAP-Strukturen](nap-structures.md)
</dt> <dt>

[**Inapenforcementclientconnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





