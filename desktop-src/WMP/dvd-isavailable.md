---
title: DVD. IsAvailable
description: Die IsAvailable-Eigenschaft gibt an, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann. | DVD. IsAvailable
ms.assetid: ed34a943-b9c3-40a8-8845-b83f16951a3e
keywords:
- DVD. IsAvailable-Windows-Media Player
topic_type:
- apiref
api_name:
- DVD.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5088b4b6365dd60d859fda8ec563cc9c8ff8a4c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366404"
---
# <a name="dvdisavailable"></a>DVD. IsAvailable

Die **IsAvailable** -Eigenschaft gibt an, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann.

``` syntax
player.dvd.isAvailable(
        name
        )
```

## <a name="parameters"></a>Parameter

*name*

Eine **Zeichenfolge** , die einen der folgenden Werte enthält.



| Zeichenfolge     | Beschreibung                                                                            |
|------------|----------------------------------------------------------------------------------------|
| back (Zurück)       | Bestimmt, ob die **Back** -Methode verfügbar ist.                                   |
| DVD        | Bestimmt, ob die DVD geladen wird.                                                  |
| dvddecoder | Bestimmt, ob der DVD-Decoder auf dem System installiert ist.                             |
| resume     | Bestimmt, ob die **Resume** -Methode verfügbar ist.                                 |
| titlemenu  | Bestimmt, ob die **titlemenu** -Methode verfügbar ist.                              |
| topmenu    | Bestimmt, ob die **topmenu** -Methode verfügbar ist. Wird üblicherweise als Stamm Menü bezeichnet. |



 

## <a name="return-values"></a>Rückgabewerte

Diese Methode gibt einen schreibgeschützten **booleschen** Wert zurück, der angibt, ob der angegebene Parameter verfügbar ist.

## <a name="remarks"></a>Bemerkungen

Die DVD-Features von Windows Media Player können nicht auf Computern verwendet werden, auf denen keine DVD-Decoder von Drittanbietern installiert sind. Sie können bestimmen, ob ein Decoder verfügbar ist, indem Sie **IsAvailable**("dvddecoder") aufrufen.

Jede DVD wird unterschiedlich verfasst. Die während der DVD-Wiedergabe und-Navigation verfügbaren Methoden hängen davon ab, wie die DVD erstellt wird.

**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer **false** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Version<br/>                  | Windows Media Player für Windows XP oder höher<br/>                            |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DVD-Objekt**](dvd-object.md)
</dt> </dl>

 

 





