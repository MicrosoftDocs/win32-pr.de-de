---
description: Die LINECALLPRIVILEGE-Bitflags-Konstanten beschreiben die Arten von Zugriffsrechten oder Berechtigungen, die eine Anwendung mit einem Aufrufhand handle für den \_ entsprechenden Aufruf haben kann.
ms.assetid: a58b7e9e-696e-4421-9b31-1ba8afe6e03b
title: LINECALLPRIVILEGE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c00dd43442345c545bb5e0b1718131b6815fd236f9c7d770c0f3b47b10b47a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660050"
---
# <a name="linecallprivilege_-constants"></a>\_LINECALLPRIVILEGE-Konstanten

Die **\_ LINECALLPRIVILEGE-Bitflags-Konstanten** beschreiben die Arten von Zugriffsrechten oder Berechtigungen, die eine Anwendung mit einem Aufrufhand handle für den entsprechenden Aufruf haben kann.

<dl> <dt>

<span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**\_LINECALLPRIVILEGE-MONITOR**
</dt> <dd> <dl> <dt>



Die Anwendung verfügt über Monitorberechtigungen für den Aufruf. Mit diesen Berechtigungen kann die Anwendung Zustandsänderungen überwachen und Informationen und den Status des Aufrufs abfragen.


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**LINECALLPRIVILEGE \_ NONE**
</dt> <dd> <dl> <dt>



Die Anwendung verfügt über keine Berechtigungen für den Aufruf. Das Handle der Anwendung ist void und sollte nicht verwendet werden.


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**LINECALLPRIVILEGE \_ OWNER**
</dt> <dd> <dl> <dt>



Die Anwendung verfügt über Besitzerberechtigungen für den Aufruf. Mit diesen Berechtigungen kann die Anwendung den Aufruf auf eine Weise bearbeiten, die sich auf den Zustand des Aufrufs auswirken kann.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Wenn ein Aufrufhand handle zum ersten Mal für eine Anwendung bereitgestellt wird oder wenn Aufrufberechtigungen dieser Anwendung geändert werden, wird die [**LINE \_ CALLSTATE-Nachricht**](line-callstate.md) an die Anwendung gesendet. Wenn eine Anwendung einen Aufruf abgibt und die empfangende Anwendung noch nicht über ein Handle mit Besitzerberechtigungen verfügt, informiert diese Meldung die Anwendung über die neuen Berechtigungen für den Aufruf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




