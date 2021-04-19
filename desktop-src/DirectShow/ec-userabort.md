---
description: Der Benutzer hat die Wiedergabe beendet.
ms.assetid: 974a9c3e-cfc9-4608-9f98-732aeaa0a752
title: EC_USERABORT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bab4f76e90d7e5f51655eda6dc72834053df87b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361931"
---
# <a name="ec_userabort"></a>EC \_ userabort

Der Benutzer hat die Wiedergabe beendet.

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

Keine. Die Anwendung muss entscheiden, ob das Diagramm angehalten werden soll.

## <a name="remarks"></a>Bemerkungen

Dieser Ereignis Code signalisiert, dass der Benutzer die normale Graph-Wiedergabe beendet hat. Beispielsweise senden Videorenderer dieses Ereignis, wenn der Benutzer das Videofenster schließt.

Nach dem Senden dieses Ereignisses sollte der Filter alle Beispiele ablehnen und keine [**EC \_ Repaint**](ec-repaint.md) -Ereignisse senden, bis der Filter beendet und zurückgesetzt wird.

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

 

 




