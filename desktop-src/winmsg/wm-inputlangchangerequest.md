---
description: Wird an das Fenster mit dem Fokus gesendet, wenn der Benutzer eine neue Eingabe Sprache auswählt, entweder mit dem Hotkey (angegeben in der System Steuerungsanwendung der Tastatur) oder über den Indikator auf der Taskleiste des Systems.
ms.assetid: db38c31c-6ae4-4401-82b8-7fd220c1678c
title: WM_INPUTLANGCHANGEREQUEST Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df361c479978083c29281764e65c48b131c22b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348619"
---
# <a name="wm_inputlangchangerequest-message"></a>WM- \_ inputlangchangerequest-Nachricht

Wird an das Fenster mit dem Fokus gesendet, wenn der Benutzer eine neue Eingabe Sprache auswählt, entweder mit dem Hotkey (angegeben in der System Steuerungsanwendung der Tastatur) oder über den Indikator auf der Taskleiste des Systems. Eine Anwendung kann die Änderung akzeptieren, indem Sie die Nachricht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergibt oder die Änderung ablehnt (und Sie nicht findet), indem Sie sofort zurückgegeben wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_INPUTLANGCHANGEREQUEST       0x0050
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das neue Eingabe Gebiets Schema. Dieser Parameter kann eine Kombination der folgenden Flags sein.



| Wert                                                                                                                                                                                                                                                            | Bedeutung                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INPUTLANGCHANGE_BACKWARD"></span><span id="inputlangchange_backward"></span><dl> <dt>**Inputlangchange \_ Rückwärts**</dt> <dt>0x0004</dt> </dl>       | Eine "Hot Key" wurde verwendet, um das vorherige Eingabe Gebiets Schema in der installierten Liste der Eingabe Gebiets Schemata auszuwählen. Dieses Flag kann nicht mit dem inputlangchange- \_ Forward-Flag verwendet werden.<br/> |
| <span id="INPUTLANGCHANGE_FORWARD"></span><span id="inputlangchange_forward"></span><dl> <dt>**Inputlangchange \_ Weiterleiten**</dt> <dt>0x0002</dt> </dl>          | Eine "Hot Key" wurde verwendet, um das nächste Eingabe Gebiets Schema in der installierten Liste der Eingabe Gebiets Schemata auszuwählen. Dieses Flag kann nicht mit dem inputlangchange-abwärts Flag verwendet werden \_ .<br/>    |
| <span id="INPUTLANGCHANGE_SYSCHARSET"></span><span id="inputlangchange_syscharset"></span><dl> <dt>**Inputlangchange \_ Syscharset**</dt> <dt>0x0001</dt> </dl> | Das Tastaturlayout des neuen Eingabe Gebiets Schemas kann mit dem System Zeichensatz verwendet werden.<br/>                                                                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Der Eingabe Gebiets Schema Bezeichner. Weitere Informationen finden Sie unter [Sprachen, Gebiets Schemas und Tastatur Layouts](../inputdev/about-keyboard-input.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Diese Nachricht wird gesendet, nicht an die Anwendung gesendet, sodass der Rückgabewert ignoriert wird. Um die Änderung zu übernehmen, sollte die Anwendung die Nachricht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben. Um die Änderung abzulehnen, sollte die Anwendung 0 (null) zurückgeben, ohne **defwindowproc** aufrufen zu müssen.

## <a name="remarks"></a>Bemerkungen

Wenn die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die " **WM \_ inputlangchangerequest** "-Nachricht empfängt, aktiviert Sie das neue Eingabe Gebiets Schema und benachrichtigt die Anwendung über die Änderung, indem die " [**WM \_ inputlangchange**](wm-inputlangchange.md) "-Meldung gesendet wird.

Der Sprachindikator ist nur auf der Taskleiste vorhanden, wenn Sie mehr als ein Tastaturlayout installiert haben und Sie den Indikator mithilfe der System Steuerungsanwendung der Tastatur aktiviert haben.

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

[**WM \_ inputlangchange**](wm-inputlangchange.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
