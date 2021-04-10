---
title: TDM_SET_ELEMENT_TEXT Meldung (kommstrg. h)
description: Aktualisiert ein Textelement in einem Aufgaben Dialogfeld.
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- Windows-Steuerelemente für TDM_SET_ELEMENT_TEXT Meldung
topic_type:
- apiref
api_name:
- TDM_SET_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2229dc269f14c9a3b0765675dcc97dc9776b72c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040945"
---
# <a name="tdm_set_element_text-message"></a>TDM \_ - \_ Element \_ Text Nachricht

Aktualisiert ein Textelement in einem Aufgaben Dialogfeld.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Gibt das zu Aktualisier Endes Element an. (Eine Abbildung finden Sie unter [Informationen zu Aufgaben Dialogfeldern](task-dialogs-overview.md).) Dieser Parameter muss einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                           | Bedeutung                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**TDE- \_ Inhalt**</dt> </dl>                                         | Inhalt.<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**\_Erweiterte Informationen zu TDE \_**</dt> </dl> | Erweiterte Informationen.<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**TDE- \_ Fußzeile**</dt> </dl>                                            | FooterText.<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**TDE- \_ Haupt \_ Anweisung**</dt> </dl>             | Main-Anweisung.<br/>     |



 

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Der zu verwendende neue Text.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Bemerkungen

Die Größe oder das Layout des Aufgaben Dialogfelds kann geändert werden, um den neuen Text zu unterstützen.

## <a name="examples"></a>Beispiele

Der folgende Beispielcode zeigt, wie der FooterText im Aufgaben Dialogfeld festgelegt wird, das durch *HWND* dargestellt wird.


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TDM- \_ Aktualisierungs \_ Element \_ Text**](tdm-update-element-text.md)
</dt> </dl>

 

 





