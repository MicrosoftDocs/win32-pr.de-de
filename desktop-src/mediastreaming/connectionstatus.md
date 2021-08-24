---
title: ConnectionStatus-Enumeration
description: Stellt den Zustand des Geräts im Netzwerk wie zuletzt gesehen dar.
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
keywords:
- Media Streaming-API für ConnectionStatus-Enumeration
topic_type:
- apiref
api_name:
- ConnectionStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8617012abe75d213e0de7be70811152315a888693c7336ef58cd34ceb98eba55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721250"
---
# <a name="connectionstatus-enumeration"></a>ConnectionStatus-Enumeration

Stellt den Zustand des Geräts im Netzwerk wie zuletzt gesehen dar.

## <a name="syntax"></a>Syntax


```C++
typedef enum ConnectionStatus { 
  Online    = 0,
  Offline   = 1,
  Sleeping  = 2
} ConnectionStatus;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Online**
</dt> <dd>

Das Gerät ist online und im Netzwerk aktiv.

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline**
</dt> <dd>

Gerät ist offline.

</dd> <dt>

<span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**Schlafen**
</dt> <dd>

Das Gerät ist derzeit offline, wird aber möglicherweise automatisch aktiviert, wenn versucht wird, mit ihm zu kommunizieren.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>Windows. Media.Streaming.idl (Referenz Windows. Media.Streaming.idl)</dt> </dl> |



 

 





