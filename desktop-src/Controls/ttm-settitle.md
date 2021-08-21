---
title: TTM_SETTITLE Nachricht (Commctrl.h)
description: Fügt einer QuickInfo ein Standardsymbol und eine Titelzeichenfolge hinzu.
ms.assetid: e745a592-eef7-4e0d-8939-a48b52c4ab9f
keywords:
- TTM_SETTITLE Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: e0e159ce522ea27361f93beaa96da06959fba6f92fedf5981dfd049ddc7f36cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166353"
---
# <a name="ttm_settitle-message"></a>TTM \_ SETTITLE-Nachricht

Fügt einer QuickInfo ein Standardsymbol und eine Titelzeichenfolge hinzu.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Legen Sie *wParam* auf einen der folgenden Werte fest, um das anzuzeigende Symbol anzugeben. Ab Windows XP SP2 und höher kann dieser Parameter auch einen **HICON-Wert** enthalten. Jeder Wert, der größer als TTI \_ ERROR ist, wird als **HICON**-Wert angenommen.



| Wert                                                                                                                                                                      | Bedeutung                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="TTI_NONE"></span><span id="tti_none"></span><dl> <dt>**TTI \_ NONE**</dt> </dl>                             | Kein Symbol.<br/>         |
| <span id="TTI_INFO"></span><span id="tti_info"></span><dl> <dt>**TTI \_ INFO**</dt> </dl>                             | Infosymbol.<br/>       |
| <span id="TTI_WARNING"></span><span id="tti_warning"></span><dl> <dt>**TTI \_ WARNING**</dt> </dl>                    | Warnungssymbol<br/>     |
| <span id="TTI_ERROR"></span><span id="tti_error"></span><dl> <dt>**\_TTI-FEHLER**</dt> </dl>                          | Fehlersymbol<br/>       |
| <span id="TTI_INFO_LARGE"></span><span id="tti_info_large"></span><dl> <dt>**TTI \_ INFO \_ LARGE**</dt> </dl>          | Symbol für große Fehler<br/> |
| <span id="TTI_WARNING_LARGE"></span><span id="tti_warning_large"></span><dl> <dt>**TTI \_ WARNING \_ LARGE**</dt> </dl> | Symbol für große Fehler<br/> |
| <span id="TTI_ERROR_LARGE"></span><span id="tti_error_large"></span><dl> <dt>**TTI \_ ERROR \_ LARGE**</dt> </dl>       | Symbol für große Fehler<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf die Titelzeichenfolge. Sie müssen *lParam* einen Wert zuweisen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **FALSE,** wenn dies nicht der Fall ist.

## <a name="remarks"></a>Hinweise

Der Titel einer QuickInfo wird über dem Text in einer anderen Schriftart angezeigt. Es reicht nicht aus, über einen Titel zu verfügen. Die QuickInfo muss ebenfalls Text enthalten, andernfalls wird sie nicht angezeigt.

Wenn *wParam* einen **HICON** enthält, wird vom QuickInfo-Fenster eine Kopie des Symbols erstellt.

Beim Aufrufen von **TTM \_ SETTITLE** darf die Zeichenfolge, auf die *von lParam* verwiesen wird, 100 **TCHARs** nicht überschreiten, einschließlich des abschließenden **NULL-Werts.**

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie Sie einer QuickInfo einen Titel und ein Systemsymbol hinzufügen.


```C++
// hwndTip is the handle of the tooltip window.
HICON hIcon = LoadIcon(NULL, IDI_INFORMATION);
SendMessage(hwndTip, TTM_SETTITLE, (WPARAM)hIcon, L"Title text");
DestroyIcon(hIcon);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ SETTITLEW** (Unicode) und **TTM \_ SETTITLEA** (ANSI)<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Informationen zu QuickInfo-Steuerelementen](tooltip-controls.md)
</dt> </dl>

 

 





