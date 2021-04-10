---
title: EM_GETSEL Meldung (Winuser. h)
description: Ruft die Position des Anfangs-und des Endzeichens (in tchars) der aktuellen Auswahl in einem Bearbeitungs Steuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- Windows-Steuerelemente für EM_GETSEL Meldung
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
ms.openlocfilehash: d28ba97c9043866c3e97c1c51389447498562455
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040548"
---
# <a name="em_getsel-message"></a>EM \_ GetSEL-Nachricht

Ruft die Position des Anfangs-und des Endzeichens (in **TCHAR** s) der aktuellen Auswahl in einem Bearbeitungs Steuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Zeiger auf einen **DWORD** -Wert, der die Anfangsposition der Auswahl empfängt. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf einen **DWORD** -Wert, der die Position des ersten nicht ausgewählten Zeichens nach dem Ende der Auswahl empfängt. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein NULL basierter Wert, der die Anfangsposition der Auswahl im [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) und die Position des ersten **tchars** nach dem letzten ausgewählten **TCHAR** im [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))-Ausdruck aufweist. Wenn einer dieser Werte 65.535 überschreitet, ist der Rückgabewert-1.

Es ist besser, die in *wParam* und *LPARAM* zurückgegebenen Werte zu verwenden, da es sich um vollständige 32-Bit-Werte handelt.

## <a name="remarks"></a>Bemerkungen

Wenn keine Auswahl vorhanden ist, sind die Anfangs-und Endwerte die Position der Einfügemarke.

**Rich Edit-Steuerelemente:** Sie können auch die [**EM \_ exgetsel**](em-exgetsel.md) -Nachricht verwenden, um die gleichen Informationen abzurufen. **EM \_ Exgetsel** gibt auch Start-und Endzeichen Positionen als 32-Bit-Werte zurück.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

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

[**EM \_ exgetsel**](em-exgetsel.md)
</dt> <dt>

[**EM- \_ tsel**](em-setsel.md)
</dt> </dl>

 

