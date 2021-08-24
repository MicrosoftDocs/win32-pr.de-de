---
title: MediaCollectionMediaAdded-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das MediaCollectionMediaAdded-Ereignis tritt auf, wenn der lokalen Bibliothek ein Medienelement hinzugefügt wird. | MediaCollectionMediaAdded-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: ba1779f6-a212-44f4-b52a-c88e22aebcce
keywords:
- MediaCollectionMediaAdded-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionMediaAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb48a41970840a45344e2e6fdd578f4e84e23751fd8e337052e66ccd0a058d5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765100"
---
# <a name="mediacollectionmediaadded-event-of-the-axwindowsmediaplayer-object"></a>MediaCollectionMediaAdded-Ereignis des AxWindowsMediaPlayer-Objekts

Das MediaCollectionMediaAdded-Ereignis tritt auf, wenn der lokalen Bibliothek ein Medienelement hinzugefügt wird.

``` syntax
[C#]
private void player_MediaCollectionMediaAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionMediaAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaAddedEvent
) Handles player.MediaCollectionMediaAdded
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaAddedEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaAddedEvent**, das die folgende Eigenschaft im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft | Beschreibung                                                                                                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------|
| pMedia   | System.ObjectDas Medienelement, das der lokalen Bibliothek hinzugefügt wurde. Sie können diese in eine IWMPMedia-Schnittstelle umleiten, um darauf zuzugreifen.<br/> |



 

## <a name="remarks"></a>Hinweise

Dieses Ereignis tritt nur für die lokale Bibliothek auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11<br/>                                                                                         |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.mediaCollection (VB und C#)**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection-Schnittstelle (VB und C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





