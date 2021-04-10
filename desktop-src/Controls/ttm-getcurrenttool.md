---
title: TTM_GETCURRENTTOOL Meldung (kommstrg. h)
description: Ruft die Informationen für das aktuelle Tool in einem QuickInfo-Steuerelement ab.
ms.assetid: acb254cf-064c-4ed8-b488-a3138b648405
keywords:
- Windows-Steuerelemente für TTM_GETCURRENTTOOL Meldung
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
ms.openlocfilehash: 5fa6218bcb4ad9aa43c7ffba0d332786956d9a62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956490"
---
# <a name="ttm_getcurrenttool-message"></a>TTM \_ getcurrenttool-Meldung

Ruft die Informationen für das aktuelle Tool in einem QuickInfo-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur, die Informationen über das aktuelle Tool empfängt. Wenn dieser Wert **null** ist, gibt der Rückgabewert an, dass das aktuelle Tool vorhanden ist, ohne dass die Tool Informationen tatsächlich abgerufen werden. Wenn dieser Wert nicht **null** ist, muss das **CBSIZE** -Element der **toolinfo** -Struktur ausgefüllt werden, bevor diese Nachricht gesendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL. Wenn *LPARAM* gleich **null** ist, gibt einen Wert ungleich 0 (null) zurück, wenn ein aktuelles Tool vorhanden ist, andernfalls NULL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ Getcurrenttoolw** (Unicode) und **TTM \_ getcurrenttola** (ANSI)<br/>     |



 

 





