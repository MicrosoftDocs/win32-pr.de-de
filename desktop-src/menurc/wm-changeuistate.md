---
title: WM_CHANGEUISTATE Meldung (Winuser.h)
description: Eine Anwendung sendet die WM \_ CHANGEUISTATE-Nachricht, um anzugeben, dass der Benutzeroberflächenzustand geändert werden soll.
ms.assetid: d8dfc2fe-c64f-4e7e-b021-127aa85d5dd6
keywords:
- WM_CHANGEUISTATE Meldung Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- WM_CHANGEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3849f9a5d2ccd0cec1bcaba4280e125ea01a669c8535c2dc520ebb98c3a3fcdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869710"
---
# <a name="wm_changeuistate-message"></a>WM \_ CHANGEUISTATE-Meldung

Eine Anwendung sendet die **WM \_ CHANGEUISTATE-Nachricht,** um anzugeben, dass der Benutzeroberflächenzustand geändert werden soll.


```C++
#define WM_CHANGEUISTATE                0x0127
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt die Aktion an, die ausgeführt werden soll. Dieser Member kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                   | Bedeutung                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <dt>**UIS \_ CLEAR**</dt> <dt>2</dt> </dl>                | Die vom Hochreihenfolgewort angegebenen Ui-Statusflags sollten gelöscht werden.<br/>                                                                  |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <dt>**UIS \_ INITIALIZE**</dt> <dt>3</dt> </dl> | Die vom Wort in hoher Reihenfolge angegebenen Ui-Statusflags sollten basierend auf dem letzten Eingabeereignis geändert werden. Weitere Informationen finden Sie in den Hinweisen.<br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <dt>**UIS \_ SET**</dt> <dt>1</dt> </dl>                      | Die vom Hochreihenfolgewort angegebenen Ui-Statusflags sollten festgelegt werden.<br/>                                                                      |



 

Das Wort in hoher Reihenfolge gibt an, welche Benutzeroberflächenzustandselemente oder das Format des Steuerelements betroffen sind. Bei diesem Member kann es sich um einen oder mehrere der folgenden Werte handelt.



| Wert                                                                                                                                                                                                                     | Bedeutung                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <dt>**UISF \_ ACTIVE**</dt> <dt>0x4</dt> </dl>          | Ein Steuerelement sollte im Stil gezeichnet werden, der für aktive Steuerelemente verwendet wird.<br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <dt>**UISF \_ HIDEACCEL-0x2**</dt> <dt></dt> </dl> | Tastaturbeschleunigungen werden ausgeblendet.<br/>                                |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt> </dl> | Fokusindikatoren werden ausgeblendet.<br/>                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 sein.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ein Fenster sollte diese Nachricht an sich selbst oder sein übergeordnetes Element senden, wenn es die Benutzeroberflächenzustandselemente aller Fenster in derselben Hierarchie ändern muss. Mit der Fensterprozedur muss [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) diese Meldung verarbeiten lassen, sodass die gesamte Fensterstruktur einen konsistenten Benutzeroberflächenzustand hat. Wenn das Fenster der obersten Ebene die **WM \_ CHANGEUISTATE-Nachricht** empfängt, sendet es eine [**WM \_ UPDATEUISTATE-Nachricht**](wm-updateuistate.md) mit den gleichen Parametern an alle untergeordneten Fenster. Wenn das System die **WM \_ UPDATEUISTATE-Nachricht** verarbeitet, nimmt es die Änderung im Benutzeroberflächenzustand vor.

Wenn das *wParam-Wort* in niedriger Reihenfolge UIS \_ INITIALIZE lautet, sendet das System die [**WM \_ UPDATEUISTATE-Nachricht**](wm-updateuistate.md) mit einem Benutzeroberflächenzustand basierend auf dem letzten Eingabeereignis. Wenn beispielsweise die letzte Eingabe von der Maus stammt, blendet das System die Tastaturhinweise aus. Und wenn die letzte Eingabe von der Tastatur stammt, zeigt das System die Tastaturhinweise an. Wenn der Status, der sich aus der Verarbeitung von **WM \_ CHANGEUISTATE** ergibt, mit dem alten Zustand identisch ist, sendet [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) diese Nachricht nicht.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ QUERYUISTATE**](wm-queryuistate.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Tastaturkürzel](keyboard-accelerators.md)
</dt> </dl>

 

