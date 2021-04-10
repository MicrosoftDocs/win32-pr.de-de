---
title: TB_SETBUTTONWIDTH Meldung (kommstrg. h)
description: Legt die minimale und maximale Schaltflächen breite im Symbolleisten-Steuerelement fest.
ms.assetid: 3311216a-e0b2-48bb-bad7-0a04185573cf
keywords:
- Windows-Steuerelemente für TB_SETBUTTONWIDTH Meldung
topic_type:
- apiref
api_name:
- TB_SETBUTTONWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e105770d72e90108b9c31311f77599520cecea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103760"
---
# <a name="tb_setbuttonwidth-message"></a>TB \_ setbuttonwidth-Meldung

Legt die minimale und maximale Schaltflächen breite im Symbolleisten-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die minimale Schaltflächen breite in Pixel an. Symbolleisten Schaltflächen werden nie kleiner als dieser Wert sein.

Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die maximale Schaltflächen breite in Pixel an. Wenn der Text der Schaltfläche zu breit ist, wird das Steuerelement mit Auslassungs Punkten angezeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Legen Sie mit " **TB \_ setbuttonwidth** " die maximale und minimale zulässige Breite für Schaltflächen fest, bevor Sie hinzugefügt werden. Legen Sie die tatsächliche Größe von Schaltflächen mit [**TB \_ setbuttonsize**](tb-setbuttonsize.md) fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

