---
title: TTM_SETTITLE Meldung (kommstrg. h)
description: Fügt einer QuickInfo ein Standard Symbol und eine Titel Zeichenfolge hinzu.
ms.assetid: e745a592-eef7-4e0d-8939-a48b52c4ab9f
keywords:
- Windows-Steuerelemente für TTM_SETTITLE Meldung
topic_type:
- apiref
api_name:
- TTM_SETTITLE
- TTM_SETTITLEA
- TTM_SETTITLEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7972a9d40347995e9d641e7fc8706f9ad4c58bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859237"
---
# <a name="ttm_settitle-message"></a>TTM- \_ SetTitle-Meldung

Fügt einer QuickInfo ein Standard Symbol und eine Titel Zeichenfolge hinzu.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Legen Sie *wParam* auf einen der folgenden Werte fest, um das Symbol anzugeben, das angezeigt werden soll. Ab Windows XP SP2 kann dieser Parameter auch einen **HICON** -Wert enthalten. Jeder Wert, der größer als der TTI- \_ Fehler ist, wird als **HICON** angenommen.



| Wert                                                                                                                                                                      | Bedeutung                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="TTI_NONE"></span><span id="tti_none"></span><dl> <dt>**TTI \_ None**</dt> </dl>                             | Kein Symbol.<br/>         |
| <span id="TTI_INFO"></span><span id="tti_info"></span><dl> <dt>**TTI- \_ Informationen**</dt> </dl>                             | Info-Symbol.<br/>       |
| <span id="TTI_WARNING"></span><span id="tti_warning"></span><dl> <dt>**TTI- \_ Warnung**</dt> </dl>                    | Warnungssymbol<br/>     |
| <span id="TTI_ERROR"></span><span id="tti_error"></span><dl> <dt>**TTI- \_ Fehler**</dt> </dl>                          | Fehler Symbol<br/>       |
| <span id="TTI_INFO_LARGE"></span><span id="tti_info_large"></span><dl> <dt>**TTI- \_ Informationen \_ groß**</dt> </dl>          | Symbol "großes Fehler"<br/> |
| <span id="TTI_WARNING_LARGE"></span><span id="tti_warning_large"></span><dl> <dt>**TTI- \_ Warnung \_ groß**</dt> </dl> | Symbol "großes Fehler"<br/> |
| <span id="TTI_ERROR_LARGE"></span><span id="tti_error_large"></span><dl> <dt>**TTI- \_ Fehler \_ groß**</dt> </dl>       | Symbol "großes Fehler"<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die Titel Zeichenfolge. Sie müssen *LPARAM* einen Wert zuweisen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **true** zurück, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Der Titel einer QuickInfo wird über dem Text in einer anderen Schriftart angezeigt. Es reicht nicht aus, einen Titel zu haben. die QuickInfo muss ebenfalls über Text verfügen, oder Sie wird nicht angezeigt.

Wenn *wParam* ein **HICON** enthält, wird eine Kopie des Symbols im QuickInfo-Fenster erstellt.

Wenn **TTM \_ SetTitle** aufgerufen wird, darf die Zeichenfolge, auf die von *LPARAM* verwiesen wird, nicht länger als 100 **tchars** sein, einschließlich der abschließenden **null**-Werte.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie ein Titel und ein System Symbol zu einer QuickInfo hinzugefügt werden.


```C++
// hwndTip is the handle of the tooltip window.
HICON hIcon = LoadIcon(NULL, IDI_INFORMATION);
SendMessage(hwndTip, TTM_SETTITLE, (WPARAM)hIcon, L"Title text");
DestroyIcon(hIcon);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ Settitlew** (Unicode) und **TTM \_ settitlea** (ANSI)<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Info-Steuerelemente](tooltip-controls.md)
</dt> </dl>

 

 





