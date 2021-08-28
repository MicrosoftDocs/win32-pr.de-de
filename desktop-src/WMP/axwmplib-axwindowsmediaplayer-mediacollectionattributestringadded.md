---
title: MediaCollectionAttributeStringAdded-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das MediaCollectionAttributeStringAdded-Ereignis tritt auf, wenn der Bibliothek ein Attributwert hinzugefügt wird. | MediaCollectionAttributeStringAdded-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: b14db0ce-bd78-4e28-a42c-1a231c29da2b
keywords:
- MediaCollectionAttributeStringAdded-Ereignis des AxWindowsMediaPlayer-Windows Media Player
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
ms.openlocfilehash: 95d0612e18256f81529a8ad703ecf887ba5976ea9913e46598bc5a0fd44a903e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123940"
---
# <a name="mediacollectionattributestringadded-event-of-the-axwindowsmediaplayer-object"></a>MediaCollectionAttributeStringAdded-Ereignis des AxWindowsMediaPlayer-Objekts

Das MediaCollectionAttributeStringAdded-Ereignis tritt auf, wenn der Bibliothek ein Attributwert hinzugefügt wird.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringAddedEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringAddedEvent**, das die folgenden Eigenschaften im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft           | Beschreibung                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bstrAttribName** | System.String Gibt den Namen des Attributs an. Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attributreferenz.](attribute-reference.md)<br/> |
| bstrAttribVal      | System.StringSpecifisiert den Wert des Attributs.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Hinweise

Wenn der Bibliothek ein Medienelement hinzugefügt wird, werden seine Metadaten der Mediensammlung hinzugefügt, und dieses Ereignis wird für jedes hinzugefügte Attribut ausgelöst.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
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

 

 





