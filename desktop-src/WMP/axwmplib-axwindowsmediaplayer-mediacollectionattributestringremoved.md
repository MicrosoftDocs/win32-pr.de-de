---
title: Mediacollectionattributestraningrebewegereignis des AxWindowsMediaPlayer-Objekts
description: Das Ereignis mediacollectionattributestraningrebewegt tritt auf, wenn ein Attribut Wert aus der Bibliothek entfernt wird. | Mediacollectionattributestraningrebewegereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 2f264416-0bc5-41d0-8863-32c284393082
keywords:
- Mediacollectionattributestraningreverschogereignis der "AxWindowsMediaPlayer"-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11b6b028a2a47585b06159ed46b986124583950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370549"
---
# <a name="mediacollectionattributestringremoved-event-of-the-axwindowsmediaplayer-object"></a>Mediacollectionattributestraningrebewegereignis des AxWindowsMediaPlayer-Objekts

Das Ereignis mediacollectionattributestraningrebewegt tritt auf, wenn ein Attribut Wert aus der Bibliothek entfernt wird.

``` syntax
[C#]
private void player_MediaCollectionAttributeStringRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent
) Handles player.MediaCollectionAttributeStringRemoved
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediacollectionattributestrauingrefivedeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediacollectionattributestrauingremuvedevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.



| Eigenschaft           | BESCHREIBUNG                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bstrattribname** | System. StringGibt den Namen des Attributs an. Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attribut Referenz](attribute-reference.md).<br/> |
| bstrattribval      | System. StringGibt den Wert des Attributs an.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Bemerkungen

Wenn ein Medien Element aus der Bibliothek entfernt wird, werden die zugehörigen Metadaten aus der **mediacollection** entfernt, und dieses Ereignis wird für jedes entfernte Attribut ausgelöst.

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

 

 





