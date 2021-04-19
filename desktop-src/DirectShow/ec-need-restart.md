---
description: Ein Filter fordert an, dass das Diagramm neu gestartet wird.
ms.assetid: 58f17338-dd60-4b77-80d3-b6b6a76af9b2
title: EC_NEED_RESTART (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9651ae51b8dd8969a95b4f5e9d5093ec2e879f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353793"
---
# <a name="ec_need_restart"></a>EC \_ muss \_ neu gestartet werden

Ein Filter fordert an, dass das Diagramm neu gestartet wird.

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

Der Filter Graph-Manager hält das Diagramm an und startet es neu. Das Ereignis wird nicht an die Anwendung übergeben.

## <a name="remarks"></a>Bemerkungen

Wenn ein Filter eine Stichprobe in der Mitte eines Streams ablehnt, hält die Upstream-Pin keine Stichproben mehr an. Der Filter kann den Stream neu starten, indem dieses Ereignis gesendet wird. Beispielsweise verliert der audiorenderer möglicherweise den Zugriff auf das Audiogerät, da ein Videofenster den Fokus verliert. An diesem Punkt beginnt der audiorenderer mit dem ablehnen von Beispielen. Wenn der Zugriff auf das Audiogerät wiedererlangt wird, sendet er dieses Ereignis, um den Audiodatenstrom neu zu starten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignis Benachrichtigungs Codes](event-notification-codes.md)
</dt> <dt>

[Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




