---
title: EM_SETRECTNP-Nachricht (Winuser.h)
description: 'EM_SETRECTNP Meldung: Legt das Formatierungsrechteck eines mehrzeiligen Bearbeitungssteuerelements fest.'
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- EM_SETRECTNP Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_SETRECTNP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60341a41706f012064d3b7cbc79aa019f1492c3a8d535866fa51fc7ea8dfd437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831131"
---
# <a name="em_setrectnp-message"></a>EM \_ SETRECTNP-Nachricht

Legt das [Formatierungsrechteck](about-edit-controls.md) eines mehrzeiligen Bearbeitungssteuerelements fest. Die **EM \_ SETRECTNP-Nachricht** ist mit der [**EM \_ SETRECT-Nachricht**](em-setrect.md) identisch, mit der Ausnahme, dass **EM \_ SETRECTNP** das Bearbeitungssteuerelementfenster *nicht* neu zeichnet.

Das Formatierungsrechteck ist das einschränkende Rechteck, in das das Steuerelement den Text zeichnet. Das einschränkende Rechteck ist unabhängig von der Größe des Bearbeitungssteuerelementfensters.

Diese Meldung wird nur von mehrzeiligen Bearbeitungssteuerelementen verarbeitet. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

**Rich Edit 3.0 und höher:** Gibt an, ob das neue Rechteck absolute oder relative Koordinaten enthält. Der Wert 0 (null) gibt absolute Koordinaten an. Der Wert 1 gibt Offsets relativ zum aktuellen Formatierungsrechteck an. (Die Offsets können positiv oder negativ sein.)

**Bearbeiten von Steuerelementen:** Dieser Parameter wird nicht verwendet und muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die die neuen Dimensionen des Rechtecks angibt. Wenn dieser Parameter **NULL** ist, wird das Formatierungsrechteck auf die Standardwerte festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

**Rich Edit:** Wird in Microsoft Rich Edit 3.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ SETRECT**](em-setrect.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

