---
title: Rich-Flags-Flags für Bearbeitungs Steuerelemente (RichEdit. h)
description: Die Ereignis Maske gibt an, welche Benachrichtigungs Codes ein Rich Edit-Steuerelement an das übergeordnete Fenster sendet. Die Ereignis Maske kann keine oder eine Kombination dieser Werte sein.
ms.assetid: ae0d2cbe-5cbc-42bb-aeb1-7e6be846a4ba
topic_type:
- apiref
api_name:
- ENM_CHANGE
- ENM_CLIPFORMAT
- ENM_CORRECTTEXT
- ENM_DRAGDROPDONE
- ENM_DROPFILES
- ENM_IMECHANGE
- ENM_KEYEVENTS
- ENM_LINK
- ENM_LOWFIRTF
- ENM_MOUSEEVENTS
- ENM_OBJECTPOSITIONS
- ENM_PARAGRAPHEXPANDED
- ENM_PROTECTED
- ENM_REQUESTRESIZE
- ENM_SCROLL
- ENM_SCROLLEVENTS
- ENM_SELCHANGE
- ENM_UPDATE
api_location:
- RichEdit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 006a6d82e7aa4958b03360d05d29a78564f99db7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364683"
---
# <a name="rich-edit-control-event-mask-flags"></a>Rich-Flags für Bearbeitungs Steuerelemente-Ereignis Maske

Die Ereignis Maske gibt an, welche Benachrichtigungs Codes ein Rich Edit-Steuerelement an das übergeordnete Fenster sendet. Die Ereignis Maske kann keine oder eine Kombination dieser Werte sein.



