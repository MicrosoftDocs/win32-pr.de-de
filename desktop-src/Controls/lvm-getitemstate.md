---
title: LVM_GETITEMSTATE Meldung (kommstrg. h)
description: Ruft den Status eines Listen Ansichts Elements ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetItemState-Makros senden.
ms.assetid: 862960ed-a64a-4d66-b384-9228932eae6f
keywords:
- Windows-Steuerelemente für LVM_GETITEMSTATE Meldung
topic_type:
- apiref
api_name:
- LVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b355e78f22c01c289f681d256ee6b4d0aa882
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478519"
---
# <a name="lvm_getitemstate-message"></a>LVM \_ GetItemState-Nachricht

Ruft den Status eines Listen Ansichts Elements ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Listen Ansichts Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Zustandsinformationen, die abgerufen werden sollen. Dieser Parameter kann eine Kombination der folgenden Werte sein:



| Wert                                                                                                                                                                           | Bedeutung                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS- \_ Ausschneiden**</dt> </dl>                                  | Das Element ist für einen Ausschneide-und Einfügevorgang gekennzeichnet.<br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS wurde \_ beendet.**</dt> </dl>          | Das Element wird als Drag & Drop-Ziel hervorgehoben.<br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS \_ fokussiert**</dt> </dl>                      | Das Element besitzt den Fokus, sodass es von einem Standard Fokus Rechteck umgeben ist. Obwohl mehr als ein Element ausgewählt werden kann, kann nur ein Element den Fokus haben.<br/> |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ ausgewählt**</dt> </dl>                   | Das Element ist ausgewählt. Die Darstellung eines ausgewählten Elements hängt davon ab, ob es den Fokus und die für die Auswahl verwendeten Systemfarben besitzt.<br/>             |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**LVIS \_ overlaymask**</dt> </dl>          | Verwenden Sie diese Maske, um den Überlagerungs Bild Index des Elements abzurufen.<br/>                                                                                                 |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS- \_ Status-magemask**</dt> </dl> | Verwenden Sie diese Maske, um den Status Bild Index des Elements abzurufen.<br/>                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den aktuellen Zustand für das angegebene Element zurück. Die einzigen gültigen Bits im Rückgabewert entsprechen den Bits, die im *LPARAM* -Parameter festgelegt sind.

## <a name="remarks"></a>Bemerkungen

Die Zustandsinformationen eines Elements enthalten einen Satz von Bitflags und Bildlisten Indizes, die das Zustands Bild des Elements und das Überlagerungs Bild angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LVM- \_ Status**](lvm-setitemstate.md)
</dt> </dl>

 

 





