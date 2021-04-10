---
title: TVM_SETINDENT Meldung (kommstrg. h)
description: Legt die Breite des Einzugs für ein Strukturansicht-Steuerelement fest und zeichnet das Steuerelement neu, um die neue Breite widerzuspiegeln. Sie können diese Nachricht explizit oder mithilfe des TreeView-Makros (TreeView) senden \_ .
ms.assetid: 377da8fe-c8e6-479b-a283-f1811cbc3e58
keywords:
- Windows-Steuerelemente für TVM_SETINDENT Meldung
topic_type:
- apiref
api_name:
- TVM_SETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85263c7c4330a692dc08949870a0eaa92f2b22c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104180"
---
# <a name="tvm_setindent-message"></a>TVM- \_ Meldung

Legt die Breite des Einzugs für ein Strukturansicht-Steuerelement fest und zeichnet das Steuerelement neu, um die neue Breite widerzuspiegeln. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ -Makros (TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) ) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Breite des Einzugs in Pixel. Wenn dieser Parameter kleiner als die vom System definierte Mindestbreite ist, wird die neue Breite auf das vom System definierte Minimalwert festgelegt.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Der vom System definierte minimale Einzugs Wert ist in der Regel fünf Pixel, aber er ist nicht korrigiert. Wenn Sie den genauen Wert für den minimalen Einzug auf einem bestimmten System abrufen möchten, senden Sie eine **TVM- \_ setIndent** -Nachricht, bei der *wParam* auf NULL festgelegt ist. Senden Sie dann eine [**TVM- \_ GetIndent**](tvm-getindent.md) -Nachricht, um den minimalen Einzug Wert abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TreeView- \_ Einzug**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
</dt> </dl>

 

 





