---
title: TLS_HANDLE
description: Stellt ein Handle für einen Remotedesktop Lizenzserver dar.
ms.assetid: 6da51660-a9fd-4e49-97e3-ba0829b1bbbf
ms.tgt_platform: multiple
keywords:
- TLS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04daf14429a5b400267e664a615739fd14e8306e987f50726cfdb341522870a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869450"
---
# <a name="tls_handle"></a>\_TLS-HANDLE

Stellt ein Handle für einen Remotedesktop Lizenzserver dar. Dieses Handle wird von der [**TLSConnectToLsServer-Funktion**](tlsconnecttolsserver.md) zurückgegeben.

> [!Note]  
> Diesem Datentyp ist keine Headerdatei zugeordnet. Um es zu verwenden, müssen Sie es selbst definieren, wie in diesem Thema gezeigt.

 


```C++
typedef HANDLE TLS_HANDLE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> </dl>

 

 





