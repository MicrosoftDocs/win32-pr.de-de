---
title: TTM_SETMARGIN Meldung (kommstrg. h)
description: Legt die oberen, linken, unteren und rechten Ränder für ein QuickInfo-Fenster fest. Ein Rand ist der Abstand zwischen dem QuickInfo-Fensterrahmen und dem im QuickInfo-Fenster enthaltenen Text in Pixel.
ms.assetid: f1663861-c217-42dd-8249-7647b1651910
keywords:
- Windows-Steuerelemente für TTM_SETMARGIN Meldung
topic_type:
- apiref
api_name:
- TTM_SETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed46bf40833a3046d15386782897eb6b573b29c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338732"
---
# <a name="ttm_setmargin-message"></a>TTM- \_ setMargin-Nachricht

Legt die oberen, linken, unteren und rechten Ränder für ein QuickInfo-Fenster fest. Ein Rand ist der Abstand zwischen dem QuickInfo-Fensterrahmen und dem im QuickInfo-Fenster enthaltenen Text in Pixel.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die zu festzulegenden Rand Informationen enthält. Die Elemente der **Rect** -Struktur definieren kein Begrenzungs Rechteck. Für den Zweck dieser Nachricht werden die Strukturmember wie folgt interpretiert:



| Wert                                                                                                                                   | Bedeutung                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**top**</dt> </dl>          | Abstand zwischen dem oberen und oberen Rand des QuickInfo-Texts in Pixel.<br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**linken**</dt> </dl>       | Abstand zwischen dem linken Rand und dem linken Ende des QuickInfo-Texts in Pixel.<br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <dt>**unten**</dt> </dl> | Abstand zwischen dem unteren und dem unteren Rand des QuickInfo-Texts in Pixel.<br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <dt>**Richting**</dt> </dl>    | Abstand zwischen dem rechten Rand und dem rechten Ende des QuickInfo-Texts in Pixel.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Diese Nachricht hat keine Auswirkung, wenn die Anwendung unter Windows Vista ausgeführt wird und visuelle Stile für die QuickInfo aktiviert sind. Sie können visuelle Stile für die QuickInfo mithilfe von [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme)deaktivieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TTM \_ getMargin**](ttm-getmargin.md)
</dt> </dl>

 

