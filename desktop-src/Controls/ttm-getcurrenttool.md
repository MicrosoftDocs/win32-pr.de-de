---
title: TTM_GETCURRENTTOOL Meldung (Commctrl.h)
description: Ruft die Informationen für das aktuelle Tool in einem QuickInfo-Steuerelement ab.
ms.assetid: acb254cf-064c-4ed8-b488-a3138b648405
keywords:
- TTM_GETCURRENTTOOL Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TTM_GETCURRENTTOOL
- TTM_GETCURRENTTOOLA
- TTM_GETCURRENTTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4558e582e4619cd7d96380a1e38e2efe68808b9241e4c627e12a74946965d8de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769340"
---
# <a name="ttm_getcurrenttool-message"></a>TTM \_ GETCURRENTTOOL-Nachricht

Ruft die Informationen für das aktuelle Tool in einem QuickInfo-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TOOLINFO-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) die Informationen zum aktuellen Tool empfängt. Wenn dieser Wert **NULL** ist, gibt der Rückgabewert das Vorhandensein des aktuellen Tools an, ohne die Toolinformationen tatsächlich abzurufen. Wenn dieser Wert nicht **NULL** ist, muss der **cbSize-Member** der **TOOLINFO-Struktur** ausgefüllt werden, bevor diese Nachricht gesendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück. Andernfalls wird 0 (null) zurückgegeben. Wenn *lParam* **NULL** ist, gibt einen Wert ungleich 0 (null) zurück, wenn ein aktuelles Tool vorhanden ist, andernfalls 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ GETCURRENTTOOLW** (Unicode) und **TTM \_ GETCURRENTTOOLA** (ANSI)<br/>     |



 

 





