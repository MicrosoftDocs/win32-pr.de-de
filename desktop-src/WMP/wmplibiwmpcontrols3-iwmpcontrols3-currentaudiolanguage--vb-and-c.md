---
title: IWMPControls3 currentAudioLanguage-Eigenschaft
description: Die currentAudioLanguage-Eigenschaft ruft den Gebietsschemabezeichner (LCID) der Audiosprache für die Wiedergabe ab oder legt diese fest.
ms.assetid: 4adf26c7-077a-483e-8a76-accf871eca4c
keywords:
- currentAudioLanguage-Eigenschaft Windows Media Player
- currentAudioLanguage-Eigenschaft Windows Media Player , IWMPControls3-Schnittstelle
- IWMPControls3-Schnittstelle Windows Media Player , currentAudioLanguage-Eigenschaft
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
ms.openlocfilehash: 1e1a4f668cec560528270d52a2abe4777ce32d3ceb38ce21345342ef87866c38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115877"
---
# <a name="iwmpcontrols3currentaudiolanguage-property"></a>IWMPControls3::currentAudioLanguage-Eigenschaft

Die **currentAudioLanguage-Eigenschaft** ruft den Gebietsschemabezeichner (LCID) der Audiosprache für die Wiedergabe ab oder legt diese fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 currentAudioLanguage {get; set;}
```


```VB

Public Property currentAudioLanguage As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Eine **System.Int32-Datei,** die die LCID der Audiosprache ist.

## <a name="remarks"></a>Hinweise

Eine LCID identifiziert eindeutig einen bestimmten Sprachdialekt, der als Gebietsschema bezeichnet wird.

Für Windows medienbasierten Inhalt unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzelne Ausgabe.

Wenn Sie mit DVD-Inhalten arbeiten, führt die Angabe einer LCID dazu, dass die erste verfügbare Audiospur mit der angegebenen Sprach-ID ausgewählt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPControls3-Schnittstelle (VB und C#)**](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.audioLanguageCount (VB und C#)**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.currentAudioLanguageIndex (VB und C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getAudioLanguageDescription (VB und C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getAudioLanguageID (VB und C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getLanguageName (VB und C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





