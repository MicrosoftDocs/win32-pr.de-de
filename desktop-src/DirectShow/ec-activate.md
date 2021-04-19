---
description: Ein Videofenster wird aktiviert oder deaktiviert.
ms.assetid: 2e004899-bb2b-4127-b606-e2a979275836
title: EC_ACTIVATE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e48adb3ae98af172664b807386c615d34b6b22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359390"
---
# <a name="ec_activate"></a>Aktivieren von EC \_

Ein Videofenster wird aktiviert oder deaktiviert.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**Bool**) **True** , wenn das Fenster aktiviert ist, oder **false** , wenn das Fenster deaktiviert ist.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Ein Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Renderers.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Der Filter Graph-Manager legt den Fokus über die [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) -Schnittstelle fest. Die Ereignis Benachrichtigung wird nicht an die Anwendung gesendet.

## <a name="remarks"></a>Bemerkungen

Ein Videorenderer sendet dieses Ereignis, wenn das Fenster aktiviert oder deaktiviert wird (d. h., wenn es eine WM \_ activateapp-Nachricht empfängt). Die Fenster Aktivierung oder-Deaktivierung kann auftreten, da der Fokus im Fenster erreicht oder verloren gegangen ist oder der Renderer zwischen dem Vollbildmodus und dem Fenstermodus gewechselt hat.

Dieses Ereignis ermöglicht es dem Filter Graph-Manager, Ressourcen zuzuordnen, die von Fenster Fokus abhängen, z. b. Audiogeräte.

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

 

 




