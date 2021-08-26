---
description: Wird an das Fenster mit dem Fokus gesendet, wenn der Benutzer eine neue Eingabesprache ausgibt, entweder mit dem Hotkey (angegeben in der Tastatursteuerungsanwendung) oder aus dem Indikator auf der Systemtaskleiste.
ms.assetid: db38c31c-6ae4-4401-82b8-7fd220c1678c
title: WM_INPUTLANGCHANGEREQUEST-Nachricht (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644fa4764c5172edc34f16509c6a6b00be6356b80c460a08233be8aa64ef69c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056060"
---
# <a name="wm_inputlangchangerequest-message"></a>WM \_ INPUTLANGCHANGEREQUEST-Nachricht

Wird an das Fenster mit dem Fokus gesendet, wenn der Benutzer eine neue Eingabesprache ausgibt, entweder mit dem Hotkey (angegeben in der Tastatursteuerungsanwendung) oder aus dem Indikator auf der Systemtaskleiste. Eine Anwendung kann die Änderung akzeptieren, indem sie die Nachricht an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergibt oder die Änderung ablehnt (und verhindert, dass sie stattfindet), indem sie sofort zurückgibt.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_INPUTLANGCHANGEREQUEST       0x0050
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das neue Eingabeschema. Dieser Parameter kann eine Kombination der folgenden Flags sein.



| Wert                                                                                                                                                                                                                                                            | Bedeutung                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INPUTLANGCHANGE_BACKWARD"></span><span id="inputlangchange_backward"></span><dl> <dt>**INPUTLANGCHANGE \_ BACKWARD**</dt> <dt>0x0004</dt> </dl>       | Ein Hot-Key wurde verwendet, um das vorherige Eingabeschema in der installierten Liste der Eingabeschemas auszuwählen. Dieses Flag kann nicht mit dem INPUTLANGCHANGE \_ FORWARD-Flag verwendet werden.<br/> |
| <span id="INPUTLANGCHANGE_FORWARD"></span><span id="inputlangchange_forward"></span><dl> <dt>**INPUTLANGCHANGE \_ FORWARD**</dt> <dt>0x0002</dt> </dl>          | Ein Hot-Key wurde verwendet, um das nächste Eingabeschema in der installierten Liste der Eingabeschemas auszuwählen. Dieses Flag kann nicht mit dem INPUTLANGCHANGE \_ BACKWARD-Flag verwendet werden.<br/>    |
| <span id="INPUTLANGCHANGE_SYSCHARSET"></span><span id="inputlangchange_syscharset"></span><dl> <dt>**INPUTLANGCHANGE \_ SYSCHARSET**</dt> <dt>0x0001</dt> </dl> | Das Tastaturlayout des neuen Eingabeschemas kann mit dem Systemzeichensatz verwendet werden.<br/>                                                                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Der Bezeichner des Eingabeschemas. Weitere Informationen finden Sie unter [Sprachen, Gebietsschemas und Tastaturlayouts.](../inputdev/about-keyboard-input.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Diese Nachricht wird nicht an die Anwendung gesendet, sodass der Rückgabewert ignoriert wird. Um die Änderung zu akzeptieren, sollte die Anwendung die Nachricht an [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben. Um die Änderung abzulehnen, sollte die Anwendung null zurückgeben, ohne **DefWindowProc** aufzurufen.

## <a name="remarks"></a>Hinweise

Wenn die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) die **WM \_ INPUTLANGCHANGEREQUEST-Nachricht** empfängt, aktiviert sie das neue Eingabegebietsschema und benachrichtigt die Anwendung über die Änderung, indem die [**WM \_ INPUTLANGCHANGE-Nachricht**](wm-inputlangchange.md) gesendet wird.

Der Sprachindikator ist auf der Taskleiste nur vorhanden, wenn Sie mehr als ein Tastaturlayout installiert haben und wenn Sie den Indikator mithilfe der Tastatursteuerungsanwendung aktiviert haben.

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

[**WM \_ INPUTLANGCHANGE**](wm-inputlangchange.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
