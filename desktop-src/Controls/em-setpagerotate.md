---
title: EM_SETPAGEROTATE Meldung (RichEdit. h)
description: Legt das Text Layout für ein Rich-Edit-Steuerelement fest.
ms.assetid: 3c2a37fe-ee9f-4b34-87bf-7ac27d010afc
keywords:
- Windows-Steuerelemente für EM_SETPAGEROTATE Meldung
topic_type:
- apiref
api_name:
- EM_SETPAGEROTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eb595456bca444c92b536b0e428ee56a5903ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949777"
---
# <a name="em_setpagerotate-message"></a>EM \_ SETPAGEROTATE Meldung

\[**EM \_ SETPAGEROTATE** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]

Legt das Text Layout für ein Rich-Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Textlayoutwert. Dies kann einer der folgenden Werte sein:



| Wert                                                                                                                                       | Bedeutung                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="EPR_0"></span><span id="epr_0"></span><dl> <dt>**EPR \_ 0**</dt> </dl>       | Der Text fließt von links nach rechts und von oben nach unten.<br/>                              |
| <span id="EPR_90"></span><span id="epr_90"></span><dl> <dt>**EPR \_ 90**</dt> </dl>    | Der Text fließt von unten nach oben und von links nach rechts.<br/>                              |
| <span id="EPR_180"></span><span id="epr_180"></span><dl> <dt>**EPR \_ 180**</dt> </dl> | Der Text fließt von rechts nach links und von unten nach oben.<br/>                              |
| <span id="EPR_270"></span><span id="epr_270"></span><dl> <dt>**EPR \_ 270**</dt> </dl> | Der Text fließt von oben nach unten und von rechts nach links.<br/>                              |
| <span id="EPR_SE"></span><span id="epr_se"></span><dl> <dt>**EPR \_ SE**</dt> </dl>    | **Windows 8:** Text fließt von oben nach unten und von links nach rechts (Mongolisches Text Layout).<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der neue textlayoutwert.

## <a name="remarks"></a>Bemerkungen

Mit dieser Meldung wird das Text Layout für das gesamte Dokument festgelegt. Eingebettete Inhalte werden jedoch nicht gedreht und müssen separat von der Anwendung gedreht werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP1 \[ Desktop-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM- \_ GETPAGEROTATE**](em-getpagerotate.md)
</dt> </dl>

 

 





