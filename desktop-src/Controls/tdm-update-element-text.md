---
title: TDM_UPDATE_ELEMENT_TEXT (Commctrl.h)
description: 'TDM_UPDATE_ELEMENT_TEXT Meldung: Aktualisiert ein Textelement in einem Aufgabendialogfeld.'
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- TDM_UPDATE_ELEMENT_TEXT Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TDM_UPDATE_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c155b426b92645c0b9cdbabe00c44ffa722b89f3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085808"
---
# <a name="tdm_update_element_text-message"></a>TDM \_ UPDATE ELEMENT TEXT \_ \_ message

Aktualisiert ein Textelement in einem Aufgabendialogfeld.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Gibt das zu aktualisierende Element an. (Eine Abbildung der Elemente finden Sie unter [Informationen zu Taskdialogfeldern.)](task-dialogs-overview.md) Dieser Parameter muss einer der folgenden Werte sein:



| Wert                                                                                                                                                                                           | Bedeutung                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**\_TDE-INHALT**</dt> </dl>                                         | Inhalt.<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**ERWEITERTE \_ \_ TDE-INFORMATIONEN**</dt> </dl> | Erweiterte Informationen.<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**\_TDE-FUßZEILE**</dt> </dl>                                            | Fußzeilentext.<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**TDE \_ \_ MAIN-ANWEISUNG**</dt> </dl>             | Main-Anweisung.<br/>     |



 

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Zeiger auf eine Unicode-Zeichenfolge, die den neuen Text enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Bemerkungen

Um Clipping zu vermeiden, darf der neue Text nicht mehr als der vorhandene Text sein. Das Festlegen des Texts auf eine kürzere Zeichenfolge führt nicht dazu, dass die Größe des Dialogfelds geändert wird.

Wenn der **pszExpandedInformation-Member** der [**TASKDIALOGCONFIG-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) der zum Erstellen des Aufgabendialogfelds verwendet wurde, **NULL** war und Sie eine **TDM \_ UPDATE ELEMENT \_ \_ TEXT-Nachricht** mit TDE \_ EXPANDED INFORMATION \_ senden, geschieht nichts.

Das obige Gilt gilt auch für die Fußzeile und die \_ TDE-FUßZEILE.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TDM \_ \_ SET-ELEMENTTEXT \_**](tdm-set-element-text.md)
</dt> </dl>

 

 





