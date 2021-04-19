---
description: Ein Plug & Play Gerät wurde entfernt oder wieder verfügbar.
ms.assetid: 0640ba96-22a5-4b82-bd9f-117b67dee311
title: EC_DEVICE_LOST (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fa3f6368e85f8dc54ca6fd8cc2e0eee21262a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367737"
---
# <a name="ec_device_lost"></a>EC- \_ Gerät \_ verloren

Ein Plug & Play Gerät wurde entfernt oder wieder verfügbar.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Ein Zeiger auf die **IUnknown** -Schnittstelle des Filters, der das Gerät darstellt.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

0 (null), wenn das Gerät entfernt wurde, oder 1, wenn das Gerät wieder verfügbar ist.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Bemerkungen

Wenn das Gerät wieder verfügbar wird, ist der vorherige Status des Geräte Filters nicht mehr gültig. Die Anwendung muss das Diagramm neu erstellen, damit das Gerät verwendet werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Benachrichtigung zum Entfernen von Geräten](device-removal-notification.md)
</dt> <dt>

[Ereignis Benachrichtigungs Codes](event-notification-codes.md)
</dt> <dt>

[Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




