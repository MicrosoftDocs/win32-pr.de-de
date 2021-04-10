---
title: WM_UPDATEUISTATE Meldung (Winuser. h)
description: Eine Anwendung sendet die WM \_ -updateuistate-Meldung, um den Benutzeroberflächen Status für das angegebene Fenster und alle untergeordneten Fenster zu ändern.
ms.assetid: cbdeeddd-59b2-4a73-bfe9-17647d32bcf3
keywords:
- WM_UPDATEUISTATE von Meldungs Menüs und anderen Ressourcen
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
ms.openlocfilehash: 003d9ca45b357a7d0ebc172000b1e2c01505db8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106454"
---
# <a name="wm_updateuistate-message"></a>WM \_ updateuistate-Meldung

Eine Anwendung sendet die **WM- \_ updateuistate** -Meldung, um den Benutzeroberflächen Status für das angegebene Fenster und alle untergeordneten Fenster zu ändern.


```C++
#define WM_UPDATEUISTATE                0x0128
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das nieder wertige Wort gibt die Aktion an, die ausgeführt werden soll. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                   | Bedeutung                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <dt>**UIs \_ Löschen**</dt> <dt>2</dt> </dl>                | Das Benutzeroberflächen-Zustands Element, das durch das hochwertige Wort angegeben wird, sollte ausgeblendet werden.<br/>                                                                   |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <dt>**UIs \_ Initialisieren**</dt> <dt>3</dt> </dl> | Das Benutzeroberflächen-Zustands Element, das durch das hochwertige Wort angegeben wird, sollte basierend auf dem letzten Eingabe Ereignis geändert werden. Weitere Informationen finden Sie in den Hinweisen.<br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <dt>**UIs \_**</dt> <dt>1</dt> festlegen </dl>                      | Das Benutzeroberflächen-Zustands Element, das durch das hochwertige Wort angegeben wird, sollte sichtbar sein.<br/>                                                                  |



 

Das hochwertige Wort gibt an, welche Benutzeroberflächen-Zustands Elemente betroffen sind, oder die Art des Steuer Elements. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                     | Bedeutung                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <dt>**Uisf \_ Aktiv**</dt> <dt>0x4</dt> </dl>          | Ein Steuerelement sollte in dem Format gezeichnet werden, das für aktive Steuerelemente verwendet wird.<br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <dt>**Uisf \_ Hideaccel**</dt> <dt>0x2</dt> </dl> | Tastaturbeschleuniger.<br/>                                           |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <dt>**Uisf \_ Hidefocus**</dt> <dt>0x1</dt> </dl> | Fokus Indikatoren.<br/>                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Meldung sollte von einem Fenster gesendet werden, um den Benutzeroberflächen Status aller untergeordneten Fenster zu ändern. Im Gegensatz zur " [**WM \_ changeuistate**](wm-changeuistate.md) "-Meldung, bei der es sich um eine Benachrichtigung handelt, wird der Benutzeroberflächen Zustand geändert, wenn [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) die " **WM \_ updateuistate** "-Meldung verarbeitet und die Änderungen an alle untergeordneten Fenster weitergegeben.

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion aktualisiert den UI-Status gemäß dem *wParam* -Wert. Wenn der Zustand der Benutzeroberfläche geändert wird, sendet die Funktion die Nachricht an alle unmittelbaren untergeordneten Fenster. **Defwindowproc** sendet diese Nachricht auch dann, wenn Sie eine [**WM \_ changeuistate**](wm-changeuistate.md) -Meldung empfängt, in der das System darüber benachrichtigt wird, dass ein untergeordnetes Fenster den Benutzeroberflächen Zustand ändern soll.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ changeuistate**](wm-changeuistate.md)
</dt> <dt>

[**WM \_ queryuistate**](wm-queryuistate.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Tastaturkürzel](keyboard-accelerators.md)
</dt> </dl>

 

