---
title: Mediacollectionmediareverschodas Ereignis des AxWindowsMediaPlayer-Objekts
description: Das Ereignis mediacollectionmediareverschohe tritt auf, wenn ein Medien Element aus der lokalen Bibliothek entfernt wird. | Mediacollectionmediareverschodas Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 66dae2be-2a71-4d53-b2e2-f106426d4eea
keywords:
- Mediacollectionmediareverschodas Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- MediaCollectionMediaRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea15ff63fb913cd399a152913a27ffda1090d9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372231"
---
# <a name="mediacollectionmediaremoved-event-of-the-axwindowsmediaplayer-object"></a>Mediacollectionmediareverschodas Ereignis des AxWindowsMediaPlayer-Objekts

Das Ereignis mediacollectionmediareverschohe tritt auf, wenn ein Medien Element aus der lokalen Bibliothek entfernt wird.

``` syntax
[C#]
private void player_MediaCollectionMediaRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaRemovedEvent e
)
        
[Visual Basic]
Private Sub player_MediaCollectionMediaRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaRemovedEvent
) Handles player.MediaCollectionMediaRemoved
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediacollectionmediaremuvedeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediacollectionmediaremuvedevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.



| Eigenschaft | BESCHREIBUNG                                                                                                                      |
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| pmedia   | System. objectdas Medien Element, das aus der lokalen Bibliothek entfernt wurde. Sie können dies in eine iwmpmedia-Schnittstelle umwandeln, um darauf zuzugreifen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis tritt nur für die lokale Bibliothek auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11<br/>                                                                                         |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





