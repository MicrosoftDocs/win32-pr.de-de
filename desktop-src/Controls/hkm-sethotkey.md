---
title: HKM_SETHOTKEY Meldung (Commctrl.h)
description: Legt die Tastenkombination für ein Hot-Key-Steuerelement fest.
ms.assetid: 372a7b2f-d9d5-43a8-9c06-730f2f5dc56e
keywords:
- HKM_SETHOTKEY Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- HKM_SETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae397e3034e917eec85a6b56397cbac8b14a59af03aca6ebee08fec89cf6b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672258"
---
# <a name="hkm_sethotkey-message"></a>HKM \_ SETHOTKEY-Nachricht

Legt die Tastenkombination für ein Hot-Key-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der [**LOBYTE-Wert**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) von [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist der virtuelle Schlüsselcode des Hot-Schlüssels. Der [**HIBYTE-Wert**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) von **LOWORD** ist der Schlüsselmodifizierer, der die Schlüssel angibt, die eine Tastenkombination definieren. Eine Liste der Modifiziererflagwerte finden Sie in der Beschreibung der [**HKM \_ GETHOTKEY-Nachricht.**](hkm-gethotkey.md)

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es wird immer NULL zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

