---
description: Der Videorenderer wechselt aus dem Vollbildmodus.
ms.assetid: f720a9b6-930a-4ed7-9798-1c72fa7a11ff
title: EC_FULLSCREEN_LOST (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf9384bec15969c904636f37db21ab19674bd2468542c2984ce80aa1773c3c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079130"
---
# <a name="ec_fullscreen_lost"></a>EC \_ FULLSCREEN \_ LOST

Der Videorenderer wechselt aus dem Vollbildmodus.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Keinen.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Zeiger auf die [**IBaseFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) des Videorenderers oder **NULL.**

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Hinweise

Wenn der [Vollbildrenderer](full-screen-renderer-filter.md) die Aktivierung verliert, sendet er dieses Ereignis. Wenn ein anderer Videorenderer aus dem Vollbildmodus wechselt, sendet der Filterdiagramm-Manager dieses Ereignis als Reaktion auf ein [**EC \_ ACTIVATE-Ereignis**](ec-activate.md) vom Renderer.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




