---
title: IWMPControls3 getAudioLanguageID-Methode
description: Die getAudioLanguageID-Methode gibt den Locale Identifier (LCID) für einen angegebenen Audiosprachindex zurück.
ms.assetid: 880bbfca-6f69-41ce-a078-467c1939fae5
keywords:
- getAudioLanguageID-Windows Media Player
- getAudioLanguageID-Methode Windows Media Player , IWMPControls3-Schnittstelle
- IWMPControls3-Schnittstelle Windows Media Player , getAudioLanguageID-Methode
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e853d5a13c40316341c0759899e06e7292c006c00068a1b527e5035ff10422b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506210"
---
# <a name="iwmpcontrols3getaudiolanguageid-method"></a>IWMPControls3::getAudioLanguageID-Methode

Die **getAudioLanguageID-Methode** gibt den Locale Identifier (LCID) für einen angegebenen Audiosprachindex zurück.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 getAudioLanguageID(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageID( _
  ByVal lIndex As System.Int32 _
) As System.Int32
Implements IWMPControls3.getAudioLanguageID
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*lIndex* \[ In\]
</dt> <dd>

Ein **System.Int32,** das der einbasierte Index der Audiosprache ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System.Int32,** das die LCID ist.

## <a name="remarks"></a>Hinweise

Eine LCID identifiziert eindeutig einen bestimmten Sprachdialekt, der als "Locale" bezeichnet wird.

Für Windows Medienbasierte Inhalte unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzelne Ausgabe.

Verwenden Sie **die audioLanguageCount-Eigenschaft,** um die Anzahl der unterstützten Audiosprachen zu erhalten, und greifen Sie dann einzeln mithilfe eines einbasierten Indexes auf eine Audiosprache zu.

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

[**IWMPControls3.currentAudioLanguage (VB und C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.currentAudioLanguageIndex (VB und C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getAudioLanguageDescription (VB und C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getLanguageName (VB und C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





