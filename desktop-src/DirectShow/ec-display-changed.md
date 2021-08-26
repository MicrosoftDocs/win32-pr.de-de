---
description: Der Anzeigemodus wurde geändert.
ms.assetid: 1f5b066b-6d5d-44bb-851a-424b2bd389c0
title: EC_DISPLAY_CHANGED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee75517c1927d7f819565d796d9f15fb21050ef7b4ead86d98f582018cc66b7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965920"
---
# <a name="ec_display_changed"></a>\_EC-ANZEIGE \_ GEÄNDERT

Der Anzeigemodus wurde geändert.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Zeiger auf ein Array von [**IPin-Schnittstellen**](/windows/desktop/api/Strmif/nn-strmif-ipin) für die Eingabepins des Videorenderers. Wenn *lParam2* 0 (null) ist, kann dieser Parameter **NULL** sein.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Wenn *lParam2* 0 (null) ist, enthält *lParam1* einen einzelnen **IPin-Zeiger** oder gleich **NULL.** Wenn *lParam2* größer als 0 (null) ist, enthält *lParam1* ein Array von **IPin-Zeigern,** und die Anzahl der Elemente im Array wird von *lParam2* angegeben.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Der Filtergraph-Manager beendet das Diagramm vorübergehend und trennt dann den Videorenderer und stellt die Verbindung wieder her. Das Ereignis wird nicht an die Anwendung übergeben.

## <a name="remarks"></a>Hinweise

Videorenderer können dieses Ereignis als Reaktion auf eine [**WM \_ DISPLAYCHANGE-Nachricht**](/windows/desktop/gdi/wm-displaychange) senden. Die **WM \_ DISPLAYCHANGE-Meldung** gibt an, dass der Benutzer die Anzeigeauflösung geändert hat.

Während der Stecknadelverbindung wählen die meisten Videorenderer ein Format basierend auf dem aktuellen Anzeigemodus aus. Wenn sich der Anzeigemodus ändert, muss der Videorenderer möglicherweise ein anderes Format auswählen. Durch das Senden dieser Nachricht signalisiert der Renderer dem Filtergraph-Manager, dass die Verbindung wiederhergestellt werden muss. Während der erneuten Verbindung kann der Renderer ein neues Format auswählen. Wenn bei der erneuten Verbindung ein Fehler auftritt, sendet der Filtergraph-Manager ein [**EC \_ ERRORABORT-Ereignis**](ec-errorabort.md) an die Anwendung.

### <a name="enhanced-video-renderer"></a>Erweiterter Videorenderer

Ein benutzerdefinierter Presenter für den [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) sollte dieses Ereignis an die EVR senden, wenn sich das Direct3D-Gerät des Moderators ändert. Legen Sie *lParam1* und *lParam2* auf 0 (null) fest. die EVR ignoriert die Ereignisparameter.

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

 

