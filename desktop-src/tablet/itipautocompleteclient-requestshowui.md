---
description: Bestimmt, ob der Eingabebereich bereit ist, die Auto Vervollständigen-Liste angezeigt zu haben.
ms.assetid: 1e0d4bc6-e6a3-4123-a381-00a41ed9c848
title: 'Itipautocompleteclient:: requestshowui-Methode (tipautocomplete. h)'
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
ms.openlocfilehash: e547376bf2e9c50c224d1917e00329e8d9555e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216407"
---
# <a name="itipautocompleteclientrequestshowui-method"></a>Itipautocompleteclient:: requestshowui-Methode

Bestimmt, ob der Eingabebereich bereit ist, die Auto Vervollständigen-Liste angezeigt zu haben.

## <a name="syntax"></a>Syntax


```C++
HRESULT RequestShowUI(
  [in]  HWND hWndACList,
  [out] BOOL *pfAllowShowing
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndaclist* \[ in\]
</dt> <dd>

Fenster Handle der Benutzeroberfläche für die automatische Vervollständigung.

</dd> <dt>

*pfallow-Anzeige* \[ vorgenommen\]
</dt> <dd>

**False** , wenn vom Client empfohlen wird, die Benutzeroberfläche für die automatische Vervollständigung nicht anzuzeigen. **True** , wenn der Anbieter für automatische Vervollständigung die Listen Benutzeroberfläche anzeigen kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode wird vom Auto Vervollständigen-Anbieter aufgerufen, wenn die Benutzeroberfläche für die automatische Vervollständigung angezeigt wird. Wenn der interne Zustand des Clients die Benutzeroberfläche nicht anzeigen kann, wird *pfallowshow* auf **false** festgelegt. Wenn der Text z. b. aus dem Handschrift Design des Tablet PC-Eingabe Bereichs an das Feld gesendet wird und der Benutzer sofort mit dem Binden beginnt, wird empfohlen, die Benutzeroberfläche für die automatische Vervollständigung nicht anzuzeigen, um zu vermeiden, dass das Inking des Benutzers zerstört wird, indem *pfallowshow* auf **false** festgelegt wird.

Aufrufen von **requestshowui** , um das Fenster Handle für das automatische Popup-Listenfenster festzulegen, bevor Sie die [**itipautocompleteclient::P referredrects-Methode**](itipautocompleteclient-preferredrects.md)aufrufen. Wenn dies nicht der Fall ist, wird beim Aufrufen von " **preferredrects**" ein **E \_ invalidArg** -Fehler ausgelöst.

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

[**Itipaudecompleteclient::P referredrects-Methode**](itipautocompleteclient-preferredrects.md)
</dt> <dt>

[Verweis auf Text Eingabe Panel](text-input-panel-reference.md)
</dt> </dl>

 

 




