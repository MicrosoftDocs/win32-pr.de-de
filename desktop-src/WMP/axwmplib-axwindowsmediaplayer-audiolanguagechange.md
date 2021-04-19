---
title: Audiolanguagechange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das audiolanguagechange-Ereignis tritt auf, wenn sich die aktuelle Audiosprache ändert. | Audiolanguagechange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 35e4ff82-fc59-4d28-b7fc-1527fb46b960
keywords:
- Audiolanguagechange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
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
ms.openlocfilehash: 354a34f30df237827e3d369721963ec2c1797e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355252"
---
# <a name="audiolanguagechange-event-of-the-axwindowsmediaplayer-object"></a>Audiolanguagechange-Ereignis des AxWindowsMediaPlayer-Objekts

Das audiolanguagechange-Ereignis tritt auf, wenn sich die aktuelle Audiosprache ändert.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ audiolanguagechangeeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ audiolanguagechangeevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.



| Eigenschaft   | BESCHREIBUNG                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| **langID** | **System. Int32** Identifiziert eindeutig einen bestimmten Sprach Dialekt, der als Gebiets Schema bezeichnet wird.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Ein Gebiets Schema Bezeichner (Locale Identifier, LCID) identifiziert eindeutig einen bestimmten Sprach Dialekt, der als locale bezeichnet wird.

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

[**IWMPControls3. currentaudiolanguage (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> </dl>

 

 





