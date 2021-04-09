---
description: Wird vom Auto Vervollständigen-Client verwendet, um die Anwendung über den Text zu benachrichtigen, den ein Benutzer in den Eingabebereich eingegeben hat.
ms.assetid: 68413836-321a-4e75-8538-c5a8fc577c0f
title: 'Itipaudecompleteprovider:: updatependingtext-Methode (tipaudecomplete. h)'
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
ms.openlocfilehash: 5c66e625639aa7088b1b3934a2f984d0f4097536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050580"
---
# <a name="itipautocompleteproviderupdatependingtext-method"></a>Itipaudecompleteprovider:: updatependingtext-Methode

Wird vom Auto Vervollständigen-Client verwendet, um die Anwendung über den Text zu benachrichtigen, den ein Benutzer in den Eingabebereich eingegeben hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT UpdatePendingText(
  [in] BSTR bstrPendingText
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstraupdingtext* \[ in\]
</dt> <dd>

Quelltext, der zum Generieren der Auto Vervollständigen-Liste verwendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Dieser Text enthält nicht den Text, der bereits in das fokussierte Feld eingefügt wurde. Der Anbieter für automatische Vervollständigung ist dafür verantwortlich, den aktuellen Feldtext und die Auswahl zum Generieren der Auto Vervollständigen-Liste zu berücksichtigen. Wenn *bstrautzdingtext* **null** ist, wird die Auto Vervollständigen-Liste mit dem aktuellen Text auf der linken Seite der Auswahl im Feld generiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                       |
| Header<br/>                   | <dl> <dt>Tipautocomplete. h (erfordert auch "pinputpanel \_ i. c")</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itipauescompleteprovider-Schnittstelle**](itipautocompleteprovider.md)
</dt> <dt>

[Verweis auf Text Eingabe Panel](text-input-panel-reference.md)
</dt> </dl>

 

 




