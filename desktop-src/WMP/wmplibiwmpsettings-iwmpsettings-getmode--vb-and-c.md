---
title: Iwmpsettings getMode-Methode
description: Die getMode-Methode gibt einen Wert zurück, der angibt, ob der Schleifen-oder Shuffle-Modus aktiv ist.
ms.assetid: a2e4bf74-017f-4c54-a3a1-a03b75a87a59
keywords:
- getMode-Methode, Windows-Media Player
- getMode-Methode, Windows Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings-Schnittstelle, Windows Media Player, getMode-Methode
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
ms.openlocfilehash: 229cacf629410f958a062615cd5feb22be2ab0d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359346"
---
# <a name="iwmpsettingsgetmode-method"></a>Iwmpsettings:: getMode-Methode

Die **getMode** -Methode gibt einen Wert zurück, der angibt, ob der Schleifen-oder Shuffle-Modus aktiv ist.

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

*bstraumode* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der einem der folgenden Werte entspricht.



| Wert      | BESCHREIBUNG                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| autorewind | Die Nachverfolgung wird von Anfang an neu gestartet.                                |
| loop       | Die Reihenfolge der Spuren wird wiederholt.                                                           |
| showframe  | Der nächste Keyframe wird angezeigt, wenn er nicht wiedergegeben wird. Dieser Modus ist für Audiospuren nicht relevant. |
| Shuffle    | Spuren werden in zufälliger Reihenfolge wiedergegeben.                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System. Boolean** -Wert, der angibt, ob der angegebene Modus aktiv ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpsettings-Schnittstelle (VB und c#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. SetMode (VB und c#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





