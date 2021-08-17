---
description: Bestimmt, ob der Eingabebereich bereit ist, damit die Liste der automatischen Vervollstehung angezeigt wird.
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

Bestimmt, ob der Eingabebereich bereit ist, damit die Liste der automatischen Vervollstehung angezeigt wird.

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

Fensterhand handle der Benutzeroberfläche für die automatisch abgeschlossene Liste.

</dd> <dt>

*pfAllowShowing* \[ out\]
</dt> <dd>

**FALSE,** wenn der Client empfiehlt, die Benutzeroberfläche für die Liste automatisch abschließen nicht zu zeigen. **TRUE,** wenn der AutoVervollständigen-Anbieter die Benutzeroberfläche der Liste anzeigen kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode wird vom AutoVervollständigen-Anbieter aufgerufen, wenn die Benutzeroberfläche für die automatische Vervollstehung angezeigt wird. Wenn der interne Zustand des Clients dem Anbieter das Anzeigen der Benutzeroberfläche nicht erlaubt, wird *pfAllowShowing* auf **FALSE festgelegt.** Wenn der Text z. B. von der Handschrift-Skin im Eingabebereich des Tablet-PCs an das Feld gesendet wird und der Benutzer sofort mit dem Freihandeingaben beginnt, empfiehlt der Client, die benutzeroberfläche für die automatische Vervollst duplizierung nicht zu zeigen, um zu verhindern, dass die Freihandeingabe des Benutzers zerstört wird, indem *pfAllowShowing auf* FALSE festgelegt **wird.**

Rufen **Sie RequestShowUI auf,** um das Popuphandl des Listenfensters für die automatische Vervollständigung vor dem Aufrufen der [**ITipAutocompleteClient::P referredRects-Methode fest.**](itipautocompleteclient-preferredrects.md) Wenn Sie dies nicht tun, tritt beim Aufrufen von PreferredRects ein **E \_ INVALIDARG-Fehler** **auf.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                                       |
| Header<br/>                   | <dl> <dt>TipAutoComplete.h (erfordert auch Peninputpanel \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITipAutocompleteClient-Schnittstelle**](itipautocompleteclient.md)
</dt> <dt>

[**ITipAutocompleteClient::P referredRects-Methode**](itipautocompleteclient-preferredrects.md)
</dt> <dt>

[Referenz zum Texteingabebereich](text-input-panel-reference.md)
</dt> </dl>

 

 




