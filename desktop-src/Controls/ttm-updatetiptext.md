---
title: TTM_UPDATETIPTEXT Meldung (Commctrl.h)
description: Legt den QuickInfo-Text für ein Tool fest.
ms.assetid: 2a7432dd-76f9-42b4-b639-178dce1d89ef
keywords:
- TTM_UPDATETIPTEXT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TTM_UPDATETIPTEXT
- TTM_UPDATETIPTEXTA
- TTM_UPDATETIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c44b28d4913e4ae502db4d48268de945660610b374b7a1b98c0754fe99bafc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119542849"
---
# <a name="ttm_updatetiptext-message"></a>TTM \_ UPDATETIPTEXT-Nachricht

Legt den QuickInfo-Text für ein Tool fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TOOLINFO-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) Die **Hinst-** und **lpszText-Member** müssen das Instanzhandle und die Adresse des Texts angeben. Die **Member hwnd** und **uId** identifizieren das zu aktualisierende Tool. Der **cbSize-Member** dieser Struktur muss ausgefüllt werden, bevor diese Nachricht gesendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ UPDATETIPTEXTW** (Unicode) und **TTM \_ UPDATETIPTEXTA** (ANSI)<br/>       |



 

 





