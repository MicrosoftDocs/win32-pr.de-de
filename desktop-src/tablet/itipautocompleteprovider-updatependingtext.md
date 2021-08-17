---
description: Wird vom Client für die automatische Vervollständigung verwendet, um die Anwendung über den Text zu informieren, den ein Benutzer in den Eingabebereich eingegeben hat.
ms.assetid: 68413836-321a-4e75-8538-c5a8fc577c0f
title: ITipAutocompleteProvider::UpdatePendingText-Methode (TipAutoComplete.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.UpdatePendingText
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 99fc67b5ba6495e2bdfb8a54de2412ca01cbdd37475d08d20d227b203f2da1bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716430"
---
# <a name="itipautocompleteproviderupdatependingtext-method"></a>ITipAutocompleteProvider::UpdatePendingText-Methode

Wird vom Client für die automatische Vervollständigung verwendet, um die Anwendung über den Text zu informieren, den ein Benutzer in den Eingabebereich eingegeben hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT UpdatePendingText(
  [in] BSTR bstrPendingText
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrPendingText* \[ In\]
</dt> <dd>

Quelltext, der zum Generieren der Automatischen Vervollständigungsliste verwendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Hinweise

Dieser Text enthält nicht den Text, der bereits in das Fokussierte Feld eingefügt wurde. Der Anbieter für die automatische Vervollständigung ist dafür verantwortlich, den aktuellen Feldtext und die Auswahl zum Generieren der Automatischen Vervollständigungsliste zu berücksichtigen. Wenn *bstrPendingText* **NULL** ist, wird die Liste für die automatische Vervollständigung mit dem aktuellen Text links neben der Auswahl im Feld generiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                       |
| Header<br/>                   | <dl> <dt>TipAutoComplete.h (erfordert auch Peninputpanel \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITipAutocompleteProvider-Schnittstelle**](itipautocompleteprovider.md)
</dt> <dt>

[Referenz zum Texteingabebereich](text-input-panel-reference.md)
</dt> </dl>

 

 




