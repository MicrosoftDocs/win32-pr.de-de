---
title: IWMPSettings getMode-Methode
description: Die getMode-Methode gibt einen Wert zurück, der angibt, ob der Schleifenmodus oder der Shufflemodus aktiv ist.
ms.assetid: a2e4bf74-017f-4c54-a3a1-a03b75a87a59
keywords:
- getMode-Methode Windows Media Player
- getMode-Methode Windows Media Player , IWMPSettings-Schnittstelle
- IWMPSettings-Schnittstelle Windows Media Player , getMode-Methode
topic_type:
- apiref
api_name:
- IWMPSettings.getMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fae5d910dbbdf1fc2241a63dcf6c61c94e968cf0f2b36316407aafc8fc5f2dcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119246300"
---
# <a name="iwmpsettingsgetmode-method"></a>IWMPSettings::getMode-Methode

Die **getMode-Methode** gibt einen Wert zurück, der angibt, ob der Schleifenmodus oder der Shufflemodus aktiv ist.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean getMode(
  System.String bstrMode
);
```


```VB

Public Function getMode( _
  ByVal bstrMode As System.String _
) As System.Boolean
Implements IWMPSettings.getMode
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrMode* \[ In\]
</dt> <dd>

Eine **System.String,die** einer der folgenden Werte ist.



| Wert      | BESCHREIBUNG                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| autoRewind | Spuren werden von Anfang an neu gestartet, nachdem sie bis zum Ende wiedergegeben wurden.                                |
| loop       | Die Sequenz von Spuren wiederholt sich selbst.                                                           |
| showFrame  | Der nächstgelegene Keyframe wird angezeigt, wenn er nicht wiedergegeben wird. Dieser Modus ist für Audiospuren nicht relevant. |
| Shuffle    | Spuren werden in zufälliger Reihenfolge wiedergegeben.                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System.Boolean-Wert,** der angibt, ob der angegebene Modus aktiv ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPSettings-Schnittstelle (VB und C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.setMode (VB und C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





