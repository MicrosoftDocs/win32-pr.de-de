---
title: TVM_SETBORDER Nachricht (Commctrl.h)
description: Legt die Größe des Rahmens für die Elemente in einem Strukturansichtssteuerelement fest. Sie können die Nachricht explizit oder mithilfe des TreeView \_ SetBorder-Makros senden.
ms.assetid: 468b46ae-2ab2-4753-a0af-7c644f75ce62
keywords:
- TVM_SETBORDER Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TVM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1c8cab133fb654e431638be96301325d68d9743109f84ed8def1ee9cc67c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669655"
---
# <a name="tvm_setborder-message"></a>TVM \_ SETBORDER-Nachricht

**Für die interne Verwendung vorgesehen; nicht für die Verwendung in Anwendungen empfohlen.**

Legt die Größe des Rahmens für die Elemente in einem Strukturansichtssteuerelement fest. Sie können die Nachricht explizit oder mithilfe des [**TreeView \_ SetBorder-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Aktionsflags. Bei diesem Parameter kann es sich um einen oder mehrere der folgenden Werte handelt:



| Wert                                                                                                                                                         | Bedeutung                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="TVSBF_XBORDER"></span><span id="tvsbf_xborder"></span><dl> <dt>**TVSBF \_ XBORDER**</dt> </dl> | Wendet die angegebene Rahmengröße auf die linke Seite der Elemente im Strukturansicht-Steuerelement an. <br/> |
| <span id="TVSBF_YBORDER"></span><span id="tvsbf_yborder"></span><dl> <dt>**TVSBF \_ YBORDER**</dt> </dl> | Wendet die angegebene Rahmengröße auf den Anfang der Elemente im Strukturansichtssteuerelement an.<br/>        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **SHORT-Wert,** der die Größe des linken Rahmens in Pixel angibt. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist ein **SHORT-Wert,** der die Größe des oberen Rahmens in Pixel angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **LONG-Wert** zurück, der die vorherige Rahmengröße in Pixel enthält. [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält die vorherige Größe des horizontalen Rahmens, und [**hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) enthält die vorherige Größe des vertikalen Rahmens.

## <a name="remarks"></a>Hinweise

**Sicherheitswarnung:** Die Verwendung dieser Meldung kann die Sicherheit Ihres Programms gefährden.

Der Elementrahmen wird nur zu Abstandszwecken festgelegt. Eine erfolgreiche Einstellung löst eine Neuberechnung der Bildlaufleisten aus.

Diese Meldung wird in zukünftigen Versionen von Comctl32.dll möglicherweise nicht mehr unterstützt. Außerdem ist diese Meldung in commctrl.h nicht definiert. Fügen Sie den Quelldateien Ihrer Anwendung die folgenden Definitionen hinzu, um die Nachricht zu verwenden:

``` syntax
#define TVM_SETBORDER (TV_FIRST + 35)
#define TVSBF_XBORDER 0x00000001
#define TVSBF_YBORDER 0x00000002 
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TreeView \_ SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
</dt> </dl>

 

