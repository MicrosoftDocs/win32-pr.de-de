---
title: Mediacollectionattributestringadded-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das mediacollectionattributestringadded-Ereignis tritt auf, wenn der Bibliothek ein Attribut Wert hinzugefügt wird. | Mediacollectionattributestringadded-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: b14db0ce-bd78-4e28-a42c-1a231c29da2b
keywords:
- Mediacollectionattributestringadded-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6712b6caa8f014ec75bf2b031e2d3f6db429dbd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371996"
---
# <a name="mediacollectionattributestringadded-event-of-the-axwindowsmediaplayer-object"></a>Mediacollectionattributestringadded-Ereignis des AxWindowsMediaPlayer-Objekts

Das mediacollectionattributestringadded-Ereignis tritt auf, wenn der Bibliothek ein Attribut Wert hinzugefügt wird.

``` syntax
[C#]
private void player_MediaCollectionAttributeStringAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringAddedEvent
) Handles player.MediaCollectionAttributeStringAdded
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediacollectionattributestringaddedeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediacollectionattributestringaddedevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.



| Eigenschaft           | BESCHREIBUNG                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bstrattribname** | System. StringGibt den Namen des Attributs an. Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attribut Referenz](attribute-reference.md).<br/> |
| bstrattribval      | System. StringGibt den Wert des Attributs an.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Bemerkungen

Wenn der Bibliothek ein Medien Element hinzugefügt wird, werden die zugehörigen Metadaten der Medien Auflistung hinzugefügt, und dieses Ereignis wird für jedes hinzugefügte Attribut ausgelöst.

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

 

 





