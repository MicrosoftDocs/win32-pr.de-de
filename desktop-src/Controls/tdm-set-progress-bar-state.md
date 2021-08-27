---
title: TDM_SET_PROGRESS_BAR_STATE (Commctrl.h)
description: Legt den Status der Statusleiste in einem Aufgabendialogfeld fest.
ms.assetid: 8b0f2ee9-e6ca-4a5b-8687-6e2682eda7d0
keywords:
- TDM_SET_PROGRESS_BAR_STATE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb3be7432ac3a93af4f27fe9b06dced50fc6c77c0176c3bff7419cf15f2c73ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104530"
---
# <a name="tdm_set_progress_bar_state-message"></a>TDM \_ SET PROGRESS BAR \_ \_ \_ STATE-Meldung

Legt den Status der Statusleiste in einem Aufgabendialogfeld fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Ein **Wert vom Wert int,** der den Status der Statusleiste angibt. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                   | Bedeutung                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <dt>**PBST \_ NORMAL**</dt> </dl> | Legt die Statusleiste auf den normalen Zustand fest.<br/> |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <dt>**PBST \_ PAUSED**</dt> </dl>    | Legt die Statusleiste auf den angehaltenen Zustand fest.<br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <dt>**\_PBST-FEHLER**</dt> </dl>    | Legen Sie die Statusleiste auf den Fehlerzustand fest.<br/>   |



 

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nicht 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null. Rufen Sie GetLastError auf, um erweiterte Fehlerinformationen zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





