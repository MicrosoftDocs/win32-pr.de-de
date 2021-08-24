---
description: Die Größe des nativen Videos wurde geändert.
ms.assetid: 276f37b3-f981-4a01-bb37-1ee77248668f
title: EC_VIDEO_SIZE_CHANGED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da9fc430b8d36a61b90f567f082c7224765a702549d050f11555c8e55c387a86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792380"
---
# <a name="ec_video_size_changed"></a>\_EC-VIDEOGRÖßE \_ \_ GEÄNDERT

Die Größe des nativen Videos wurde geändert.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) Word mit niedriger Reihenfolge gibt die neue Breite in Pixel an. Word in hoher Reihenfolge gibt die neue Höhe in Pixel an.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Hinweise

Videorenderer können dieses Ereignis senden, wenn sie eine Änderung der nativen Videogröße erkennen.

Der [Video Mixing Renderer 7](video-mixing-renderer-filter-7.md) (VMR-7) und der [Video Mixing Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9) senden dieses Ereignis im Fenstermodus, aber nicht im Fenster- oder Rendermodus. Weitere Informationen zum Fenstermodus in der VMR finden Sie unter [Video Rendering](video-rendering.md).

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

 

 




