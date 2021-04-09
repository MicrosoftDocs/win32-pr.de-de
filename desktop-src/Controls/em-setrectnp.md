---
title: EM_SETRECTNP Meldung (Winuser. h)
description: Legt das Formatierungs Rechteck eines mehrzeiligen Bearbeitungs Steuer Elements fest.
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- Windows-Steuerelemente für EM_SETRECTNP Meldung
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
ms.openlocfilehash: e017bd4737c843c2452382918d71ef63345917cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957001"
---
# <a name="em_setrectnp-message"></a>EM \_ setrectnp-Meldung

Legt das [Formatierungs Rechteck](about-edit-controls.md) eines mehrzeiligen Bearbeitungs Steuer Elements fest. Die **EM- \_ setrectnp** -Nachricht ist mit der [**EM- \_ SetRect**](em-setrect.md) -Nachricht identisch, mit dem Unterschied, dass **EM \_ setrectnp** das Bearbeitungs Steuerelement Fenster *nicht* neu zeichnet.

Das Formatierungs Rechteck ist das einschränkende Rechteck, in das das Steuerelement den Text zeichnet. Das Begrenzungs Rechteck ist unabhängig von der Größe des Bearbeitungs Steuer Elements.

Diese Meldung wird nur von mehrzeiligen Bearbeitungs Steuerelementen verarbeitet. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

**Rich Edit 3,0 und höher:** Gibt an, ob das neue Rechteck absolute oder relative Koordinaten enthält. Der Wert 0 (null) gibt absolute Koordinaten an. Der Wert 1 gibt Offsets relativ zum aktuellen Formatierungs Rechteck an. (Die Offsets können positiv oder negativ sein.)

Steuer **Elemente bearbeiten:** Dieser Parameter wird nicht verwendet und muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die neuen Abmessungen des Rechtecks angibt. Wenn dieser Parameter **null** ist, wird das Formatierungs Rechteck auf seine Standardwerte festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 3,0 und höher unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ SetRect**](em-setrect.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

