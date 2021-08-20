---
title: IWMPControls3 getAudioLanguageDescription-Methode
description: Die getAudioLanguageDescription-Methode gibt die Beschreibung für die Audiosprache zurück, die dem angegebenen einbasierten Index entspricht.
ms.assetid: bf3db27f-ba14-409e-8942-fe863d6f3670
keywords:
- getAudioLanguageDescription-Methode Windows Media Player
- getAudioLanguageDescription-Methode Windows Media Player , IWMPControls3-Schnittstelle
- IWMPControls3-Schnittstelle Windows Media Player , getAudioLanguageDescription-Methode
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1172fd119671a8452ac581d3c3a27efd890456cec98f1ef8d6e61340a54c4404
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861870"
---
# <a name="iwmpcontrols3getaudiolanguagedescription-method"></a>IWMPControls3::getAudioLanguageDescription-Methode

Die **getAudioLanguageDescription-Methode** gibt die Beschreibung für die Audiosprache zurück, die dem angegebenen einbasierten Index entspricht.

## <a name="syntax"></a>Syntax


```CSharp
public System.String getAudioLanguageDescription(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageDescription( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPControls3.getAudioLanguageDescription
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*lIndex* \[ In\]
</dt> <dd>

Eine **System.Int32-Datei,** bei der es sich um den index der 1-basierten Audiosprache handelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **System.String,die** die Beschreibung der Audiosprache ist.

## <a name="remarks"></a>Hinweise

Für Windows Medienbasierte Inhalte unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzelne Ausgabe.

Verwenden Sie die **audioLanguageCount-Eigenschaft,** um die Anzahl der unterstützten Audiosprachen abzurufen, und greifen Sie dann mithilfe eines 1-basierten Indexes einzeln auf eine Audiosprache zu.

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

[**IWMPControls3.currentAudioLanguage (VB und C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getAudioLanguageID (VB und C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getLanguageName (VB und C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





