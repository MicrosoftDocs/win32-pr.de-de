---
description: Hiermit wird die Liste der Auto Vervollständigen angezeigt oder ausgeblendet.
ms.assetid: 756ffa3d-03ee-4753-a826-3bc22ab16f5f
title: 'Itipaudecompleteprovider:: Show-Methode (tipaudecomplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.Show
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 950358ae28d1cb68af803ed6b7f520f1bbad8c03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759816"
---
# <a name="itipautocompleteprovidershow-method"></a>Itipaudecompleteprovider:: Show-Methode

Hiermit wird die Liste der Auto Vervollständigen angezeigt oder ausgeblendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT Show(
  [in] BOOL fShow
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

mit der Bezeichnung  \[ in\]
</dt> <dd>

**True** , um die Benutzeroberfläche für die automatische Vervollständigung anzuzeigen, **false** , um die Benutzeroberfläche für die automatische Vervollständigung zu blenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode wird vom Client aufgerufen, um die Auto Vervollständigen-Liste anzuzeigen oder auszublenden. Wenn die Auto Vervollständigen-Liste nicht angezeigt wird  und der Ausdruck **false** ist, führt diese Methode keine Aktion aus. Wenn die Auto Vervollständigen-Liste angezeigt wird und die Angabe von " *f* " **true** ist, führt diese Methode keine Aktion aus.

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

 

 




