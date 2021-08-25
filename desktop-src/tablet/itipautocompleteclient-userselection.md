---
description: Benachrichtigt den Eingabebereich, dass der Benutzer etwas in der AutoVervollständigen-Liste ausgewählt hat und den gesamten verbleibenden Text verwirft, der noch nicht eingefügt wurde.
ms.assetid: 2e6fabe1-7984-4908-bf90-0603d0dad268
title: ITipAutocompleteClient::UserSelection-Methode (TipAutoComplete.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UserSelection
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 2dac765c3f1c3e709bb7066a1645c2d77783ea555bccd81f9d5809da802d7043
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843480"
---
# <a name="itipautocompleteclientuserselection-method"></a>ITipAutocompleteClient::UserSelection-Methode

Benachrichtigt den Eingabebereich, dass der Benutzer etwas in der AutoVervollständigen-Liste ausgewählt hat und den gesamten verbleibenden Text verwirft, der noch nicht eingefügt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT UserSelection();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode wird vom Anbieter aufgerufen, um den Client darüber zu informieren, dass vom Benutzer eine Auswahl getroffen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                       |
| Header<br/>                   | <dl> <dt>TipAutoComplete.h (erfordert auch Peninputpanel \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITipAutocompleteClient-Schnittstelle**](itipautocompleteclient.md)
</dt> <dt>

[Referenz zum Texteingabebereich](text-input-panel-reference.md)
</dt> </dl>

 

 




