---
title: TVM_SETBORDER Meldung (kommstrg. h)
description: Legt die Größe des Rahmens für die Elemente in einem Strukturansicht-Steuerelement fest. Sie können die Nachricht explizit oder mithilfe des TreeView \_ setborder-Makros senden.
ms.assetid: 468b46ae-2ab2-4753-a0af-7c644f75ce62
keywords:
- Windows-Steuerelemente für TVM_SETBORDER Meldung
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
ms.openlocfilehash: 6b4401959e2579caab7f2cb4b6eed1ea34481ffa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859000"
---
# <a name="tvm_setborder-message"></a>TVM- \_ setborder-Meldung

**Zur internen Verwendung vorgesehen. wird nicht für die Verwendung in Anwendungen empfohlen.**

Legt die Größe des Rahmens für die Elemente in einem Strukturansicht-Steuerelement fest. Sie können die Nachricht explizit oder mithilfe des [**TreeView \_ setborder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Aktionsflags. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen:



| Wert                                                                                                                                                         | Bedeutung                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="TVSBF_XBORDER"></span><span id="tvsbf_xborder"></span><dl> <dt>**tvsbf- \_ xborder**</dt> </dl> | Wendet die angegebene Rahmengröße auf die linke Seite der Elemente im Strukturansicht-Steuerelement an. <br/> |
| <span id="TVSBF_YBORDER"></span><span id="tvsbf_yborder"></span><dl> <dt>**tvsbf \_ yborder**</dt> </dl> | Wendet die angegebene Rahmengröße auf den oberen Rand der Elemente im Strukturansicht-Steuerelement an.<br/>        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist ein **kurzes** , das die Größe des linken Rahmens in Pixel angibt. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist ein **kurzes** , das die Größe des oberen Rahmens in Pixel angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **Long** -Wert zurück, der die vorherige Rahmengröße in Pixel enthält. Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält die vorherige Größe des horizontalen Rahmens, und das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) enthält die vorherige Größe des vertikalen Rahmens.

## <a name="remarks"></a>Bemerkungen

**Sicherheitswarnung:** Die Verwendung dieser Nachricht kann die Sicherheit des Programms beeinträchtigen.

Der Element Rahmen wird nur für Abstands Zwecke festgelegt. Eine erfolgreiche Einstellung löst eine Neuberechnung der Schiebe leisten aus.

Diese Meldung wird in zukünftigen Versionen von Comctl32.dll möglicherweise nicht mehr unterstützt. Außerdem ist diese Meldung nicht in "kommctrl. h" definiert. Fügen Sie den Quelldateien Ihrer Anwendung die folgenden Definitionen hinzu, um die Meldung zu verwenden:

``` syntax
#define TVM_SETBORDER (TV_FIRST + 35)
#define TVSBF_XBORDER 0x00000001
#define TVSBF_YBORDER 0x00000002 
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TreeView \_ setborder**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
</dt> </dl>

 

