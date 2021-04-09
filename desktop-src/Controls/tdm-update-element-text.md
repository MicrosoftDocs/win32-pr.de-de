---
title: TDM_UPDATE_ELEMENT_TEXT Meldung (kommstrg. h)
description: Aktualisiert ein Textelement in einem Aufgaben Dialogfeld.
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- Windows-Steuerelemente für TDM_UPDATE_ELEMENT_TEXT Meldung
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
ms.openlocfilehash: b6dac6787c68d0cbe619bbf28fa1a6383606e99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106245"
---
# <a name="tdm_update_element_text-message"></a>TDM- \_ Aktualisierungs \_ Element- \_ Text Nachricht

Aktualisiert ein Textelement in einem Aufgaben Dialogfeld.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Gibt das zu Aktualisier Endes Element an. (Eine Abbildung der Elemente finden Sie unter [Informationen zu Aufgaben Dialogfeldern](task-dialogs-overview.md).) Dieser Parameter muss einen der folgenden Werte aufweisen:



| Wert                                                                                                                                                                                           | Bedeutung                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**TDE- \_ Inhalt**</dt> </dl>                                         | Inhalt.<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**\_Erweiterte Informationen zu TDE \_**</dt> </dl> | Erweiterte Informationen.<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**TDE- \_ Fußzeile**</dt> </dl>                                            | FooterText.<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**TDE- \_ Haupt \_ Anweisung**</dt> </dl>             | Main-Anweisung.<br/>     |



 

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Zeiger auf eine Unicode-Zeichenfolge, die den neuen Text enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Bemerkungen

Der neue Text darf nicht länger als der vorhandene Text sein, um das Abschneiden zu vermeiden. Wenn Sie den Text auf eine kürzere Zeichenfolge festlegen, wird die Größe des Dialog Felds nicht geändert.

Wenn der **pszexpandedinformation** -Member der [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) -Struktur, die zum Erstellen des Aufgaben Dialogfelds verwendet wurde, **null** war und Sie eine **TDM- \_ Aktualisierungs \_ Element- \_ Text** Nachricht mit erweiterten TDE- \_ Informationen senden \_ , geschieht nichts.

Das obige gilt auch für die Fußzeile und den TDE- \_ Fußzeile.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TDM \_ - \_ Element \_ Text festlegen**](tdm-set-element-text.md)
</dt> </dl>

 

 





