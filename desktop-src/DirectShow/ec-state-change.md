---
description: Der Zustand des Filter Diagramms wurde geändert.
ms.assetid: f77b4c06-46a5-4912-adb0-0fa8cb7769aa
title: EC_STATE_CHANGE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64cc62ba15f77370e52821c3335f9a22f573d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360412"
---
# <a name="ec_state_change"></a>Änderung des EC- \_ Zustands \_

Der Zustand des Filter Diagramms wurde geändert.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) Member des Enumerationstyps des [**Filter \_ Zustands**](/windows/win32/api/strmif/ne-strmif-filter_state) , der den neuen Diagramm Zustand angibt.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Keinen.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine Standardaktion. Das Ereignis wird nicht an die Anwendung gesendet.

> [!Note]  
> Dieses Ereignis kann auftreten, wenn das Diagramm heruntergefahren wird. Wenn Sie die Standardaktion überschreiben und auf dieses Ereignis lauschen, müssen Sie besonders darauf achten, dass Ereignisse nach der Freigabe des Filter-Graph-Managers nicht verarbeitet werden. Andernfalls verweist die Anwendung möglicherweise auf einen ungültigen [**imediaevent**](/windows/desktop/api/Control/nn-control-imediaevent) -Zeiger und stürzt ab. Weitere Informationen finden Sie unter [reagieren auf Ereignisse](responding-to-events.md).

 

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

 

 




