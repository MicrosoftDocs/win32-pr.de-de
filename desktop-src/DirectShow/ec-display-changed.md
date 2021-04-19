---
description: Der Anzeigemodus wurde geändert.
ms.assetid: 1f5b066b-6d5d-44bb-851a-424b2bd389c0
title: EC_DISPLAY_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549a4c5201906b692a1bd726e65269679705e9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356016"
---
# <a name="ec_display_changed"></a>EC- \_ Anzeige \_ geändert

Der Anzeigemodus wurde geändert.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Zeiger auf ein Array von [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstellen für die Eingabe Pins des Video-Renderers. Wenn *lParam2* NULL ist, kann dieser Parameter **null** sein.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Wenn *lParam2* NULL ist, enthält *lParam1* einen einzelnen **IPin** -Zeiger oder ist gleich **null**. Wenn *lParam2* größer als 0 (null) ist, enthält *lParam1* ein Array von **IPin** -Zeigern, und die Anzahl der Elemente im Array wird von *lParam2* angegeben.

</dd> </dl>

## <a name="default-action"></a>Standardaktion

Der Filter Graph-Manager stoppt das Diagramm temporär und trennt dann die Verbindung mit dem Videorenderer und stellt die Verbindung wieder her. Das Ereignis wird nicht an die Anwendung übergeben.

## <a name="remarks"></a>Bemerkungen

Videorenderer können dieses Ereignis als Antwort auf eine WM- [**\_ displaychange**](/windows/desktop/gdi/wm-displaychange) -Nachricht senden. Die Meldung " **WM \_ displaychange** " gibt an, dass der Benutzer die Bildschirmauflösung geändert hat.

Während der Pin-Verbindung wählen die meisten Videorenderer ein Format aus, das auf dem aktuellen Anzeigemodus basiert. Wenn sich der Anzeigemodus ändert, muss der Videorenderer möglicherweise ein anderes Format auswählen. Durch Senden dieser Nachricht signalisiert der Renderer dem Filter Graph-Manager, dass er erneut verbunden werden muss. Während der erneuten Verbindung kann der Renderer ein neues Format auswählen. Wenn die erneute Verbindungs Herstellung fehlschlägt, sendet der Filter Graph-Manager ein [**EC \_ errorabort**](ec-errorabort.md) -Ereignis an die Anwendung.

### <a name="enhanced-video-renderer"></a>Erweiterter Videorenderer

Ein benutzerdefinierter Presenter für den [**erweiterten Videorenderer**](enhanced-video-renderer-filter.md) (EVR) sollte dieses Ereignis an den EVR senden, wenn sich das Direct3D-Gerät des Presenter ändert. Legen Sie *lParam1* und *lParam2* auf 0 (null) fest. der EVR ignoriert die Ereignis Parameter.

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

 

