---
description: Registriert den Anbieter beim Client, damit der Client das Auto Vervollständigen-Anbieter Objekt der Anwendung abrufen kann.
ms.assetid: 7b761b30-66f7-454a-9e0d-f45c8099f19f
title: 'Itipaudecompleteclient:: adviseprovider-Methode (tipaudecomplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.AdviseProvider
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 9ef35ac730089403ac47c14421de96e75a022192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363531"
---
# <a name="itipautocompleteclientadviseprovider-method"></a>Itipaudecompleteclient:: adviseprovider-Methode

Registriert den Anbieter beim Client, damit der Client das Auto Vervollständigen-Anbieter Objekt der Anwendung abrufen kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT AdviseProvider(
  [in] HWND                     hWndField,
  [in] ITipAutocompleteProvider *pIACProvider
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndfield* \[ in\]
</dt> <dd>

Das Fenster Handle des Felds, das die Funktion für automatisches Vervollständigen bereitstellt.

</dd> <dt>

*piacprovider* \[ in\]
</dt> <dd>

Der Schnittstellen Zeiger auf die Auto Vervollständigen-Anbieter Schnittstelle.

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

[**Itipaudecompleteclient:: unadviseprovider-Methode**](itipautocompleteclient-unadviseprovider.md)
</dt> <dt>

[Verweis auf Text Eingabe Panel](text-input-panel-reference.md)
</dt> </dl>

 

 




