---
title: CbruStStateChange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das CglühEndstateStateChange-Ereignis tritt auf, wenn ein CD-Vorgang den Zustand ändert.
ms.assetid: fec8a8e5-e282-454e-9713-fd9bb131df6a
keywords:
- CbruStStateChange-Ereignis des AxWindowsMediaPlayer-Windows Media Player
topic_type:
- apiref
api_name:
- CdromBurnStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a28a8dfad6e5d9bc7bb603632e2eb08ceb5810f9bf02f395d825fc2d7ac64c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055038"
---
# <a name="cdromburnstatechange-event-of-the-axwindowsmediaplayer-object"></a>CbruStStateChange-Ereignis des AxWindowsMediaPlayer-Objekts

Das CglühEndstateStateChange-Ereignis tritt auf, wenn ein CD-Vorgang den Zustand ändert.

``` syntax
[C#]
private void player_CdromBurnStateChange(
  object sender,
  _WMPOCXEvents_CdromBurnStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromBurnStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnStateChangeEvent
) Handles player.CdromBurnStateChange
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ C enumerationStateChangeEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ CladungsStateChangeEvent**, das die folgenden Eigenschaften im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft   | BESCHREIBUNG                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| pC wies | WMPLib.IWMPC wie Die Schnittstelle, die den Vorgang darstellt, der den Fehler ausgelöst hat.<br/> |
| wmpbs      | WMPLib.WMPMemberStateDer -Enumerationswert, der den neuen Zustand angibt.<br/>                         |



 

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

[**IWMPCführungsschnittstelle (VB und C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**WMP-Zustand**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





