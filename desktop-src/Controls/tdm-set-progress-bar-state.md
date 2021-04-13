---
title: TDM_SET_PROGRESS_BAR_STATE Meldung (kommstrg. h)
description: Legt den Zustand der Statusanzeige in einem Aufgaben Dialogfeld fest.
ms.assetid: 8b0f2ee9-e6ca-4a5b-8687-6e2682eda7d0
keywords:
- Windows-Steuerelemente für TDM_SET_PROGRESS_BAR_STATE Meldung
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
ms.openlocfilehash: 00f0ae4ec104c8472d3640aa804650640d77cc63
ms.sourcegitcommit: e584514ced7396dde55e58501c8c8a872229acc4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2021
ms.locfileid: "104352038"
---
# <a name="tdm_set_progress_bar_state-message"></a>TDM \_ - \_ \_ \_ Statusmeldung "Statusleiste festlegen"

Legt den Zustand der Statusanzeige in einem Aufgaben Dialogfeld fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Ein **int** -Wert, der den Status der Statusanzeige angibt. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                   | Bedeutung                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <dt>**PBST \_ Normal**</dt> </dl> | Legt die Statusanzeige auf den normalen Zustand fest.<br/> |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <dt>**PBST \_ angehalten**</dt> </dl>    | Legt die Statusanzeige auf den angehaltenen Zustand fest.<br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <dt>**PBST- \_ Fehler**</dt> </dl>    | Legen Sie die Statusanzeige auf den Fehlerstatus fest.<br/>   |



 

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null. Um erweiterte Fehlerinformationen abzurufen, nennen Sie GetLastError.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





