---
title: Disconnect-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das Disconnect-Ereignis ist für die zukünftige Verwendung reserviert.
ms.assetid: 3baecc6c-e772-4269-96c1-900be270543e
keywords:
- Disconnect-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- Disconnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dffe3191efeddba74eb22c7c5c72b8c52bc095
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358275"
---
# <a name="disconnect-event-of-the-axwindowsmediaplayer-object"></a>Disconnect-Ereignis des AxWindowsMediaPlayer-Objekts

Das Disconnect-Ereignis ist für die zukünftige Verwendung reserviert.

``` syntax
[C#]
private void player_Disconnect(
  object sender,
  _WMPOCXEvents_DisconnectEvent e
)

[Visual Basic]
Private Sub player_Disconnect(  
  sender As Object,
  e As _WMPOCXEvents_DisconnectEvent
) Handles player.Disconnect
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ disconnecteventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ disconnectevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.



| Eigenschaft | BESCHREIBUNG                               |
|----------|-------------------------------------------|
| result   | **System. Int32** Nicht unterstützt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis ist für die zukünftige Verwendung reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





