---
title: IWMPDVD.isAvailable (VB und C )
description: Die isAvailable-Eigenschaft (die get isAvailable-Methode in C\ ) ruft einen Wert ab, der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine angegebene \_ Aktion ausgeführt werden kann.
ms.assetid: 55690783-df2f-473d-a6f2-a4907b7e8a78
keywords:
- IWMPDVD.isAvailable (VB und C ) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPDVD.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78c9dda7bff764752dc55524000ccd3695863afe69dcf45c2ed971c9c0373fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415918"
---
# <a name="iwmpdvdisavailable-vb-and-c"></a>IWMPDVD.isAvailable (VB und C#)

Die **isAvailable-Eigenschaft** (die **get \_ isAvailable-Methode** in C#) ruft einen Wert ab, der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine angegebene Aktion ausgeführt werden kann.


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
)
```



## <a name="parameters"></a>Parameter

*bstrItem*

Eine System.String, bei der es sich um einen der folgenden Werte handelt.



| Wert      | Beschreibung                                                                                   |
|------------|-----------------------------------------------------------------------------------------------|
| back (Zurück)       | Hier wird festgestellt, ob **die IWMPDVD.back-Methode** verfügbar ist.                                   |
| Dvd        | Hier wird festgestellt, ob die DVD geladen ist.                                                          |
| dvdDecoder | Hier wird festgestellt, ob der DVD-Decoder auf dem System installiert ist.                                     |
| resume     | Hier wird festgestellt, ob **die IWMPDVD.resume-Methode** verfügbar ist.                                 |
| titleMenu  | Hier wird festgestellt, **ob die IWMPDVD.titleMenu-Methode** verfügbar ist.                              |
| topMenu    | Hier wird festgestellt, **ob die IWMPDVD.topMenu-Methode** verfügbar ist. Wird häufig als Stammmenü bezeichnet. |



 

## <a name="property-value"></a>Eigenschaftswert

**System.Boolean**

Ein **system.boolesscher Wert,** der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine angegebene Aktion ausgeführt werden kann.

## <a name="remarks"></a>Hinweise

Die DVD-Features Windows Media Player funktionieren nicht auf Computern, auf denen kein DVD-Decoder installiert ist. Sie können ermitteln, ob ein Decoder verfügbar ist, indem Sie die **isAvailable-Eigenschaft** aufrufen (die **get \_ isAvailable-Methode** in C#) und den **System.String-Wert** "dvdDecoder" übergeben.

Jede DVD wird anders verfasst. Welche Methoden während der Wiedergabe und Navigation der DVD verfügbar sind, hängt davon ab, wie die DVD verfasst wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IWMPDVD-Schnittstelle (VB und C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPDVD.back (VB und C#)**](wmplibiwmpdvd-iwmpdvd-back--vb-and-c.md)
</dt> <dt>

[**IWMPDVD.resume (VB und C#)**](wmplibiwmpdvd-iwmpdvd-resume--vb-and-c.md)
</dt> <dt>

[**IWMPDVD.titleMenu (VB und C#)**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> <dt>

[**IWMPDVD.topMenu (VB und C#)**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





