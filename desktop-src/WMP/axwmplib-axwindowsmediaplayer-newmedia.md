---
title: AxWindowsMediaPlayer.newMedia-Methode
description: Die newMedia-Methode gibt eine IWMPMedia-Schnittstelle für ein neues Medienelement zurück.
ms.assetid: d10a517e-b4da-4f0b-9d51-9d387578d7dd
keywords:
- newMedia-Windows Media Player
- newMedia-Windows Media Player , AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse Windows Media Player , newMedia-Methode
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdde19a6cb5da5113cb580c1916052c7ae0d38756bbc120368ffdfd464105591
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618740"
---
# <a name="axwindowsmediaplayernewmedia-method"></a>AxWindowsMediaPlayer.newMedia-Methode

Die newMedia-Methode gibt eine IWMPMedia-Schnittstelle für ein neues Medienelement zurück.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPMedia newMedia(
  System.String bstrURL
);
```


```VB

Public Function newMedia( _
  ByVal bstrURL As System.String _
) As IWMPMedia
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrURL* 
</dt> <dd>

Eine **System.String,die** die URL der digitalen Mediendatei ist, die zum Initialisieren des neuen Medienelements verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine WMPLib.IWMPMedia-Schnittstelle, die das neu erstellte Medienelement darstellt.

## <a name="remarks"></a>Hinweise

Der *bstrURL-Parameter* darf keine Zeichenfolge der Länge 0 (null) ("") oder NULL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





