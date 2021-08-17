---
title: DurationUnitChange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das DurationUnitChange-Ereignis ist für die zukünftige Verwendung reserviert.
ms.assetid: d8d7da21-bc61-49f8-91bd-4c232295c1ac
keywords:
- DurationUnitChange-Ereignis des AxWindowsMediaPlayer-Windows Media Player
topic_type:
- apiref
api_name:
- DurationUnitChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1efa872389ad88a236808de64ed299dd3afc123cee59f39f1215f7a16bcb589f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136043"
---
# <a name="durationunitchange-event-of-the-axwindowsmediaplayer-object"></a>DurationUnitChange-Ereignis des AxWindowsMediaPlayer-Objekts

Das DurationUnitChange-Ereignis ist für die zukünftige Verwendung reserviert.

``` syntax
[C#]
private void player_DurationUnitChange(
  object sender,
  _WMPOCXEvents_DurationUnitChangeEvent e
)

[Visual Basic]
Private Sub player_DurationUnitChange(  
  sender As Object,  
  e As _WMPOCXEvents_DurationUnitChangeEvent
) Handles player.DurationUnitChange
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ DurationUnitChangeEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ DurationUnitChangeEvent**, die die folgende Eigenschaft im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft        | Beschreibung                               |
|-----------------|-------------------------------------------|
| newDurationUnit | **System.Int32** Nicht unterstützt.<br/> |



 

## <a name="remarks"></a>Hinweise

Dieses Ereignis ist für die zukünftige Verwendung reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





