---
description: Registriert den Anbieter beim Client, damit der Client das Anbieterobjekt für die automatische Vervollständigung der Anwendung aufrufen kann.
ms.assetid: 7b761b30-66f7-454a-9e0d-f45c8099f19f
title: ITipAutocompleteClient::AdviseProvider-Methode (TipAutoComplete.h)
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
ms.openlocfilehash: dd48cdfbf35c5132b42f8185cdc93f53ec34c77df78a51d16da9fa5a5311c144
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938580"
---
# <a name="itipautocompleteclientadviseprovider-method"></a>ITipAutocompleteClient::AdviseProvider-Methode

Registriert den Anbieter beim Client, damit der Client das Anbieterobjekt für die automatische Vervollständigung der Anwendung aufrufen kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT AdviseProvider(
  [in] HWND                     hWndField,
  [in] ITipAutocompleteProvider *pIACProvider
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hWndField* \[ In\]
</dt> <dd>

Das Fensterhandle des Felds, das die Funktion für die automatische Vervollständigung bereitstellt.

</dd> <dt>

*pLIAProvider* \[ In\]
</dt> <dd>

Der Schnittstellenzeiger auf die Anbieterschnittstelle für die automatische Vervollständigung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

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

[**ITipAutocompleteClient::UnadviseProvider-Methode**](itipautocompleteclient-unadviseprovider.md)
</dt> <dt>

[Referenz zum Texteingabebereich](text-input-panel-reference.md)
</dt> </dl>

 

 




