---
description: Das Diagramm puffert Daten oder hat die Pufferung von Daten beendet.
ms.assetid: 39e8b151-0323-42b3-99f0-3dcd230925c8
title: EC_BUFFERING_DATA (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc937973db8435657d131ff4adea83892bf87681bb3db9b7d016565f5c38670
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965970"
---
# <a name="ec_buffering_data"></a>EC \_ BUFFERING \_ DATA

Das Diagramm puffert Daten oder hat die Pufferung von Daten beendet.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**BOOL**) **TRUE,** wenn der Puffer für das Diagramm beginnt, oder **FALSE,** wenn die Pufferung des Graphen beendet wurde.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Hinweise

Ein Filter kann dieses Ereignis senden, wenn daten aus einer externen Quelle gepuffert werden müssen. (Dies kann z. B. das Laden von Daten aus einem Netzwerk sein.) Die Anwendung kann dieses Ereignis verwenden, um die Benutzeroberfläche anzupassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




