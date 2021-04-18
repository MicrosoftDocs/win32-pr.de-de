---
title: WM_QUERYUISTATE Meldung (Winuser. h)
description: Eine Anwendung sendet die WM- \_ Abfrage queryuistate, um den Benutzeroberflächen Zustand für ein Fenster abzurufen.
ms.assetid: 3a9e3477-b5d7-4c55-b6d4-8a479451fee8
keywords:
- WM_QUERYUISTATE von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_QUERYUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1574fe0dab2a0885c8012bf19eed50facfd6cce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338805"
---
# <a name="wm_queryuistate-message"></a>WM \_ queryuistate-Meldung

Eine Anwendung sendet die **WM- \_ Abfrage queryuistate** , um den Benutzeroberflächen Zustand für ein Fenster abzurufen.


```C++
#define WM_QUERYUISTATE                 0x0129
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist **null** , wenn die Fokus Indikatoren und die Tastaturbeschleuniger sichtbar sind. Andernfalls kann der Rückgabewert einen oder mehrere der folgenden Werte aufweisen.



| Rückgabecode/-wert                                                                                                                                       | BESCHREIBUNG                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**Uisf \_ Aktiv**</dt> <dt>0x4</dt> </dl>    | Ein Steuerelement sollte in dem Format gezeichnet werden, das für aktive Steuerelemente verwendet wird.<br/> |
| <dl> <dt>**Uisf \_ Hideaccel**</dt> <dt>0x2</dt> </dl> | Tastaturbeschleuniger werden ausgeblendet.<br/>                                |
| <dl> <dt>**Uisf \_ Hidefocus**</dt> <dt>0x1</dt> </dl> | Fokus Indikatoren werden ausgeblendet.<br/>                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**WM \_ changeuistate**](wm-changeuistate.md)
</dt> <dt>

[**WM \_ updateuistate**](wm-updateuistate.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastaturkürzel](keyboard-accelerators.md)
</dt> </dl>

 

 





