---
title: TTM_GETMARGIN Meldung (kommstrg. h)
description: Ruft die oberen, linken, unteren und rechten Ränder für ein QuickInfo-Fenster ab. Ein Rand ist der Abstand zwischen dem QuickInfo-Fensterrahmen und dem im QuickInfo-Fenster enthaltenen Text in Pixel.
ms.assetid: c33ee1de-5fbd-4c7e-a703-576c2ffd3052
keywords:
- Windows-Steuerelemente für TTM_GETMARGIN Meldung
topic_type:
- apiref
api_name:
- TTM_GETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3e795d8eac14522f0994a342c7f781b7112ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956489"
---
# <a name="ttm_getmargin-message"></a>TTM \_ getMargin-Nachricht

Ruft die oberen, linken, unteren und rechten Ränder für ein QuickInfo-Fenster ab. Ein Rand ist der Abstand zwischen dem QuickInfo-Fensterrahmen und dem im QuickInfo-Fenster enthaltenen Text in Pixel.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Rand Informationen empfängt. Die Elemente der **Rect** -Struktur definieren kein Begrenzungs Rechteck. Für den Zweck dieser Nachricht werden die Strukturmember wie folgt interpretiert:



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

Alle vier Ränder werden standardmäßig auf 0 gesetzt, wenn Sie das ToolTip-Steuerelement erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TTM- \_ setMargin**](ttm-setmargin.md)
</dt> </dl>

 

