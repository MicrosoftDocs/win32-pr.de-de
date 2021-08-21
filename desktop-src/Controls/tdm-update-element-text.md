---
title: TDM_UPDATE_ELEMENT_TEXT (Commctrl.h)
description: 'TDM_UPDATE_ELEMENT_TEXT Meldung: Aktualisiert ein Textelement in einem Aufgabendialogfeld.'
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- TDM_UPDATE_ELEMENT_TEXT meldungssteuerelemente Windows
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
ms.openlocfilehash: 5abf6eb91b3eadfea71d0c9a4b5386e44db100c3a548998d5113636ff7f8cc29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166913"
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

## <a name="remarks"></a>Hinweise

Um Clipping zu vermeiden, darf der neue Text nicht mehr als der vorhandene Text sein. Das Festlegen des Texts auf eine kürzere Zeichenfolge führt nicht dazu, dass die Größe des Dialogfelds geändert wird.

Wenn das **pszExpandedInformation-Element** der [**TASKDIALOGCONFIG-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) das zum Erstellen des Aufgabendialogfelds verwendet wurde, **NULL** war und Sie eine **TDM \_ UPDATE ELEMENT \_ \_ TEXT-Nachricht** mit TDE EXPANDED INFORMATION senden, geschieht \_ \_ nichts.

Die obigen Angaben gelten auch für die Fußzeile und die \_ TDE-FUßZEILE.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TDM \_ SET \_ ELEMENT \_ TEXT**](tdm-set-element-text.md)
</dt> </dl>

 

 





