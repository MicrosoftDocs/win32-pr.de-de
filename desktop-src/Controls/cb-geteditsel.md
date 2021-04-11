---
title: CB_GETEDITSEL Meldung (Winuser. h)
description: Ruft die Position des Anfangs-und des Endzeichens der aktuellen Auswahl im Bearbeitungs Steuerelement eines Kombinations Felds ab.
ms.assetid: 72b64135-e35a-4f72-9fc7-e6bedf495f23
keywords:
- Windows-Steuerelemente für CB_GETEDITSEL Meldung
topic_type:
- apiref
api_name:
- CB_GETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 319ce4a3c7a5a61903d4fc3bf04eed223e749787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040605"
---
# <a name="cb_geteditsel-message"></a>CB \_ geteditsel-Meldung

Ruft die Position des Anfangs-und des Endzeichens der aktuellen Auswahl im Bearbeitungs Steuerelement eines Kombinations Felds ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Zeiger auf einen **DWORD** -Wert, der die Anfangsposition der Auswahl empfängt. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf einen **DWORD** -Wert, der die Endposition der Auswahl empfängt. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein NULL basierter **DWORD** -Wert mit der Anfangsposition der Auswahl im [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) und mit der Endposition des ersten Zeichens nach dem letzten ausgewählten Zeichen im [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt zwei Möglichkeiten, den aktuellen Auswahlbereich abzurufen.


```C++
DWORD start, end;

// Get the range from [out] parameters.
// hwnd is the handle of the combo box control.
SendMessage(hwnd, CB_GETEDITSEL, (WPARAM)&start, (LPARAM)&end;

// Get the range from the return value.
DWORD range = SendMessage(hwnd, CB_GETEDITSEL, NULL, NULL);
start = LOWORD(range);
end = HIWORD(range);
```



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

[**CB- \_ Sekunden**](cb-seteditsel.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

