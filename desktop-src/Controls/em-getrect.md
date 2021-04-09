---
title: EM_GETRECT Meldung (Winuser. h)
description: Ruft das Formatierungs Rechteck eines Bearbeitungs Steuer Elements ab.
ms.assetid: eef0150d-9b7a-4247-acbf-6fea2efd1dc3
keywords:
- Windows-Steuerelemente für EM_GETRECT Meldung
topic_type:
- apiref
api_name:
- EM_GETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8192fd4c3aa7fbe953a36217f6b1408f055d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858961"
---
# <a name="em_getrect-message"></a>EM \_ GetRect-Nachricht

Ruft das [Formatierungs Rechteck](about-edit-controls.md) eines Bearbeitungs Steuer Elements ab. Das Formatierungs Rechteck ist das einschränkende Rechteck, in das das Steuerelement den Text zeichnet. Das Begrenzungs Rechteck ist unabhängig von der Größe des Bearbeitungs Steuer Elements. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das Formatierungs Rechteck empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist nicht sinnvoll.

## <a name="remarks"></a>Bemerkungen

Sie können das Formatierungs Rechteck eines mehrzeiligen Bearbeitungs Steuer Elements ändern, indem Sie die Meldungen " [**EM \_ SetRect**](em-setrect.md) " und " [**EM \_ setrectnp**](em-setrectnp.md) " verwenden.

Unter bestimmten Bedingungen gibt **EM \_ GetRect** möglicherweise nicht die exakten Werte zurück, die von [**EM \_ SetRect**](em-setrect.md) oder [**EM \_ setrectnp**](em-setrectnp.md) festgelegt wurden

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Das Formatierungs Rechteck enthält nicht die Auswahl Leiste, bei der es sich um einen nicht markierten Bereich links neben den einzelnen Absätzen handelt. Wenn Sie darauf klicken, wählt die Auswahl Leiste die Zeile aus. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

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

[**EM \_ setrectnp**](em-setrectnp.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

