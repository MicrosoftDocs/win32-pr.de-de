---
title: IWMPControls3 getLanguageName-Methode
description: Die getLanguageName-Methode gibt den Namen der Audiosprache mit dem angegebenen Gebietsschemabezeichner (LCID) zurück.
ms.assetid: a0651e8d-0ba1-4fff-93f0-fe097231723e
keywords:
- getLanguageName-Methode Windows Media Player
- getLanguageName-Methode Windows Media Player , IWMPControls3-Schnittstelle
- IWMPControls3-Schnittstelle Windows Media Player , getLanguageName-Methode
topic_type:
- apiref
api_name:
- IWMPControls3.getLanguageName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6850bd73c9add044bdb845d17341745c7546918f7824b611ed2f018f66139d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000490"
---
# <a name="iwmpcontrols3getlanguagename-method"></a>IWMPControls3::getLanguageName-Methode

Die **getLanguageName-Methode** gibt den Namen der Audiosprache mit dem angegebenen Gebietsschemabezeichner (LCID) zurück.

## <a name="syntax"></a>Syntax


```CSharp
public System.String getLanguageName(
  System.Int32 lLangID
);
```


```VB

Public Function getLanguageName( _
  ByVal lLangID As System.Int32 _
) As System.String
Implements IWMPControls3.getLanguageName
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*lLangID* \[ In\]
</dt> <dd>

Eine **System.Int32-Datei,** die die LCID ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **System.String,die** der Name der Audiosprache ist.

## <a name="remarks"></a>Hinweise

Eine LCID identifiziert eindeutig einen bestimmten Sprachdialekt, der als Gebietsschema bezeichnet wird.

Für Windows medienbasierten Inhalt unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzelne Ausgabe.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

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

[**IWMPControls3.getAudioLanguageID (VB und C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> </dl>

 

 





