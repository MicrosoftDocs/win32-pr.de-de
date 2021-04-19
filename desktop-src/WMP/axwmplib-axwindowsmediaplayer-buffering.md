---
title: Bufferingereignis des AxWindowsMediaPlayer-Objekts
description: Das bufferingereignis tritt auf, wenn das Windows Media Player-Steuerelement die Pufferung oder den Download beendet. | Bufferingereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: ad152c4d-1c91-4da1-bec0-46f89f3b8c79
keywords:
- Bufferingereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- Buffering Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af595443d78a311510df6a7e06b2e716da22ecae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367511"
---
# <a name="buffering-event-of-the-axwindowsmediaplayer-object"></a>Bufferingereignis des AxWindowsMediaPlayer-Objekts

Das bufferingereignis tritt auf, wenn das Windows Media Player-Steuerelement die Pufferung oder den Download beendet.

``` syntax
[C#]
private void player_Buffering(
  object sender,
  _WMPOCXEvents_BufferingEvent e
)

[Visual Basic]
Private Sub player_Buffering(
  sender As Object,
  e As _WMPOCXEvents_BufferingEvent
) Handles player.Buffering
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ bufferingeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ bufferingevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.



| Eigenschaft | BESCHREIBUNG                                                                                                                                                         |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Start    | System. booleangibt an, ob die Pufferung gestartet oder beendet wurde. Der Wert true gibt an, dass er begonnen hat. der Wert false gibt an, dass er beendet wurde.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses Ereignis, um zu bestimmen, wann ein-oder herunterladen gestartet oder beendet wird. Sie können den gleichen Ereignisblock für beide Fälle verwenden und *iwmpnetwork* testen. **BufferingProgress** und *iwmpnetwork*. **Download Progress** , um zu bestimmen, ob der Inhalt von Windows Media Player derzeit gepuffert oder heruntergeladen wird.

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

[**Iwmpnetwork. BufferingProgress (VB und c#)**](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)
</dt> <dt>

[**Iwmpnetwork. Download Progress (VB und c#)**](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)
</dt> </dl>

 

 





