---
description: Das EC \_ CODECAPI EVENT-Ereignis wird von einem Encoder gesendet, \_ um ein Codierungsereignis zu signalisieren. Der Client registriert sich für das Encoderereignis, indem er die ICodecAPI::RegisterForEvent-Methode aufruft.
ms.assetid: 88924ba9-707b-41a7-9bca-c630b4a9c4c8
title: EC_CODECAPI_EVENT (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5765c2a1156653e66c5d3685cacfdd551cd22032eea34463f5450dc6d4fbea3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965940"
---
# <a name="ec_codecapi_event"></a>EC \_ \_ CODECAPI-EREIGNIS

Das EC \_ CODECAPI EVENT-Ereignis wird von einem Encoder gesendet, \_ um ein Codierungsereignis zu signalisieren. Der Client registriert sich für das Encoderereignis, indem er die [**ICodecAPI::RegisterForEvent-Methode**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) aufruft.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Benutzerdaten. Der Wert dieses Parameters ist der Zeiger, den der Aufrufer im *userData-Parameter* der [**RegisterForEvent-Methode angegeben**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) hat.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zeiger auf die Ereignisdaten. Diese Daten werden vom Encoder zugeordnet und müssen von der Anwendung mithilfe der **CoTaskMemFree-Funktion frei werden.** Der Datenblock beginnt mit einer [**CodecAPIEventData-Struktur.**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) cast the lParam2 parameter to a pointer to this structure. (Der *lParam2-Parameter* wird in einen Zeiger auf diese Struktur umgeformt.)

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Keine Standardaktion.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Ereignisbenachrichtigungscodes](event-notification-codes.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




