---
title: ComeRipMediaError-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das CiererRipMediaError-Ereignis tritt auf, wenn beim Berieren einer einzelnen Spur von einer CD ein Fehler auftritt.
ms.assetid: 542d0184-d893-4b98-903e-339909276fd6
keywords:
- ComeRipMediaError-Ereignis des AxWindowsMediaPlayer-Windows Media Player
topic_type:
- apiref
api_name:
- CdromRipMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea2be1f777c4af3385e41939743bb91a20d3d7094f1a38917b3e79686b2a2863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136183"
---
# <a name="cdromripmediaerror-event-of-the-axwindowsmediaplayer-object"></a>ComeRipMediaError-Ereignis des AxWindowsMediaPlayer-Objekts

Das CiererRipMediaError-Ereignis tritt auf, wenn beim Berieren einer einzelnen Spur von einer CD ein Fehler auftritt.

``` syntax
[C#]
private void player_CdromRipMediaError(
  object sender,
  _WMPOCXEvents_CdromRipMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromRipMediaError( 
  sender As Object,
  e As _WMPOCXEvents_CdromRipMediaErrorEvent
) Handles player.CdromRipMediaError
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ ComeRipMediaErrorEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ ComeRipMediaErrorEvent**, das die folgenden Eigenschaften im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft  | Beschreibung                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| pCiererRip | WMPLib.IWMPCiererRipDie Schnittstelle, die den Löschvorgang darstellt, der den Fehler ausgelöst hat.<br/>                |
| pMedia    | System.ObjectDas Medienelement, das den Fehler ausgelöst hat. Sie können dies in eine IWMPMedia-Schnittstelle um casten, um darauf zu zugreifen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11<br/>                                                                                         |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPCiererRip-Schnittstelle (VB und C#)**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