| Konstante                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ENM_CHANGE"></span><span id="enm_change"></span><dl> <dt>**in-m- \_ Änderung**</dt> </dl>                                  | Sendet [en \_ Änderungs](en-change--rich-edit-control-.md) Benachrichtigungen.<br/>                                                                                                                                                                                                                                   |
| <span id="ENM_CLIPFORMAT"></span><span id="enm_clipformat"></span><dl> <dt>**ENM- \_ clipFormat**</dt> </dl>                      | Sendet [en \_ clipFormat](/windows/desktop/Controls/en-clipformat) -Benachrichtigungen.<br/>                                                                                                                                                                                                                                          |
| <span id="ENM_CORRECTTEXT"></span><span id="enm_correcttext"></span><dl> <dt>**\_TM-Korrektur Text**</dt> </dl>                   | Sendet [de- \_ Korrekturen](en-correcttext.md) .<br/>                                                                                                                                                                                                                                             |
| <span id="ENM_DRAGDROPDONE"></span><span id="enm_dragdropdone"></span><dl> <dt>**Umm \_ dragdropdone**</dt> </dl>                | Sendet [en \_ dragdropdone](en-dragdropdone.md) -Benachrichtigungen.<br/>                                                                                                                                                                                                                                           |
| <span id="ENM_DROPFILES"></span><span id="enm_dropfiles"></span><dl> <dt>**"SEM"- \_ dropfiles**</dt> </dl>                         | Sendet "s [ \_ dropfiles](en-dropfiles.md) "-Benachrichtigungen.<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_IMECHANGE"></span><span id="enm_imechange"></span><dl> <dt>**\_ImeChange-Element**</dt> </dl>                         | Microsoft Rich Edit 1,0 only: sendet [en \_ ImeChange](en-imechange.md) -Benachrichtigungen, wenn sich der IME-Konvertierungs Status geändert hat. Nur für asiatische Sprachversionen des Betriebssystems.<br/>                                                                                                              |
| <span id="ENM_KEYEVENTS"></span><span id="enm_keyevents"></span><dl> <dt>**"ESM"- \_ KEYEVENTs**</dt> </dl>                         | Sendet [en \_ msgfilter](en-msgfilter.md) -Benachrichtigungen für Tastatur Ereignisse.<br/>                                                                                                                                                                                                                             |
| <span id="ENM_LINK"></span><span id="enm_link"></span><dl> <dt>**Link "m" \_**</dt> </dl>                                        | **Rich Edit 2,0 und höher:** Sendet [en \_ Link](en-link.md) Benachrichtigungen, wenn sich der Mauszeiger über dem Text befindet, der den CFE \_ -Link aufweist und eine von mehreren Mausaktionen ausgeführt wird.<br/>                                                                                                                     |
| <span id="ENM_LOWFIRTF"></span><span id="enm_lowfirtf"></span><dl> <dt>**"m \_ lowfirtf"**</dt> </dl>                            | Sendet [en \_ lowfirtf](en-lowfirtf.md) -Benachrichtigungen.<br/>                                                                                                                                                                                                                                                   |
| <span id="ENM_MOUSEEVENTS"></span><span id="enm_mouseevents"></span><dl> <dt>**"en"- \_ mouevent-Ereignisse**</dt> </dl>                   | Sendet [en \_ msgfilter](en-msgfilter.md) -Benachrichtigungen für Mausereignisse.<br/>                                                                                                                                                                                                                                |
| <span id="ENM_OBJECTPOSITIONS"></span><span id="enm_objectpositions"></span><dl> <dt>**\_objectpositions-Objekte**</dt> </dl>       | Sendet [en \_ objectpositions](en-objectpositions.md) -Benachrichtigungen.<br/>                                                                                                                                                                                                                                     |
| <span id="ENM_PARAGRAPHEXPANDED"></span><span id="enm_paragraphexpanded"></span><dl> <dt>**Umm \_ .**</dt> </dl> | Sendet [en- \_ paragraphexpanded](/windows/desktop/Controls/en-paragraphexpanded) -Benachrichtigungen.<br/>                                                                                                                                                                                                                            |
| <span id="ENM_PROTECTED"></span><span id="enm_protected"></span><dl> <dt>**durch ein-m \_ geschützt**</dt> </dl>                         | Sendet [ \_ geschützte](en-protected.md) Benachrichtigungen.<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_REQUESTRESIZE"></span><span id="enm_requestresize"></span><dl> <dt>**anforderungsantragnehmergröße \_**</dt> </dl>             | Sendet [en \_ RequestResize](en-requestresize.md) -Benachrichtigungen.<br/>                                                                                                                                                                                                                                         |
| <span id="ENM_SCROLL"></span><span id="enm_scroll"></span><dl> <dt>**Umm- \_ scrollvorgang**</dt> </dl>                                  | Sendet [en \_ HScroll](en-hscroll.md) -und [en \_ VScroll](en-vscroll.md) -Benachrichtigungen.<br/>                                                                                                                                                                                                                   |
| <span id="ENM_SCROLLEVENTS"></span><span id="enm_scrollevents"></span><dl> <dt>**\_SM-scrollevents**</dt> </dl>                | Sendet [en \_ msgfilter](en-msgfilter.md) -Benachrichtigungen für Mausrad Ereignisse.<br/>                                                                                                                                                                                                                          |
| <span id="ENM_SELCHANGE"></span><span id="enm_selchange"></span><dl> <dt>**\_Selm selChange**</dt> </dl>                         | Sendet [en \_ selChange](en-selchange.md) -Benachrichtigungen.<br/>                                                                                                                                                                                                                                                 |
| <span id="ENM_UPDATE"></span><span id="enm_update"></span><dl> <dt>**m- \_ Update**</dt> </dl>                                  | Sendet [en \_ Update](en-update.md) -Benachrichtigungen. <br/> **Rich Edit 2,0 und höher:** dieses Flag wird ignoriert, und es werden immer die [en \_ Update](en-update.md) -Benachrichtigungen gesendet. Wenn Rich Edit 3,0 jedoch Microsoft Rich Edit 1,0 emuliert, müssen Sie dieses Flag verwenden, um en \_ Update Benachrichtigungen zu senden.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Standard Ereignis Maske ist "ENM \_ None". in diesem Fall werden keine Benachrichtigungen an das übergeordnete Fenster gesendet. Sie können die Ereignis Maske für ein Rich Edit-Steuerelement mithilfe der Nachrichten [**EM \_ GetEventMask**](em-geteventmask.md) und [**EM \_ SetEventMask**](em-seteventmask.md) abrufen und festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>RichEdit. h</dt> </dl> |



 

