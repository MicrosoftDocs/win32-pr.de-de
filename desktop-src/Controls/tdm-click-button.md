---
title: TDM_CLICK_BUTTON Meldung (kommstrg. h)
description: Simuliert die Aktion eines Schaltflächen-Click in einem Aufgaben Dialogfeld.
ms.assetid: cc8a8252-3418-4a28-bfb7-11d6e3fee903
keywords:
- Windows-Steuerelemente für TDM_CLICK_BUTTON Meldung
topic_type:
- apiref
api_name:
- TDM_CLICK_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5933668eca907f36414113091b8901bfb9c110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345294"
---
# <a name="tdm_click_button-message"></a>TDM- \_ Click- \_ Schaltflächen Meldung

Simuliert die Aktion eines Schaltflächen-Click in einem Aufgaben Dialogfeld.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Ein **int** -Wert, der die ID der Schaltfläche angibt, auf die geklickt werden soll.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Bemerkungen

Die von *wParam* angegebene Schaltflächen-ID wird als Teil eines Benachrichtigungs Codes auf [TDN- \_ Schaltfläche \_](tdn-button-clicked.md) an die [**taskdialogcallbackproc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) -Rückruffunktion gesendet. Nachdem die Rückruffunktion zurückgegeben wurde, wird das Aufgaben Dialogfeld geschlossen, wenn S \_ OK von der Rückruffunktion zurückgegeben wurde. Wenn ' \_ false ' von der Rückruffunktion zurückgegeben wurde, bleibt das Aufgaben Dialogfeld aktiv.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

