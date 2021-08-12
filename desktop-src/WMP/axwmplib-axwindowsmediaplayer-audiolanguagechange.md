---
title: AudioLanguageChange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das AudioLanguageChange-Ereignis tritt auf, wenn sich die aktuelle Audiosprache ändert. | AudioLanguageChange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 35e4ff82-fc59-4d28-b7fc-1527fb46b960
keywords:
- AudioLanguageChange-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
topic_type:
- apiref
api_name:
- AudioLanguageChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40538dad18c4cb6767a034ab5d163f16d1822d9149e15c07ca1130f5eb17f30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582725"
---
# <a name="audiolanguagechange-event-of-the-axwindowsmediaplayer-object"></a>AudioLanguageChange-Ereignis des AxWindowsMediaPlayer-Objekts

Das AudioLanguageChange-Ereignis tritt auf, wenn sich die aktuelle Audiosprache ändert.

``` syntax
[C#]
private void player_AudioLanguageChange(
  object sender,
  _WMPOCXEvents_AudioLanguageChangeEvent e
)

[Visual Basic]
Private Sub player_AudioLanguageChange(
  sender As Object,
  e As _WMPOCXEvents_AudioLanguageChangeEvent
) Handles player.AudioLanguageChange
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ AudioLanguageChangeEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ AudioLanguageChangeEvent**, das die folgende Eigenschaft im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft   | BESCHREIBUNG                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| **Langid** | **System.Int32** Identifiziert eindeutig einen bestimmten Sprachdialekt, der als Gebietsschema bezeichnet wird.<br/> |



 

## <a name="remarks"></a>Hinweise

Ein Gebietsschemabezeichner (LCID) identifiziert eindeutig einen bestimmten Sprachdialekt, der als Gebietsschema bezeichnet wird.

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

[**IWMPControls3.currentAudioLanguage (VB und C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> </dl>

 

 





