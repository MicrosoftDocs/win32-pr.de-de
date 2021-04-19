---
description: Die Größe des nativen Videos wurde geändert.
ms.assetid: 276f37b3-f981-4a01-bb37-1ee77248668f
title: EC_VIDEO_SIZE_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a70ceab583d8dfc51b417fb701a2988b2e96f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367037"
---
# <a name="ec_video_size_changed"></a>Größe des EC- \_ Videos \_ \_ geändert

Die Größe des nativen Videos wurde geändert.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) Word in niedriger Ordnung gibt die neue Breite in Pixel an. hohes Wort gibt die neue Höhe in Pixel an.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Bemerkungen

Videorenderer Senden dieses Ereignis möglicherweise, wenn Sie eine Änderung an der systemeigenen Videogröße erkennen.

Der [Video Mischungs-Renderer 7](video-mixing-renderer-filter-7.md) (VMR-7) und der [Video Mischungs-Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9) senden dieses Ereignis im Fenstermodus, aber nicht im fensterlosen Modus oder im Modus für renderlos. Weitere Informationen zum Fenster-Modus in der VMR finden Sie unter [Video Rendering](video-rendering.md).

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

 

 




