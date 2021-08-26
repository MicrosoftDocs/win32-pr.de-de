---
title: EM_GETSEL-Nachricht (Winuser.h)
description: Ruft die Anfangs- und Endzeichenpositionen (in TCHARs) der aktuellen Auswahl in einem Bearbeitungssteuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- EM_GETSEL Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca5f3cf1fdaa3c40dd1bb25ebbabb672474e76ae621a05cf52247c216adca17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048800"
---
# <a name="em_getsel-message"></a>EM \_ GETSEL-Nachricht

Ruft die Anfangs- und Endzeichenpositionen (in **TCHAR** s) der aktuellen Auswahl in einem Bearbeitungssteuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Zeiger auf einen **DWORD-Wert,** der die Anfangsposition der Auswahl empfängt. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf einen **DWORD-Wert,** der die Position des ersten nicht ausgewählten Zeichens nach dem Ende der Auswahl empfängt. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein nullbasierter Wert mit der Anfangsposition der Auswahl im [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) und der Position des ersten **TCHAR-Werts** nach dem letzten ausgewählten **TCHAR** im [**HIWORD.**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) Wenn einer dieser Werte 65.535 überschreitet, ist der Rückgabewert -1.

Es ist besser, die in *wParam* und *lParam* zurückgegebenen Werte zu verwenden, da es sich um vollständige 32-Bit-Werte handelt.

## <a name="remarks"></a>Hinweise

Wenn keine Auswahl vorhanden ist, sind die Start- und Endwerte sowohl die Position des Carets.

**Rich Edit-Steuerelemente:** Sie können auch die [**EM \_ EXGETSEL-Nachricht**](em-exgetsel.md) verwenden, um die gleichen Informationen abzurufen. **EM \_ EXGETSEL** gibt auch Anfangs- und Endzeichenpositionen als 32-Bit-Werte zurück.

**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

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

[**EM \_ EXGETSEL**](em-exgetsel.md)
</dt> <dt>

[**EM \_ SETSEL**](em-setsel.md)
</dt> </dl>

 

