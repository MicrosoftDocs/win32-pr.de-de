---
description: Ein Filter fordert, dass der Graph neu gestartet wird.
ms.assetid: 58f17338-dd60-4b77-80d3-b6b6a76af9b2
title: EC_NEED_RESTART (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fae3426048229c19b1d35a061d67d3d1d0a3149a8f820e891987c88405b76f7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820142"
---
# <a name="ec_need_restart"></a>EC \_ NEED \_ RESTART

Ein Filter fordert, dass der Graph neu gestartet wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Keinen.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Der Filterdiagramm-Manager hält das Diagramm an und startet es neu. Das Ereignis wird nicht an die Anwendung übergeben.

## <a name="remarks"></a>Hinweise

Wenn ein Filter eine Stichprobe in der Mitte eines Streams zurückweisen soll, wird die Bereitstellung von Stichproben durch den Upstreampin nicht mehr durchgeführt. Der Filter kann den Stream neu starten, indem er dieses Ereignis sendet. Beispielsweise kann der Audiorenderer den Zugriff auf das Soundgerät verlieren, da ein Videofenster den Fokus verloren hat. An diesem Punkt beginnt der Audiorenderer damit, Beispiele abzulehnen. Wenn der Zugriff auf das Soundgerät wiedererlangt wird, sendet es dieses Ereignis, um den Audiostream neu zu starten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




