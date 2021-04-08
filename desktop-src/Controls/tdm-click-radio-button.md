---
title: TDM_CLICK_RADIO_BUTTON Meldung (kommstrg. h)
description: Simuliert die Aktion eines Options Felds in einem Aufgaben Dialogfeld.
ms.assetid: ad1616fc-f64d-4575-8bd1-7ce63185d725
keywords:
- Windows-Steuerelemente für TDM_CLICK_RADIO_BUTTON Meldung
topic_type:
- apiref
api_name:
- TDM_CLICK_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b76d465b1b937359a3d312a401914d497f9c9b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957099"
---
# <a name="tdm_click_radio_button-message"></a>TDM-Click-Optionsfeld \_ \_ \_ Meldung

Simuliert die Aktion eines Options Felds in einem Aufgaben Dialogfeld.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Ein **int** -Wert, der die ID des Options Felds angibt, auf das geklickt werden soll.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Bemerkungen

Die angegebene Optionsfeld-ID wird an die [**taskdialogcallbackproc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) -Rückruffunktion als Teil eines von [TDN \_ \_ \_ angeklickten](tdn-radio-button-clicked.md) Benachrichtigungs Codes gesendet. Nachdem die Rückruffunktion zurückgegeben wurde, wird das Optionsfeld ausgewählt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

