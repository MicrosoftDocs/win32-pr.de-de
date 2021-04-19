---
title: Mediacollectionattributestringchanged-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das mediacollectionattributestringchanged-Ereignis tritt auf, wenn ein Attribut Wert in der Bibliothek geändert wird. | Mediacollectionattributestringchanged-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: f5b91399-42b7-4202-9b65-caa9b15847b9
keywords:
- Mediacollectionattributestringchanged-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
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
ms.openlocfilehash: c8b83d8036ca0dca7f79e2a9ba721830447f9c5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365613"
---
# <a name="mediacollectionattributestringchanged-event-of-the-axwindowsmediaplayer-object"></a>Mediacollectionattributestringchanged-Ereignis des AxWindowsMediaPlayer-Objekts

Das mediacollectionattributestringchanged-Ereignis tritt auf, wenn ein Attribut Wert in der Bibliothek geändert wird.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediacollectionattributestringchangedeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediacollectionattributestringchangedevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.



| Eigenschaft         | BESCHREIBUNG                                                                                                                                                                                  |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| bstrattribname   | System. StringGibt den Namen des Attributs an. Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attribut Referenz](attribute-reference.md).<br/> |
| bstroldattribval | System. StringGibt den alten Wert des Attributs an.<br/>                                                                                                                            |
| bstraunetwattribval | System. StringGibt den neuen Wert des Attributs an.<br/>                                                                                                                            |



 

## <a name="remarks"></a>Bemerkungen

Wenn ein Benutzer Bibliotheks Metadaten ändert, wird die Mediensammlung aktualisiert, und dieses Ereignis wird für jedes geänderte Attribut ausgelöst.

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

[**AxWindowsMediaPlayer. mediacollection (VB und c#)**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**Iwmpmediacollection-Schnittstelle (VB und c#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





