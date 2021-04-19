---
title: OpenStateChange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das OpenStateChange-Ereignis tritt auf, wenn die openstate-Eigenschaft den Wert ändert. | OpenStateChange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 0229f8b4-7216-44f6-9838-a640b99bd9f3
keywords:
- OpenStateChange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- OpenStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcd1f2b7e59fdfd35bf31719cbb6a1a5e6c29e66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369547"
---
# <a name="openstatechange-event-of-the-axwindowsmediaplayer-object"></a>OpenStateChange-Ereignis des AxWindowsMediaPlayer-Objekts

Das OpenStateChange-Ereignis tritt auf, wenn die **openstate** -Eigenschaft den Wert ändert.

``` syntax
[C#]
private void player_OpenStateChange(
  object sender,
  _WMPOCXEvents_OpenStateChangeEvent e
)

[Visual Basic]
Private Sub player_OpenStateChange(
  sender As Object,
  e As _WMPOCXEvents_OpenStateChangeEvent
) Handles player.OpenStateChange
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ openstatechangeeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ openstatechangeevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.



| Eigenschaft | BESCHREIBUNG                                                                                                                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NewState | System. Int32Specifies der neue offene Zustand. Eine Tabelle mit Werten finden Sie unter [openstate](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md).<br/> |



 

## <a name="remarks"></a>Bemerkungen

Windows-Media Player können mehrere offene Zustände durchlaufen, während versucht wird, eine Netzwerkdatei zu öffnen, z. b. das Auffinden des Servers, das Herstellen einer Verbindung mit dem Server und schließlich das Öffnen der Datei. Dieses Ereignis wird jedes Mal ausgelöst, wenn sich der Status des geöffneten Zustands ändert.

Es ist nicht garantiert, dass Windows-Media Player Zustände in einer bestimmten Reihenfolge auftreten. Außerdem treten nicht alle Zustände notwendigerweise während einer Sequenz von Ereignissen auf. Sie sollten keinen Code schreiben, der auf der Status Reihenfolge basiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. openstate (VB und c#)**](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> </dl>

 

 





