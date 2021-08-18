---
title: CurrentMediaItemAvailable-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das CurrentMediaItemAvailable-Ereignis tritt auf, wenn ein grafisches Metadatenelement im aktuellen Medienelement verfügbar wird. | CurrentMediaItemAvailable-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 7db62e6a-5f20-441a-801f-147ac386c5f8
keywords:
- CurrentMediaItemAvailable-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
topic_type:
- apiref
api_name:
- CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b5bbac6f27dfa7c9de1115eb3c2f5eea85096e0868ac17e0f8b11d81385f344
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582349"
---
# <a name="currentmediaitemavailable-event-of-the-axwindowsmediaplayer-object"></a>CurrentMediaItemAvailable-Ereignis des AxWindowsMediaPlayer-Objekts

Das CurrentMediaItemAvailable-Ereignis tritt auf, wenn ein grafisches Metadatenelement im aktuellen Medienelement verfügbar wird.

``` syntax
[C#]
private void player_CurrentMediaItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentMediaItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentMediaItemAvailable(
  sender As Object,  
  e As _WMPOCXEvents_CurrentMediaItemAvailableEvent
) Handles player.CurrentMediaItemAvailable
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEvent**, das die folgende Eigenschaft im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft     | BESCHREIBUNG                                                 |
|--------------|-------------------------------------------------------------|
| bstrItemName | System.StringDer Name des aktuellen Medienelements.<br/> |



 

## <a name="remarks"></a>Hinweise

Da die Wiedergabe beginnen kann, bevor ein Medienelement vollständig heruntergeladen wird, sind metadatengrafiken, die im Medienelement enthalten sind (z. B. Album cover art), möglicherweise nicht verfügbar, wenn es mit der Wiedergabe beginnt. Dieses Ereignis warnt Sie, wenn das Herunterladen eines Metadatengrafikelements abgeschlossen ist. Sie können dann die **IWMPMedia-Schnittstelle** abrufen, indem Sie den Wert von **bstrItemName** an die *IWMPMediaCollection* übergeben. **getByName-Methode,** nach der Sie mithilfe von *IWMPMedia3* auf das Metadatengrafikelement zugreifen können. **getItemInfoByType** und Angeben von **WM/Picture** für den Attributnamen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player Serie 9 oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3.getItemInfoByType (VB und C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection.getByName (VB und C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





