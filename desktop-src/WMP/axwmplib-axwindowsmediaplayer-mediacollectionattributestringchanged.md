---
title: MediaCollectionAttributeStringChanged-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das MediaCollectionAttributeStringChanged-Ereignis tritt auf, wenn ein Attributwert in der Bibliothek geändert wird. | MediaCollectionAttributeStringChanged-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: f5b91399-42b7-4202-9b65-caa9b15847b9
keywords:
- MediaCollectionAttributeStringChanged-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringChanged Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dcc755d1a183525923b91ce2de7937860582c3cf795d13cbf4a8c22d7c9c37f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618780"
---
# <a name="mediacollectionattributestringchanged-event-of-the-axwindowsmediaplayer-object"></a>MediaCollectionAttributeStringChanged-Ereignis des AxWindowsMediaPlayer-Objekts

Das MediaCollectionAttributeStringChanged-Ereignis tritt auf, wenn ein Attributwert in der Bibliothek geändert wird.

``` syntax
[C#]
private void player_MediaCollectionAttributeStringChanged(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringChanged(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringChangedEvent
) Handles player.MediaCollectionAttributeStringChanged
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringChangedEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringChangedEvent**, das die folgenden Eigenschaften im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft         | Beschreibung                                                                                                                                                                                  |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| bstrAttribName   | System.String Gibt den Namen des Attributs an. Informationen zu den attributen, die von Windows Media Player unterstützt werden, finden Sie unter [Attributverweis.](attribute-reference.md)<br/> |
| bstrOldAttribVal | System.String Gibt den alten Wert des Attributs an.<br/>                                                                                                                            |
| bstrNewAttribVal | System.String Gibt den neuen Wert des Attributs an.<br/>                                                                                                                            |



 

## <a name="remarks"></a>Hinweise

Wenn ein Benutzer Bibliotheksmetadaten ändert, wird die Mediensammlung aktualisiert, und dieses Ereignis wird für jedes geänderte Attribut ausgelöst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.mediaCollection (VB und C#)**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection-Schnittstelle (VB und C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





