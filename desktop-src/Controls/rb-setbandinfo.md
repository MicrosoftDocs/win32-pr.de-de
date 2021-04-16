---
title: RB_SETBANDINFO Meldung (kommstrg. h)
description: Legt die Eigenschaften eines vorhandenen Bands in einem Grund leisten-Steuerelement fest.
ms.assetid: 00021c35-612d-4278-b10c-6e9f1f45a543
keywords:
- Windows-Steuerelemente für RB_SETBANDINFO Meldung
topic_type:
- apiref
api_name:
- RB_SETBANDINFO
- RB_SETBANDINFOA
- RB_SETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e81377a40f8b6054f5d8cfae16837621b77b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477865"
---
# <a name="rb_setbandinfo-message"></a>RB \_ SetBandInfo-Meldung

Legt die Eigenschaften eines vorhandenen Bands in einem Grund leisten-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

NULL basierter Index des Bands, um die neuen Einstellungen zu erhalten.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur, die das zu ändernde Band und die neuen Einstellungen definiert. Vor dem Senden dieser Nachricht müssen Sie das **CBSIZE** -Element dieser Struktur auf die **sizeof**(REBARBANDINFO)-Struktur festlegen. Außerdem müssen Sie den **CCH** -Member der **REBARBANDINFO** -Struktur auf die Größe des **lpText** -Puffers festlegen, wenn rbbim- \_ Text angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **RB \_ Setbandinfow** (Unicode) und **RB \_ setbandinfoa** (ANSI)<br/>             |



 

 





