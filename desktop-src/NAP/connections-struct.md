---
title: Verbindungsstruktur (NapEnforcementClient.h)
description: Enthält Informationen über die Liste der Verbindungen, die von einem Erzwingenden verwaltet werden.
ms.assetid: 79466099-b567-4268-b9bf-d5e57f4d4900
keywords:
- Verbindungsstruktur NAP
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
ms.openlocfilehash: f91e2dc404ff50c7edc3ba80a3c772ac6be762c1fe49575d8503a783e83bbef6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800147"
---
# <a name="connections-structure"></a>Verbindungsstruktur

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **Connections-Struktur** enthält Informationen zur Liste der Verbindungen, die von einem Enforcer verwaltet werden.

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

Die Anzahl aktiver Verbindungen, die derzeit von einem Erzwinger im Bereich von 0 (null) bis [**maxConnectionCountPerEnforcer**](nap-type-constants.md)verwaltet werden.

</dd> <dt>

**connections**
</dt> <dd>

Ein COM-Zeiger auf eine Liste von [**INapEnforcementClientConnection-Schnittstellen,**](inapenforcementclientconnection.md) die Clientverbindungen darstellen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NAP-Referenz](nap-reference.md)
</dt> <dt>

[NAP-Strukturen](nap-structures.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





