---
title: Currentplaylistitemavailable-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das currentplaylistitemavailable-Ereignis tritt auf, wenn die aktuelle Wiedergabeliste verfügbar wird. | Currentplaylistitemavailable-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 101807c9-b00f-4351-a9a3-5413a52496f4
keywords:
- Currentplaylistitemavailable-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- CurrentPlaylistItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be9362a569fe8296284d92204628627c74ae3b44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350755"
---
# <a name="currentplaylistitemavailable-event-of-the-axwindowsmediaplayer-object"></a>Currentplaylistitemavailable-Ereignis des AxWindowsMediaPlayer-Objekts

Das currentplaylistitemavailable-Ereignis tritt auf, wenn die aktuelle Wiedergabeliste verfügbar wird.

``` syntax
[C#]
private void player_CurrentPlaylistItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentPlaylistItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentPlaylistItemAvailable(  
  sender As Object,
  e As _WMPOCXEvents_CurrentPlaylistItemAvailableEvent
) Handles player.CurrentPlaylistItemAvailable
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ currentplaylistitemavailableeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ currentplaylistitemavailableevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.



| Eigenschaft         | BESCHREIBUNG                                                    |
|------------------|----------------------------------------------------------------|
| **bstritemname** | System. stringder Name des aktuellen Wiedergabelisten Elements.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Name der aktuellen Wiedergabeliste kann verwendet werden, um die entsprechende **iwmpwiedergabe** -Schnittstelle von der iwmpplaylistarray-Schnittstelle abzurufen, die von der iwmpplaylistcollection. getByName-Methode zurückgegeben wird.

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

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistarray-Schnittstelle (VB und c#)**](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistcollection. getByName (VB und c#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





