---
description: Hebt die Registrierung des zugeordneten Anbieters auf.
ms.assetid: b5edc33d-dfd0-4350-b8cd-eaa30b726771
title: 'Itipaudecompleteclient:: unadviseprovider-Methode (tipaudecomplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.UnadviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 1100ebb700ef2fb769a13f9b62aacf5c1d007e0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865820"
---
# <a name="itipautocompleteclientunadviseprovider-method"></a>Itipaudecompleteclient:: unadviseprovider-Methode

Hebt die Registrierung des zugeordneten Anbieters auf.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnadviseProvider(
  [in] HWND                   hWndField,
  [in] ITipAutocompleProvider *pIACProvider
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndfield* \[ in\]
</dt> <dd>

Fenster Handle des Felds, das die Funktion für automatisches Vervollständigen bereitstellt.

</dd> <dt>

*piacprovider* \[ in\]
</dt> <dd>

Der Schnittstellen Zeiger auf die Auto Vervollständigen-Anbieter Schnittstelle, deren Registrierung aufgehoben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                       |
| Header<br/>                   | <dl> <dt>Tipautocomplete. h (erfordert auch "pinputpanel \_ i. c")</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itipauwebcompleteclient-Schnittstelle**](itipautocompleteclient.md)
</dt> <dt>

[Verweis auf Text Eingabe Panel](text-input-panel-reference.md)
</dt> </dl>

 

 




