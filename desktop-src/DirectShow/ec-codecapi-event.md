---
description: 'Das EC \_ codecapi- \_ Ereignis Ereignis wird von einem Encoder gesendet, um ein Codierungs Ereignis zu signalisieren. Der Client registriert sich für das encoderereignis, indem er die icodecapi:: RegisterForEvent-Methode aufrufen.'
ms.assetid: 88924ba9-707b-41a7-9bca-c630b4a9c4c8
title: EC_CODECAPI_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c24ece20a0c729b251c56b50b5b44fc9f7fa98f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372075"
---
# <a name="ec_codecapi_event"></a>EC \_ codecapi- \_ Ereignis

Das EC \_ codecapi- \_ Ereignis Ereignis wird von einem Encoder gesendet, um ein Codierungs Ereignis zu signalisieren. Der Client registriert sich für das encoderereignis, indem er die [**icodecapi:: RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) -Methode aufrufen.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Benutzerdaten. Der Wert dieses Parameters ist der Zeiger, den der Aufrufer im *UserData* -Parameter der [**RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) -Methode angegeben hat.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ein Zeiger auf die Ereignisdaten. Diese Daten werden vom Encoder zugeordnet und müssen von der Anwendung freigegeben werden, indem die **CoTaskMemFree** -Funktion verwendet wird. Der Datenblock beginnt mit einer [**codecapieventdata**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) -Struktur. Wandeln Sie den *lParam2* -Parameter in einen Zeiger auf diese-Struktur um.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine Standardaktion.

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

 

 




