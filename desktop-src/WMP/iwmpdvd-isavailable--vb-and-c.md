---
title: Iwmpdvd. IsAvailable (VB und C)
description: Die IsAvailable-Eigenschaft (die get \_ IsAvailable-Methode in C \) Ruft einen Wert ab, der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann.
ms.assetid: 55690783-df2f-473d-a6f2-a4907b7e8a78
keywords:
- Iwmpdvd. IsAvailable (VB und C) Windows Media Player
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
ms.openlocfilehash: 2e3409da619f337b61606baaf546cebbb438087c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365703"
---
# <a name="iwmpdvdisavailable-vb-and-c"></a>Iwmpdvd. IsAvailable (VB und c#)

Die **IsAvailable** -Eigenschaft (die **get \_ IsAvailable** -Methode in c#) Ruft einen Wert ab, der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann.


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

*bstritem*

Ein System. String-Wert, der einem der folgenden Werte entspricht.



| Wert      | BESCHREIBUNG                                                                                   |
|------------|-----------------------------------------------------------------------------------------------|
| back (Zurück)       | Ermittelt, ob die **iwmpdvd. Back** -Methode verfügbar ist.                                   |
| DVD        | Ermittelt, ob die DVD geladen wurde.                                                          |
| dvddecoder | Ermittelt, ob der DVD-Decoder auf dem System installiert ist.                                     |
| resume     | Ermittelt, ob die **iwmpdvd. Resume** -Methode verfügbar ist.                                 |
| titlemenu  | Ermittelt, ob die **iwmpdvd. titlemenu** -Methode verfügbar ist.                              |
| topmenu    | Ermittelt, ob die **iwmpdvd. topmenu** -Methode verfügbar ist. Wird üblicherweise als Stamm Menü bezeichnet. |



 

## <a name="property-value"></a>Eigenschaftswert

**System.Boolean**

Ein **System. boolescher** Wert, der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann.

## <a name="remarks"></a>Bemerkungen

Die DVD-Features von Windows Media Player können nicht auf Computern verwendet werden, auf denen kein DVD-Decoder installiert ist. Sie können bestimmen, ob ein Decoder verfügbar ist, indem Sie die **IsAvailable** -Eigenschaft (die **get \_ IsAvailable** -Methode in c#) aufrufen und den **System. String** -Wert "dvddecoder" übergeben.

Jede DVD wird unterschiedlich verfasst. Die während der DVD-Wiedergabe und-Navigation verfügbaren Methoden hängen davon ab, wie die DVD erstellt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpdvd-Schnittstelle (VB und c#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**Iwmpdvd. Back (VB und c#)**](wmplibiwmpdvd-iwmpdvd-back--vb-and-c.md)
</dt> <dt>

[**Iwmpdvd. Resume (VB und c#)**](wmplibiwmpdvd-iwmpdvd-resume--vb-and-c.md)
</dt> <dt>

[**Iwmpdvd. titlemenu (VB und c#)**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> <dt>

[**Iwmpdvd. topmenu (VB und c#)**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





