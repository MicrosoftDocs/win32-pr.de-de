---
title: TTM_TRACKPOSITION Meldung (kommstrg. h)
description: Legt die Position einer nach Verfolgungs-QuickInfo fest.
ms.assetid: 9eb7c86c-78e6-442a-ad77-5fb919cab591
keywords:
- Windows-Steuerelemente für TTM_TRACKPOSITION Meldung
topic_type:
- apiref
api_name:
- TTM_TRACKPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6eab8184049d8bf876a7e782b9adc2091d5fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040759"
---
# <a name="ttm_trackposition-message"></a>TTM \_ trackposition-Nachricht

Legt die Position einer nach Verfolgungs-QuickInfo fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die x-Koordinate des Punkts an, an dem die nach Verfolgungs-QuickInfo in Bildschirm Koordinaten angezeigt wird. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die y-Koordinate des Punkts an, an dem die nach Verfolgungs-QuickInfo in Bildschirm Koordinaten angezeigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Das QuickInfo-Steuerelement wählt basierend auf den Koordinaten, die Sie mit dieser Meldung bereitstellen, das QuickInfo-Fenster aus. Dies bewirkt, dass das QuickInfo-Fenster neben dem Tool angezeigt wird, dem es entspricht. Wenn QuickInfo-Fenster an bestimmten Koordinaten angezeigt werden sollen, schließen Sie beim Hinzufügen des Tools das "ttf absolute"- \_ Flag in den **uFlags** -Member der [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur ein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**TTM \_ trackaktivierungs**](ttm-trackactivate.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Verwenden von Quick Infos](using-tooltip-contro.md)
</dt> </dl>

 

