---
title: WM_CHANGEUISTATE Meldung (Winuser. h)
description: Eine Anwendung sendet die WM \_ changeuistate-Nachricht, um anzugeben, dass der Benutzeroberflächen Zustand geändert werden soll.
ms.assetid: d8dfc2fe-c64f-4e7e-b021-127aa85d5dd6
keywords:
- WM_CHANGEUISTATE von Meldungs Menüs und anderen Ressourcen
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
ms.openlocfilehash: 1cdfec2a26b3b3d160d3d207c338c8ebecd32bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743584"
---
# <a name="wm_changeuistate-message"></a>WM \_ changeuistate-Meldung

Eine Anwendung sendet die **WM \_ changeuistate** -Nachricht, um anzugeben, dass der Benutzeroberflächen Zustand geändert werden soll.


```C++
#define WM_CHANGEUISTATE                0x0127
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das nieder wertige Wort gibt die Aktion an, die durchgeführt werden soll. Dieser Member kann einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                   | Bedeutung                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <dt>**UIs \_ Löschen**</dt> <dt>2</dt> </dl>                | Die vom höherwertigen Wort angegebenen benutzeroberflächenstatusflags sollten gelöscht werden.<br/>                                                                  |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <dt>**UIs \_ Initialisieren**</dt> <dt>3</dt> </dl> | Die vom höherwertigen Wort angegebenen benutzeroberflächenstatusflags sollten basierend auf dem letzten Eingabe Ereignis geändert werden. Weitere Informationen finden Sie in den Hinweisen.<br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <dt>**UIs \_**</dt> <dt>1</dt> festlegen </dl>                      | Die vom höherwertigen Wort angegebenen benutzeroberflächenstatusflags müssen festgelegt werden.<br/>                                                                      |



 

Das hochwertige Wort gibt an, welche Benutzeroberflächen-Zustands Elemente betroffen sind, oder die Art des Steuer Elements. Dieser Member kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                     | Bedeutung                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <dt>**Uisf \_ Aktiv**</dt> <dt>0x4</dt> </dl>          | Ein Steuerelement sollte in dem Format gezeichnet werden, das für aktive Steuerelemente verwendet wird.<br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <dt>**Uisf \_ Hideaccel**</dt> <dt>0x2</dt> </dl> | Tastaturbeschleuniger werden ausgeblendet.<br/>                                |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <dt>**Uisf \_ Hidefocus**</dt> <dt>0x1</dt> </dl> | Fokus Indikatoren werden ausgeblendet.<br/>                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 sein.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Nachricht sollte von einem Fenster an sich selbst oder über das übergeordnete Fenster gesendet werden, wenn die Benutzeroberflächen-Zustands Elemente aller Fenster in derselben Hierarchie geändert werden müssen. Die Fenster Prozedur muss die Verarbeitung dieser Nachricht durch [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) zulassen, damit die gesamte Fenster Struktur einen konsistenten Benutzeroberflächen Zustand aufweist. Wenn das Fenster der obersten Ebene die **WM \_ changeuistate** -Nachricht empfängt, sendet es eine [**WM- \_ updateuistate**](wm-updateuistate.md) -Nachricht mit denselben Parametern an alle untergeordneten Fenster. Wenn das System die **WM- \_ updateuistate** -Nachricht verarbeitet, wird die Änderung im Zustand der Benutzeroberfläche vorgenommen.

Wenn das nieder wertige Wort von *wParam* "UIs \_ Initialize" lautet, sendet das System die [**WM- \_ updateuistate**](wm-updateuistate.md) -Nachricht mit einem UI-Status, der auf dem letzten Eingabe Ereignis basiert. Wenn z. b. die letzte Eingabe von der Maus stammt, werden die Tastatur-Cues vom System ausgeblendet. Und wenn die letzte Eingabe von der Tastatur stammt, zeigt das System die Tastatur Hinweise an. Wenn der Status, der sich aus der Verarbeitung von **WM \_ changeuistate** ergibt, mit dem alten Zustand identisch ist, wird diese Meldung von [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) nicht gesendet.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ queryuistate**](wm-queryuistate.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastaturkürzel](keyboard-accelerators.md)
</dt> </dl>

 

