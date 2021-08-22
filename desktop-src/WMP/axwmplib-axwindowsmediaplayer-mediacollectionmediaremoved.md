---
title: MediaCollectionMediaRemoved-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das MediaCollectionMediaRemoved-Ereignis tritt auf, wenn ein Medienelement aus der lokalen Bibliothek entfernt wird. | MediaCollectionMediaRemoved-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 66dae2be-2a71-4d53-b2e2-f106426d4eea
keywords:
- MediaCollectionMediaRemoved-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
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
ms.openlocfilehash: 7ee9555b3efc4cb95b164fc8922b1ce4253613fbd2c45c0624a3d61d0fa7a9f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135983"
---
# <a name="mediacollectionmediaremoved-event-of-the-axwindowsmediaplayer-object"></a>MediaCollectionMediaRemoved-Ereignis des AxWindowsMediaPlayer-Objekts

Das MediaCollectionMediaRemoved-Ereignis tritt auf, wenn ein Medienelement aus der lokalen Bibliothek entfernt wird.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaRemovedEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaRemovedEvent**, das die folgende Eigenschaft im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft | Beschreibung                                                                                                                      |
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| pMedia   | System.ObjectDas Medienelement, das aus der lokalen Bibliothek entfernt wurde. Sie können diese in eine IWMPMedia-Schnittstelle umleiten, um darauf zuzugreifen.<br/> |



 

## <a name="remarks"></a>Hinweise

Dieses Ereignis tritt nur für die lokale Bibliothek auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11<br/>                                                                                         |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





