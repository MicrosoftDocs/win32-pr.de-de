---
title: Cdrommediachange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das cdrommediachange-Ereignis tritt auf, wenn eine CD oder eine DVD in ein CD-oder DVD-Laufwerk eingefügt oder daraus entfernt wird. | Cdrommediachange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 0a6378c1-59e4-4be3-8764-d5c4ab478b6c
keywords:
- Cdrommediachange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- CdromMediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35385541f6bc91b6935f148fd8ae28df6a415f3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353415"
---
# <a name="cdrommediachange-event-of-the-axwindowsmediaplayer-object"></a>Cdrommediachange-Ereignis des AxWindowsMediaPlayer-Objekts

Das **cdrommediachange** -Ereignis tritt auf, wenn eine CD oder eine DVD in ein CD-oder DVD-Laufwerk eingefügt oder daraus entfernt wird.

``` syntax
[C#]
private void player_CdromMediaChange(
  object sender,
  _WMPOCXEvents_CdromMediaChangeEvent e
)

[Visual Basic]
Private Sub player_CdromMediaChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromMediaChangeEvent
) Handles player.CdromMediaChange
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdrommediachangeeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ cdrommediachangeevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.



| Eigenschaft | BESCHREIBUNG                                                        |
|----------|--------------------------------------------------------------------|
| Cdromnum | System. Int32Specifies der Index des CD-oder DVD-Laufwerks.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Index des CD-Laufwerks entspricht dem Index einer iwmpcdrom-Schnittstelle, auf die über die iwmpcdromcollection-Schnittstelle zugegriffen werden kann.

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

[**Iwmpcdrom-Schnittstelle (VB und c#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**Iwmpcdromcollection-Schnittstelle (VB und c#)**](iwmpcdromcollection--vb-and-c.md)
</dt> </dl>

 

 





