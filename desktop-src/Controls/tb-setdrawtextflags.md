---
title: TB_SETDRAWTEXTFLAGS Meldung (kommstrg. h)
description: Legt die textzeichenflags für die Symbolleiste fest.
ms.assetid: b088af32-ea8a-4304-89f1-a7cec5497f85
keywords:
- Windows-Steuerelemente für TB_SETDRAWTEXTFLAGS Meldung
topic_type:
- apiref
api_name:
- TB_SETDRAWTEXTFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890a24239ff2257ffaccff6613b3765711b2ef7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956877"
---
# <a name="tb_setdrawtextflags-message"></a>TB \_ setdrawtextflags-Meldung

Legt die textzeichenflags für die Symbolleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein oder mehrere der \_ in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext)angegebenen dt-Flags, die angeben, welche Bits in *LPARAM* verwendet werden, wenn der Text gezeichnet wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Mindestens eines der \_ in [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext)angegebenen dt-Flags, die angeben, wie der Schaltflächen Text gezeichnet wird. Dieser Wert wird an die **DrawText** -Funktion übermittelt, wenn der Schaltflächen Text gezeichnet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherigen textzeichenflags zurück.

## <a name="remarks"></a>Bemerkungen

Mit dem *wParam* -Parameter können Sie angeben, welche Flags verwendet werden, wenn der Text gezeichnet wird, auch wenn diese Flags ausgeschaltet sind. Wenn Sie z. b. nicht möchten, dass beim Zeichnen von Text das Flag dt Center \_ verwendet wird, fügen Sie \_ *wParam* das Flag dt Center hinzu, und geben Sie \_ in *LPARAM* nicht das Flag dt Center an. Dadurch wird verhindert, dass das Steuerelement das DT \_ Center-Flag an die [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) -Funktion übergibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

