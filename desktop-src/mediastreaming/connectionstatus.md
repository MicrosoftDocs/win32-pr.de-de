---
title: ConnectionStatus-Enumeration
description: Stellt den Status des Geräts im Netzwerk als zuletzt angezeigt dar.
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
keywords:
- ConnectionStatus-Enumeration Medien Streaming-API
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
ms.openlocfilehash: 61368a494e5bff0f6aca575380937b98f9d6b650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357687"
---
# <a name="connectionstatus-enumeration"></a>ConnectionStatus-Enumeration

Stellt den Status des Geräts im Netzwerk als zuletzt angezeigt dar.

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

<span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Internet**
</dt> <dd>

Das Gerät ist online und im Netzwerk aktiv.

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Aufzu**
</dt> <dd>

Gerät ist offline.

</dd> <dt>

<span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**Geschlafen**
</dt> <dd>

Das Gerät ist zurzeit offline, wird jedoch möglicherweise automatisch aktiviert, wenn versucht wird, damit zu kommunizieren.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Windows. Media. Streaming. idl (Referenz zu Windows. Media. Streaming. idl)</dt> </dl> |



 

 





