---
description: Der Zustand des Filterdiagramms wurde geändert.
ms.assetid: f77b4c06-46a5-4912-adb0-0fa8cb7769aa
title: EC_STATE_CHANGE (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2b476c923f0b812196a5697444433ea0be65b8d3f46bd0388261b2a67a66881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905730"
---
# <a name="ec_state_change"></a>EC \_ STATE \_ CHANGE

Der Zustand des Filterdiagramms wurde geändert.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) Member des [**\_ aufzählten FILTER**](/windows/win32/api/strmif/ne-strmif-filter_state) STATE-Typs, der den neuen Diagrammzustand angibt.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine Standardaktion. Das Ereignis wird nicht an die Anwendung gesendet.

> [!Note]  
> Dieses Ereignis kann auftreten, wenn das Diagramm heruntergefahren wird. Wenn Sie die Standardaktion außer Kraft setzen und auf dieses Ereignis lauschen, müssen Sie besonders darauf achten, keine Ereignisse zu verarbeiten, nachdem Sie den Filter Graph Manager veröffentlicht haben. Andernfalls verweist Ihre Anwendung möglicherweise auf einen ungültigen [**IMediaEvent-Zeiger**](/windows/desktop/api/Control/nn-control-imediaevent) und stürzt ab. Weitere Informationen finden Sie unter [Reagieren auf Ereignisse.](responding-to-events.md)

 

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

 

 




