---
description: Ein Videofenster wird aktiviert oder deaktiviert.
ms.assetid: 2e004899-bb2b-4127-b606-e2a979275836
title: EC_ACTIVATE (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b14d9b0ad192045f179d9f0f366eed6a32efb0e6cc6f61b47255f118b7f55258
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966060"
---
# <a name="ec_activate"></a>EC \_ ACTIVATE

Ein Videofenster wird aktiviert oder deaktiviert.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**BOOL**) **TRUE,** wenn das Fenster aktiviert ist, oder **FALSE,** wenn das Fenster deaktiviert ist.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Zeiger auf die [**IBaseFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) des Renderers.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Der Filterdiagramm-Manager legt den Fokus über die [**IResourceManager-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) fest. Die Ereignisbenachrichtigung wird nicht an die Anwendung gesendet.

## <a name="remarks"></a>Hinweise

Ein Videorenderer sendet dieses Ereignis, wenn sein Fenster aktiviert oder deaktiviert wird (d. h. wenn er eine WM \_ ACTIVATEAPP-Nachricht empfängt). Die Fensteraktivierung oder -deaktivierung kann auftreten, weil das Fenster den Fokus gewonnen oder verloren hat oder weil der Renderer zwischen dem Vollbildmodus und dem Fenstermodus umgeschaltet wurde.

Mit diesem Ereignis kann der Filtergraph-Manager Ressourcen zuordnen, die vom Fensterfokus abhängig sind, z. B. Audiogeräte.

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

 

 




