---
title: CmediaMediaChange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das C csvMediaChange-Ereignis tritt auf, wenn eine CD oder DVD in ein CD- oder DVD-Laufwerk eingefügt oder von einem CD- oder DVD-Laufwerk aus ihr eingefügt wird. | CmediaMediaChange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 0a6378c1-59e4-4be3-8764-d5c4ab478b6c
keywords:
- CorporaMediaChange-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
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
ms.openlocfilehash: 55dac05b3ca8a8675bfae431d3f2e8ffbb38db8701a2501fa80d282cd3c976ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055003"
---
# <a name="cdrommediachange-event-of-the-axwindowsmediaplayer-object"></a>CmediaMediaChange-Ereignis des AxWindowsMediaPlayer-Objekts

Das **C csvMediaChange-Ereignis** tritt auf, wenn eine CD oder DVD in ein CD- oder DVD-Laufwerk eingefügt oder von einem CD- oder DVD-Laufwerk aus ihr eingefügt wird.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ C csvMediaChangeEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ C csvMediaChangeEvent**, das die folgende Eigenschaft im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft | Beschreibung                                                        |
|----------|--------------------------------------------------------------------|
| CredoNum | System.Int32 Gibt den Index des CD- oder DVD-Laufwerks an.<br/> |



 

## <a name="remarks"></a>Hinweise

Der Index des CD-Laufwerks entspricht dem Index einer IWMPC interfaces-Schnittstelle, auf die über die IWMPCcollection-Schnittstelle zugegriffen werden kann.

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

[**IWMPCorpora-Schnittstelle (VB und C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPCcollectionCollection-Schnittstelle (VB und C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> </dl>

 

 





