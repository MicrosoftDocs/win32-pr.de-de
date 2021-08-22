---
title: IWMPSettings setMode-Methode
description: Die setMode-Methode legt den Schleifenmodus oder Shufflemodus auf aktiv oder inaktiv fest.
ms.assetid: e9d3765e-6edb-47a5-ac97-5e00b62498c2
keywords:
- setMode-Methode Windows Media Player
- setMode-Methode Windows Media Player , IWMPSettings-Schnittstelle
- IWMPSettings-Schnittstelle Windows Media Player , setMode-Methode
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
ms.openlocfilehash: 529aadf412cdae869ae3c308d82dcd08a7dfd581aeb7ecc711052f6acd54b962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568407"
---
# <a name="iwmpsettingssetmode-method"></a>IWMPSettings::setMode-Methode

Die **setMode-Methode** legt den Schleifenmodus oder Shufflemodus auf aktiv oder inaktiv fest.

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

*bstrMode* \[ In\]
</dt> <dd>

Eine **System.String-** mit dem Namen des modus, der geändert wird und einen der folgenden Werte enthält.



| Wert      | Beschreibung                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| autoRewind | Spuren werden von Anfang an neu gestartet, nachdem sie bis zum Ende wiedergegeben wurden.                                |
| loop       | Die Sequenz von Spuren wiederholt sich selbst.                                                           |
| showFrame  | Der nächstgelegene Keyframe wird angezeigt, wenn er nicht wiedergegeben wird. Dieser Modus ist für Audiospuren nicht relevant. |
| Shuffle    | Spuren werden in zufälliger Reihenfolge wiedergegeben.                                                               |



 

</dd> <dt>

*varfMode* \[ In\]
</dt> <dd>

Ein **System.Boolean-Wert,** der angibt, ob der neue angegebene Modus aktiv ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn der ShowFrame-Modus aktiv ist, müssen Windows Media Player auf den Trackinhalt zugreifen, um den Videoframe abzurufen. Verwenden Sie diesen Modus vorsichtig, wenn Sie Inhalte wiedergeben, die nicht lokal sind.

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

[**IWMPSettings.getMode (VB und C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> </dl>

 

 





