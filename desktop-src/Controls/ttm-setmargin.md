---
title: TTM_SETMARGIN (Commctrl.h)
description: Legt den oberen, linken, unteren und rechten Rand für ein QuickInfo-Fenster fest. Ein Rand ist der Abstand zwischen dem Rahmen des QuickInfo-Fensters und dem im QuickInfo-Fenster enthaltenen Text in Pixel.
ms.assetid: f1663861-c217-42dd-8249-7647b1651910
keywords:
- TTM_SETMARGIN meldungssteuerelemente Windows
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
ms.openlocfilehash: 04e5792b33f7f9f5a997759ba390c1b8a713308f95c4ba3f7b5cd0460747ff62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914060"
---
# <a name="ttm_setmargin-message"></a>TTM \_ SETMARGIN-Nachricht

Legt den oberen, linken, unteren und rechten Rand für ein QuickInfo-Fenster fest. Ein Rand ist der Abstand zwischen dem Rahmen des QuickInfo-Fensters und dem im QuickInfo-Fenster enthaltenen Text in Pixel.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die die zu setzenden Randinformationen enthält. Die Member der **RECT-Struktur** definieren kein umgebundenes Rechteck. Für diese Nachricht werden die Strukturmitglieder wie folgt interpretiert:



| Wert                                                                                                                                   | Bedeutung                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**top**</dt> </dl>          | Abstand zwischen dem oberen Rahmen und dem oberen Rand des QuickInfo-Texts in Pixel.<br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**Links**</dt> </dl>       | Abstand zwischen linker Rahmen und linker Seite des QuickInfo-Texts in Pixel.<br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <dt>**Unteres**</dt> </dl> | Abstand zwischen dem unteren Rahmen und dem unteren Rand des QuickInfo-Texts in Pixel.<br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <dt>**Richting**</dt> </dl>    | Abstand zwischen dem rechten Rahmen und dem rechten Ende des QuickInfo-Texts in Pixel.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Meldung wird nicht verwendet.

## <a name="remarks"></a>Hinweise

Diese Meldung hat keine Auswirkungen, wenn die Anwendung unter Windows Vista ausgeführt wird und visuelle Stile für die QuickInfo aktiviert sind. Sie können visuelle Stile für die QuickInfo deaktivieren, indem Sie [**SetWindowTheme verwenden.**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TTM \_ GETMARGIN**](ttm-getmargin.md)
</dt> </dl>

 

