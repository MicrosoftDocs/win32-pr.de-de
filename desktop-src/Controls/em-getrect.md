---
title: EM_GETRECT Meldung (Winuser.h)
description: Ruft das Formatierungsrechteck eines Bearbeitungssteuerelements ab.
ms.assetid: eef0150d-9b7a-4247-acbf-6fea2efd1dc3
keywords:
- EM_GETRECT Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: f1d4ad7dbab40a8d294d814e3524b54c5b11206c91608e9293bdf88df2a63f23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541040"
---
# <a name="em_getrect-message"></a>EM \_ GETRECT-Nachricht

Ruft das [Formatierungsrechteck](about-edit-controls.md) eines Bearbeitungssteuerelements ab. Das Formatierungsrechteck ist das einschränkende Rechteck, in das das Steuerelement den Text zeichnet. Das einschränkende Rechteck ist unabhängig von der Größe des Bearbeitungssteuerelementfensters. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die das Formatierungsrechteck empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist nicht aussagekräftig.

## <a name="remarks"></a>Hinweise

Sie können das Formatierungsrechteck eines mehrzeiligen Bearbeitungssteuerelements mithilfe der [**EM \_ SETRECT-**](em-setrect.md) und [**EM \_ SETRECTNP-Meldungen**](em-setrectnp.md) ändern.

Unter bestimmten Umständen gibt **EM \_ GETRECT** möglicherweise nicht die genauen Werte zurück, die [**EM \_ SETRECT**](em-setrect.md) oder [**EM \_ SETRECTNP**](em-setrectnp.md) festlegen, sind ungefähr richtig, können aber um einige Pixel deaktiviert sein.

**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Das Formatierungsrechteck enthält nicht die Auswahlleiste, bei der es sich um einen nicht markierten Bereich links neben jedem Absatz handelt. Wenn Sie darauf klicken, wählt die Auswahlleiste die Zeile aus. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

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

[**EM \_ SETRECTNP**](em-setrectnp.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

