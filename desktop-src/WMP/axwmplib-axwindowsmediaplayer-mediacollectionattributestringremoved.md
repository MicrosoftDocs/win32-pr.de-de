---
title: MediaCollectionAttributeStringRemoved-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das MediaCollectionAttributeStringRemoved-Ereignis tritt auf, wenn ein Attributwert aus der Bibliothek entfernt wird. | MediaCollectionAttributeStringRemoved-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 2f264416-0bc5-41d0-8863-32c284393082
keywords:
- MediaCollectionAttributeStringRemoved-Ereignis des AxWindowsMediaPlayer-Windows Media Player
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
ms.openlocfilehash: f56a6e997ada3296a0ec1df841797c1495ccde0864495dcf77a0a0634ccde5fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582076"
---
# <a name="mediacollectionattributestringremoved-event-of-the-axwindowsmediaplayer-object"></a>MediaCollectionAttributeStringRemoved-Ereignis des AxWindowsMediaPlayer-Objekts

Das MediaCollectionAttributeStringRemoved-Ereignis tritt auf, wenn ein Attributwert aus der Bibliothek entfernt wird.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEvent**, das die folgenden Eigenschaften im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft           | Beschreibung                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bstrAttribName** | System.String Gibt den Namen des Attributs an. Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attributreferenz.](attribute-reference.md)<br/> |
| bstrAttribVal      | System.String Gibt den Wert des Attributs an.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Hinweise

Wenn ein Medienelement aus der Bibliothek entfernt wird, werden seine Metadaten aus **der MediaCollection** entfernt, und dieses Ereignis wird für jedes entfernte Attribut ausgelöst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.mediaCollection (VB und C#)**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection-Schnittstelle (VB und C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





