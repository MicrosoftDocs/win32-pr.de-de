---
description: Bestimmt, ob der Eingabebereich für die Automatische Vervollständigungsliste bereit ist.
ms.assetid: 1e0d4bc6-e6a3-4123-a381-00a41ed9c848
title: ITipAutocompleteClient::RequestShowUI-Methode (TipAutoComplete.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteClient.RequestShowUI
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 4288a506e14ae8096db9be051e3282bb2ebd62522988d75574f3e56070419fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449793"
---
# <a name="itipautocompleteclientrequestshowui-method"></a>ITipAutocompleteClient::RequestShowUI-Methode

Bestimmt, ob der Eingabebereich für die Automatische Vervollständigungsliste bereit ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT RequestShowUI(
  [in]  HWND hWndACList,
  [out] BOOL *pfAllowShowing
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hWndACList* \[ In\]
</dt> <dd>

Fensterhandle der Benutzeroberfläche für die automatische Vervollständigung der Liste.

</dd> <dt>

*pfAllowShowing* \[ out\]
</dt> <dd>

**FALSE,** wenn der Client empfiehlt, die Benutzeroberfläche der automatischen Vervollständigungsliste nicht anzuzeigen. **TRUE,** wenn der Anbieter für die automatische Vervollständigung die Benutzeroberfläche der Liste anzeigen kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode wird vom Anbieter für die automatische Vervollständigung aufgerufen, wenn die Benutzeroberfläche für die automatische Vervollständigung angezeigt wird. Wenn der interne Zustand des Clients nicht zulässt, dass der Anbieter die Benutzeroberfläche anzeigen kann, wird *pfAllowShowing* auf **FALSE** festgelegt. Wenn der Text z. B. vom Handschriftskin im Tablet PC-Eingabebereich an das Feld gesendet wird und der Benutzer sofort mit dem Freihandeingaben beginnt, empfiehlt der Client, die automatisch vollständige Benutzeroberfläche nicht anzuzeigen, um eine Destruktion des Freihandeingabens des Benutzers zu vermeiden, indem *pfAllowShowing* auf **FALSE** festgelegt wird.

Rufen Sie **RequestShowUI** auf, um das Popuphandle für das Automatische Abschließen des Listenfensters festzulegen, bevor Sie die [**ITipAutocompleteClient::P referredRects-Methode**](itipautocompleteclient-preferredrects.md)aufrufen. Wenn Sie dies nicht tun, tritt beim Aufrufen von **PreferredRects** ein **E \_ INVALIDARG-Fehler** auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                       |
| Header<br/>                   | <dl> <dt>TipAutoComplete.h (erfordert auch Peninputpanel \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**ITipAutocompleteClient-Schnittstelle**](itipautocompleteclient.md)
</dt> <dt>

[**ITipAutocompleteClient::P referredRects-Methode**](itipautocompleteclient-preferredrects.md)
</dt> <dt>

[Referenz zum Texteingabebereich](text-input-panel-reference.md)
</dt> </dl>

 

 




