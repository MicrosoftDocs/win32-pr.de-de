---
title: Iwmpsettings setmode-Methode
description: Die setmode-Methode legt den Schleifen Modus oder den Shuffle-Modus auf aktiv oder inaktiv fest.
ms.assetid: e9d3765e-6edb-47a5-ac97-5e00b62498c2
keywords:
- setmode-Methode, Windows-Media Player
- setmode-Methode, Windows Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings-Schnittstelle, Windows Media Player, setmode-Methode
topic_type:
- apiref
api_name:
- IWMPSettings.setMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dffede5e634c5c4f726cff1631b79781ed5179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365394"
---
# <a name="iwmpsettingssetmode-method"></a>Iwmpsettings:: setmode-Methode

Die **setmode** -Methode legt den Schleifen Modus oder den Shuffle-Modus auf aktiv oder inaktiv fest.

## <a name="syntax"></a>Syntax


```CSharp
public void setMode(
  System.String bstrMode,
  System.Boolean varfMode
);
```


```VB

Public Sub setMode( _
  ByVal bstrMode As System.String, _
  ByVal varfMode As System.Boolean _
)
Implements IWMPSettings.setMode
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstraumode* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der der Name des geänderten Modus ist, der einen der folgenden Werte enthält.



| Wert      | BESCHREIBUNG                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| autorewind | Die Nachverfolgung wird von Anfang an neu gestartet.                                |
| loop       | Die Reihenfolge der Spuren wird wiederholt.                                                           |
| showframe  | Der nächste Keyframe wird angezeigt, wenn er nicht wiedergegeben wird. Dieser Modus ist für Audiospuren nicht relevant. |
| Shuffle    | Spuren werden in zufälliger Reihenfolge wiedergegeben.                                                               |



 

</dd> <dt>

*varf-Modus* \[ in\]
</dt> <dd>

Ein **System. Boolean** -Wert, der angibt, ob der neue angegebene Modus aktiv ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der showframe-Modus aktiv ist, muss Windows Media Player auf den Inhalt der Nachverfolgung zugreifen, um den Videoframe abzurufen. Verwenden Sie diesen Modus bei der Wiedergabe von Inhalten, die nicht lokal sind, vorsichtig.

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

[**Iwmpsettings. getMode (VB und c#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> </dl>

 

 





