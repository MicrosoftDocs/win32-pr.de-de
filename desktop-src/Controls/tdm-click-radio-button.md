---
title: TDM_CLICK_RADIO_BUTTON Meldung (Commctrl.h)
description: Simuliert die Aktion eines Optionsfeldklicks in einem Aufgabendialogfeld.
ms.assetid: ad1616fc-f64d-4575-8bd1-7ce63185d725
keywords:
- TDM_CLICK_RADIO_BUTTON Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 80c1eb7e72030a3c2dadc61bfd90027dab032c3342a25c72e4da9dd9a7338142
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104660"
---
# <a name="tdm_click_radio_button-message"></a>TDM CLICK RADIO BUTTON message (TDM \_ CLICK \_ RADIO \_ BUTTON-Meldung)

Simuliert die Aktion eines Optionsfeldklicks in einem Aufgabendialogfeld.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Ein **int-Wert,** der die ID des Optionsfelds angibt, auf das geklickt werden soll.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Hinweise

Die angegebene Optionsfeld-ID wird als Teil eines [TDN RADIO BUTTON \_ \_ CLICKED-Benachrichtigungscodes \_](tdn-radio-button-clicked.md) an die [**Rückruffunktion TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) gesendet. Nachdem die Rückruffunktion zurückgegeben wurde, wird das Optionsfeld ausgewählt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

