---
description: Der Videorenderer wurde zerstört oder aus dem Diagramm entfernt.
ms.assetid: facf35c2-d6a2-4373-bce5-171fd9325116
title: EC_WINDOW_DESTROYED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdd3e641c7fb911a8da10a4c89682fa266e862de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369579"
---
# <a name="ec_window_destroyed"></a>EC- \_ Fenster \_ zerstört

Der Videorenderer wurde zerstört oder aus dem Diagramm entfernt.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Ein Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Video-Renderers.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Der Filter Graph-Manager gibt dieses Fenster als Fokus über die [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) -Schnittstelle frei. Die Ereignis Benachrichtigung wird nicht an die Anwendung gesendet.

## <a name="remarks"></a>Bemerkungen

Der Videorenderer sendet dieses Ereignis, wenn es das Filter Diagramm verlässt, in der [**ibasefilter:: joinfiltergraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) -Methode. (Das Senden des Ereignisses, wenn der Filter zerstört wird, ist möglicherweise zu spät, da der Filter-Graph-Manager zu diesem Zeitpunkt ebenfalls zerstört werden kann.)

Dieses Ereignis ermöglicht anderen Filtern das Abrufen von Ressourcen, die vom Fenster Fokus abhängen, z. b. Audiogeräte.

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

 

 




