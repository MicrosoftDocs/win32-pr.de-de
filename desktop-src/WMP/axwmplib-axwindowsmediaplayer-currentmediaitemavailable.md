---
title: Currentmediaitemavailable-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das currentmediaitemavailable-Ereignis tritt auf, wenn ein grafisches Metadatenelement im aktuellen Medien Element verfügbar wird. | Currentmediaitemavailable-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 7db62e6a-5f20-441a-801f-147ac386c5f8
keywords:
- Currentmediaitemavailable-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
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
ms.openlocfilehash: 547622424194e63733cec6166d813d42ebf577ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360991"
---
# <a name="currentmediaitemavailable-event-of-the-axwindowsmediaplayer-object"></a>Currentmediaitemavailable-Ereignis des AxWindowsMediaPlayer-Objekts

Das currentmediaitemavailable-Ereignis tritt auf, wenn ein grafisches Metadatenelement im aktuellen Medien Element verfügbar wird.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ currentmediaitemavailableeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ currentmediaitemavailableevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.



| Eigenschaft     | BESCHREIBUNG                                                 |
|--------------|-------------------------------------------------------------|
| bstritemname | System. stringder Name des aktuellen Medien Elements.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Da die Wiedergabe beginnen kann, bevor ein Medien Element vollständig heruntergeladen wird, sind alle im Medien Element enthaltenen metadatengrafiken (z. b. Albumcover Art) möglicherweise nicht verfügbar, wenn die Wiedergabe gestartet wird. Dieses Ereignis warnt Sie, wenn ein metadatengrafieelement den Download abgeschlossen hat. Sie können dann die **iwmpmedia** -Schnittstelle abrufen, indem Sie den Wert von **bstritemname** an die *iwmpmediacollection* übergeben. **getByName** -Methode, nach der Sie mithilfe von *IWMPMedia3* auf das metadatengrafieelement zugreifen können. **getItemInfoByType** und Angeben von **WM/Bild** für den Attributnamen.

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

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB und c#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[**Iwmpmediacollection. getByName (VB und c#)**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





