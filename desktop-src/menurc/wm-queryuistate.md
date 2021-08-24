---
title: WM_QUERYUISTATE-Nachricht (Winuser.h)
description: Eine Anwendung sendet die WM \_ QUERYUISTATE-Nachricht, um den Benutzeroberflächenzustand für ein Fenster abzurufen.
ms.assetid: 3a9e3477-b5d7-4c55-b6d4-8a479451fee8
keywords:
- WM_QUERYUISTATE Meldung Menüs und andere Ressourcen
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
ms.openlocfilehash: e62fc33fb79594f3e07c0d44d4b25fd16e980ef3a4a89b3079c69ef6eb5d1b89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119267910"
---
# <a name="wm_queryuistate-message"></a>WM \_ QUERYUISTATE-Nachricht

Eine Anwendung sendet die **WM \_ QUERYUISTATE-Nachricht,** um den Benutzeroberflächenzustand für ein Fenster abzurufen.


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

Der Rückgabewert ist **NULL,** wenn die Fokusindikatoren und die Tastenkombinationen sichtbar sind. Andernfalls kann der Rückgabewert einer oder mehrere der folgenden Werte sein.



| Rückgabecode/-wert                                                                                                                                       | BESCHREIBUNG                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**UISF \_ ACTIVE**</dt> <dt>0x4</dt> </dl>    | Ein Steuerelement sollte im Stil gezeichnet werden, der für aktive Steuerelemente verwendet wird.<br/> |
| <dl> <dt>**UISF \_ HIDEACCEL-0x2**</dt> <dt></dt> </dl> | Tastaturbeschleunigungen werden ausgeblendet.<br/>                                |
| <dl> <dt>**UISF \_ HIDEFOCUS-0x1**</dt> <dt></dt> </dl> | Fokusindikatoren werden ausgeblendet.<br/>                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**WM \_ CHANGEUISTATE**](wm-changeuistate.md)
</dt> <dt>

[**WM \_ UPDATEUISTATE**](wm-updateuistate.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Tastaturkürzel](keyboard-accelerators.md)
</dt> </dl>

 

 





