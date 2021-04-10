---
title: TTM_UPDATETIPTEXT Meldung (kommstrg. h)
description: Legt den QuickInfo-Text für ein Tool fest.
ms.assetid: 2a7432dd-76f9-42b4-b639-178dce1d89ef
keywords:
- Windows-Steuerelemente für TTM_UPDATETIPTEXT Meldung
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
ms.openlocfilehash: f6c94b14ec83c190ce019ecba1413d2fa05f0103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104433"
---
# <a name="ttm_updatetiptext-message"></a>TTM- \_ updatetiptext-Nachricht

Legt den QuickInfo-Text für ein Tool fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur. Die **hInst** -und **lpszText** -Member müssen den Instanzhandle und die Adresse des Texts angeben. Das zu aktualisierenden Tool wird durch die **HWND** -und **UID** -Mitglieder identifiziert Der **CBSIZE** -Member dieser Struktur muss ausgefüllt werden, bevor diese Nachricht gesendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ Updatetiptextw** (Unicode) und **TTM \_ updatetiptexta** (ANSI)<br/>       |



 

 





