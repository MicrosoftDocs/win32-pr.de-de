---
title: TBM_SETSEL Meldung (kommstrg. h)
description: Legt die Anfangs-und Endpositionen für den verfügbaren Auswahlbereich in einer TrackBar fest.
ms.assetid: 71f5b9f8-4850-44a8-8acf-adca9bda84c3
keywords:
- Windows-Steuerelemente für TBM_SETSEL Meldung
topic_type:
- apiref
api_name:
- TBM_SETSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2edebc6b6dcf3b0b93e3047a39aac74c34d121bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739904"
---
# <a name="tbm_setsel-message"></a>TBM- \_ Nachricht

Legt die Anfangs-und Endpositionen für den verfügbaren Auswahlbereich in einer TrackBar fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag neu zeichnen. Wenn dieser Parameter **true** ist, zeichnet die Nachricht die TrackBar neu, nachdem der Auswahlbereich festgelegt wurde. Wenn dieser Parameter auf **false** festgelegt ist, legt die Meldung den Auswahlbereich fest, aber die TrackBar wird nicht neu gezeichnet.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die logische Startposition für den Auswahlbereich an, und das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die logische Endposition an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird ignoriert, wenn die TrackBar nicht über den [**\_ enableselrange**](trackbar-control-styles.md) -Stil von TB verfügt.

**TBM \_** Mithilfe von "-tsel" können Sie den Zeiger auf einen Teil des Bereichs beschränken, der für die Statusanzeige verfügbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**TBM- \_ getselend**](tbm-getselend.md)
</dt> <dt>

[**TBM \_ getselstart**](tbm-getselstart.md)
</dt> <dt>

[**TBM- \_ setselend**](tbm-setselend.md)
</dt> <dt>

[**TBM- \_ setselstart**](tbm-setselstart.md)
</dt> </dl>

 

