---
title: TLS_HANDLE
description: Stellt ein Handle für einen Remotedesktop-Lizenzserver dar.
ms.assetid: 6da51660-a9fd-4e49-97e3-ba0829b1bbbf
ms.tgt_platform: multiple
keywords:
- TLS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09764072b42e14aea2d1b8242dbc3cbb044442b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740713"
---
# <a name="tls_handle"></a>TLS- \_ handle

Stellt ein Handle für einen Remotedesktop-Lizenzserver dar. Dieses Handle wird von der [**tlsconnecttolsserver**](tlsconnecttolsserver.md) -Funktion zurückgegeben.

> [!Note]  
> Diesem Datentyp ist keine Header Datei zugeordnet. Um es zu verwenden, müssen Sie es selbst definieren, wie in diesem Thema gezeigt.

 


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

[**Tlsconnecttolsserver**](tlsconnecttolsserver.md)
</dt> <dt>

[**Tlsdisconnectfromserver**](tlsdisconnectfromserver.md)
</dt> </dl>

 

 





