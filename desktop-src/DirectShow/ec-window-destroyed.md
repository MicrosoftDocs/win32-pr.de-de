---
description: Der Videorenderer wurde zerstört oder aus dem Diagramm entfernt.
ms.assetid: facf35c2-d6a2-4373-bce5-171fd9325116
title: EC_WINDOW_DESTROYED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d7b26224fee4e18d92d16d8f3bfe277c70cf2b260a19c9c7d6438477266c3e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686030"
---
# <a name="ec_window_destroyed"></a>\_EC-FENSTER \_ ZERSTÖRT

Der Videorenderer wurde zerstört oder aus dem Diagramm entfernt.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Zeiger auf die [**IBaseFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) des Videorenderers.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Der Filtergraph-Manager gibt dieses Fenster über die [**IResourceManager-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) als Fokus frei. Die Ereignisbenachrichtigung wird nicht an die Anwendung gesendet.

## <a name="remarks"></a>Hinweise

Der Videorenderer sendet dieses Ereignis, wenn er das Filterdiagramm verlässt, in seiner [**IBaseFilter::JoinFilterGraph-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) (Das Senden des Ereignisses, wenn der Filter zerstört wird, kann zu spät sein, da an diesem Punkt auch der Filtergraph-Manager zerstört werden kann.)

Dieses Ereignis ermöglicht anderen Filtern das Abrufen von Ressourcen, die vom Fensterfokus abhängen, z. B. Audiogeräte.

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

 

 




