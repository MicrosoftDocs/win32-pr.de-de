---
description: Ein Plug & Play wurde entfernt oder wieder verfügbar.
ms.assetid: 0640ba96-22a5-4b82-bd9f-117b67dee311
title: EC_DEVICE_LOST (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4868890967d6448226c1f000ab06b7ccbcf7a06e3062d1cdef03e0ad960bc7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998160"
---
# <a name="ec_device_lost"></a>EC \_ DEVICE LOST (EC-GERÄT \_ VERLOREN)

Ein Plug & Play wurde entfernt oder wieder verfügbar.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Zeiger auf die **IUnknown-Schnittstelle** des Filters, der das Gerät darstellt.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

0 (null), wenn das Gerät entfernt wurde, oder 1, wenn das Gerät wieder verfügbar ist.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine.

## <a name="remarks"></a>Hinweise

Wenn das Gerät wieder verfügbar ist, ist der vorherige Zustand des Gerätefilters nicht mehr gültig. Die Anwendung muss das Diagramm neu erstellen, um das Gerät verwenden zu können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Benachrichtigung zum Entfernen von Geräten](device-removal-notification.md)
</dt> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




