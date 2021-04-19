---
title: IWMPControls3 currentaudiolanguage (Eigenschaft)
description: Die currentaudiolanguage-Eigenschaft ruft den Gebiets Schema Bezeichner (LCID) der Audiosprache für die Wiedergabe ab oder legt ihn fest.
ms.assetid: 4adf26c7-077a-483e-8a76-accf871eca4c
keywords:
- currentaudiolanguage-Eigenschaft, Windows Media Player
- currentaudiolanguage-Eigenschaft, Windows Media Player, IWMPControls3-Schnittstelle
- IWMPControls3 Interface Windows Media Player, currentaudiolanguage-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c4621b5eace56cb883a6c8b14c3b1f082b12d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367794"
---
# <a name="iwmpcontrols3currentaudiolanguage-property"></a>IWMPControls3:: currentaudiolanguage (Eigenschaft)

Die **currentaudiolanguage** -Eigenschaft ruft den Gebiets Schema Bezeichner (LCID) der Audiosprache für die Wiedergabe ab oder legt ihn fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 currentAudioLanguage {get; set;}
```


```VB

Public Property currentAudioLanguage As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der die LCID der Audiosprache ist.

## <a name="remarks"></a>Bemerkungen

Eine LCID identifiziert eindeutig einen bestimmten Sprach Dialekt, der als Gebiets Schema bezeichnet wird.

Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzige Ausgabe.

Beim Arbeiten mit DVD-Inhalten bewirkt die Angabe einer LCID, dass die erste verfügbare Audiospur mit der angegebenen Sprach-ID ausgewählt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPControls3-Schnittstelle (VB und c#)**](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. audiolanguagecount (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentaudiolanguageindex (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getaudiolanguagedescription (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getaudiolanguageid (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getlanguagename (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





