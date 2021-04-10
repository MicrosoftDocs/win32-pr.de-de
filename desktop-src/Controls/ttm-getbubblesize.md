---
title: TTM_GETBUBBLESIZE Meldung (kommstrg. h)
description: Gibt die Breite und Höhe eines QuickInfo-Steuer Elements zurück.
ms.assetid: 6afb971e-f05d-4b7a-b63d-3672bfcc32dc
keywords:
- Windows-Steuerelemente für TTM_GETBUBBLESIZE Meldung
topic_type:
- apiref
api_name:
- TTM_GETBUBBLESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48b48bda0f795473cb48303e88bbf3c1c35df7cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103749"
---
# <a name="ttm_getbubblesize-message"></a>TTM \_ getbubblesize-Meldung

Gibt die Breite und Höhe eines QuickInfo-Steuer Elements zurück.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf die [**QuickInfo-toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Breite der QuickInfo im unteren Wort und die Höhe im großen Wort zurück, wenn erfolgreich. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn die "ttf \_ Track"-und "ttf absolute"- \_ Flags im **uFlags** -Member der [**QuickInfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur festgelegt sind, kann diese Meldung verwendet werden, um die QuickInfo korrekt zu positionieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





