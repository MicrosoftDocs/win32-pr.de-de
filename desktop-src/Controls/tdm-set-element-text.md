---
title: TDM_SET_ELEMENT_TEXT (Commctrl.h)
description: 'TDM_SET_ELEMENT_TEXT Meldung: Aktualisiert ein Textelement in einem Aufgabendialogfeld.'
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- TDM_SET_ELEMENT_TEXT von Windows-Steuerelementen
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
ms.openlocfilehash: 7bb0f81867bcff4fd5f7d533c156c8af17d0f4a761b6f8560aa584a85c62b7c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060770"
---
# <a name="tdm_set_element_text-message"></a>TDM \_ SET \_ ELEMENT \_ TEXT-Meldung

Aktualisiert ein Textelement in einem Aufgabendialogfeld.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Gibt das zu aktualisierende Element an. (Eine Abbildung finden Sie unter [Informationen zu Taskdialogfeldern.)](task-dialogs-overview.md) Dieser Parameter muss einer der folgenden Werte sein.



| Wert                                                                                                                                                                                           | Bedeutung                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**\_TDE-INHALT**</dt> </dl>                                         | Inhalt.<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**ERWEITERTE \_ \_ TDE-INFORMATIONEN**</dt> </dl> | Erweiterte Informationen.<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**\_TDE-FUßZEILE**</dt> </dl>                                            | Fußzeilentext.<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**TDE \_ \_ MAIN-ANWEISUNG**</dt> </dl>             | Main-Anweisung.<br/>     |



 

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Der zu verwendende neue Text.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Hinweise

Die Größe oder das Layout des Aufgabendialogfelds kann sich ändern, um den neuen Text zu unterstützen.

## <a name="examples"></a>Beispiele

Der folgende Beispielcode zeigt, wie der Fußzeilentext im Aufgabendialogfeld festgelegt wird, das durch *hwnd dargestellt wird.*


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TDM \_ UPDATE \_ ELEMENT \_ TEXT**](tdm-update-element-text.md)
</dt> </dl>

 

 





