---
title: AxWindowsMediaPlayer. newmedia-Methode
description: Die newmedia-Methode gibt eine iwmpmedia-Schnittstelle für ein neues Medien Element zurück.
ms.assetid: d10a517e-b4da-4f0b-9d51-9d387578d7dd
keywords:
- newmedia-Methode, Windows-Media Player
- newmedia-Methode, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, newmedia-Methode
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
ms.openlocfilehash: 093a4e2b8181aac9148686108ad2c5c318a4d0cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365492"
---
# <a name="axwindowsmediaplayernewmedia-method"></a>AxWindowsMediaPlayer. newmedia-Methode

Die newmedia-Methode gibt eine iwmpmedia-Schnittstelle für ein neues Medien Element zurück.

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

Ein **System. String** -Wert, der die URL der digitalen Mediendatei ist, die zum Initialisieren des neuen Medien Elements verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine WMPLib. iwmpmedia-Schnittstelle, die das neu erstellte Medien Element darstellt.

## <a name="remarks"></a>Bemerkungen

Der *bstrinurl* -Parameter darf keine Zeichenfolge der Länge 0 ("") oder NULL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





