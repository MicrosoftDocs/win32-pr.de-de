---
description: Die \_ Bitflag-Konstanten von linecallprivilege beschreiben die Arten von Zugriffsrechten oder Berechtigungen, die eine Anwendung mit einem callhandle möglicherweise auf den entsprechenden-Befehl hat.
ms.assetid: a58b7e9e-696e-4421-9b31-1ba8afe6e03b
title: LINECALLPRIVILEGE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2569ec255d2da3ad384292eb87afaa285f54b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371767"
---
# <a name="linecallprivilege_-constants"></a>Linecallprivilege- \_ Konstanten

Die Bitflag-Konstanten von **linecallprivilege \_** beschreiben die Arten von Zugriffsrechten oder Berechtigungen, die eine Anwendung mit einem callhandle möglicherweise auf den entsprechenden-Befehl hat.

<dl> <dt>

<span id="LINECALLPRIVILEGE_MONITOR"></span><span id="linecallprivilege_monitor"></span>**linecallprivilege- \_ Monitor**
</dt> <dd> <dl> <dt>



Die Anwendung verfügt über Monitor Berechtigungen für den-Befehl. Diese Berechtigungen ermöglichen es der Anwendung, Zustandsänderungen sowie Abfrage Informationen und den Status des Aufrufes zu überwachen.


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_NONE"></span><span id="linecallprivilege_none"></span>**linecallprivilege \_ None**
</dt> <dd> <dl> <dt>



Die Anwendung besitzt keine Berechtigungen für den-Befehl. Das Handle der Anwendung ist void und sollte nicht verwendet werden.


</dt> </dl> </dd> <dt>

<span id="LINECALLPRIVILEGE_OWNER"></span><span id="linecallprivilege_owner"></span>**linecallprivilege- \_ Besitzer**
</dt> <dd> <dl> <dt>



Die Anwendung verfügt über Besitzer Berechtigungen für den-Befehl. Mit diesen Berechtigungen kann die Anwendung den-Befehl so bearbeiten, dass Sie den Status des Aufrufes beeinflussen.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Wenn ein Aufruf handle zuerst für eine Anwendung bereitgestellt wird oder wenn die Aufruf Berechtigungen dieser Anwendung geändert werden, wird die [**Zeile \_ CallState**](line-callstate.md) -Nachricht an die Anwendung gesendet. Wenn eine Anwendung einen-Rückruf übergibt und die empfangende Anwendung nicht bereits über ein Handle mit Besitzer Berechtigungen verfügt, informiert diese Nachricht die Anwendung über die neuen Berechtigungen des Aufrufes.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




