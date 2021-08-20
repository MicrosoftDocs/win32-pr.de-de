---
title: TB_SETBUTTONWIDTH (Commctrl.h)
description: Legt die minimale und maximale Schaltflächenbreite im Symbolleisten-Steuerelement fest.
ms.assetid: 3311216a-e0b2-48bb-bad7-0a04185573cf
keywords:
- TB_SETBUTTONWIDTH von Windows-Steuerelementen
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
ms.openlocfilehash: 145ae1459b76fba60dd76b34e36d222cf62b93af071f2b430321d86956a3a871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167595"
---
# <a name="tb_setbuttonwidth-message"></a>TB \_ SETBUTTONWIDTH-Nachricht

Legt die minimale und maximale Schaltflächenbreite im Symbolleisten-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LOWORD gibt**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) die minimale Schaltflächenbreite in Pixel an. Symbolleistenschaltflächen sind nie schmaler als dieser Wert.

Das [**HIWORD gibt**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) die maximale Schaltflächenbreite in Pixel an. Wenn der Schaltflächentext zu breit ist, zeigt das Steuerelement ihn mit Auslassungspunkten an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Verwenden **Sie TB \_ SETBUTTONWIDTH,** um die maximal zulässige und minimale Breite für Schaltflächen vor dem Hinzugefügten zu setzen. Verwenden [**Sie TB \_ SETBUTTONSIZE,**](tb-setbuttonsize.md) um die tatsächliche Größe von Schaltflächen festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

