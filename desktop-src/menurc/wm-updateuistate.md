---
title: WM_UPDATEUISTATE-Nachricht (Winuser.h)
description: Eine Anwendung sendet die WM \_ UPDATEUISTATE-Nachricht, um den Benutzeroberflächenzustand für das angegebene Fenster und alle untergeordneten Fenster zu ändern.
ms.assetid: cbdeeddd-59b2-4a73-bfe9-17647d32bcf3
keywords:
- WM_UPDATEUISTATE Meldung Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- WM_UPDATEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 351770019f18c52c4ff1588a09c803d07f0f58ce032b35af53501ff4e47b6aed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112860"
---
# <a name="wm_updateuistate-message"></a>WM \_ UPDATEUISTATE-Meldung

Eine Anwendung sendet die **WM \_ UPDATEUISTATE-Nachricht,** um den Benutzeroberflächenzustand für das angegebene Fenster und alle untergeordneten Fenster zu ändern.


```C++
#define WM_UPDATEUISTATE                0x0128
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt die auszuführende Aktion an. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                   | Bedeutung                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <dt>**UIS \_ CLEAR**</dt> <dt>2</dt> </dl>                | Das vom Hochreihenfolgewort angegebene Benutzeroberflächenzustandselement sollte ausgeblendet werden.<br/>                                                                   |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <dt>**UIS \_ INITIALIZE**</dt> <dt>3</dt> </dl> | Das vom Wort in hoher Reihenfolge angegebene Benutzeroberflächenzustandselement sollte basierend auf dem letzten Eingabeereignis geändert werden. Weitere Informationen finden Sie in den Hinweisen.<br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <dt>**UIS \_ SET**</dt> <dt>1</dt> </dl>                      | Das vom Hochordnungswort angegebene Benutzeroberflächenzustandselement sollte sichtbar sein.<br/>                                                                  |



 

Das Wort in hoher Reihenfolge gibt an, welche Benutzeroberflächenzustandselemente oder das Format des Steuerelements betroffen sind. Bei diesem Parameter kann es sich um einen oder mehrere der folgenden Werte handelt.



| Wert                                                                                                                                                                                                                     | Bedeutung                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <dt>**UISF \_ ACTIVE**</dt> <dt>0x4</dt> </dl>          | Ein Steuerelement sollte im Stil gezeichnet werden, der für aktive Steuerelemente verwendet wird.<br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <dt>**UISF \_ HIDEACCEL-0x2**</dt> <dt></dt> </dl> | Tastenkombinationen.<br/>                                           |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt> </dl> | Fokusindikatoren.<br/>                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ein Fenster sollte diese Meldung senden, um den Benutzeroberflächenzustand aller untergeordneten Fenster zu ändern. Im Gegensatz zur [**WM \_ CHANGEUISTATE-Nachricht,**](wm-changeuistate.md) bei der es sich um eine Benachrichtigung handelt, ändert [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) die **WM \_ UPDATEUISTATE-Nachricht** und gibt die Änderungen an alle untergeordneten Fenster weiter.

Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) aktualisiert den Benutzeroberflächenzustand entsprechend dem *wParam-Wert.* Wenn der Benutzeroberflächenzustand geändert wird, sendet die Funktion die Meldung an alle unmittelbar untergeordneten Fenster. **DefWindowProc** sendet diese Nachricht auch, wenn sie eine [**WM \_ CHANGEUISTATE-Nachricht**](wm-changeuistate.md) empfängt, die das System darüber informiert, dass ein untergeordnetes Fenster den Benutzeroberflächenzustand ändern möchte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ CHANGEUISTATE**](wm-changeuistate.md)
</dt> <dt>

[**WM \_ QUERYUISTATE**](wm-queryuistate.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Tastaturkürzel](keyboard-accelerators.md)
</dt> </dl>

 

