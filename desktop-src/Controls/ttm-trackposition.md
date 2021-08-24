---
title: TTM_TRACKPOSITION (Commctrl.h)
description: Legt die Position einer Nachverfolgungs-QuickInfo fest.
ms.assetid: 9eb7c86c-78e6-442a-ad77-5fb919cab591
keywords:
- TTM_TRACKPOSITION meldungssteuerelemente Windows
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
ms.openlocfilehash: 547af5014bbf897d320894c4924911b830997ec3d8532e2ce2c7b63f361a11da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119542825"
---
# <a name="ttm_trackposition-message"></a>TTM \_ TRACKPOSITION-Meldung

Legt die Position einer Nachverfolgungs-QuickInfo fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LOWORD gibt**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) die x-Koordinate des Punkts an, an dem die QuickInfo für die Nachverfolgung in Bildschirmkoordinaten angezeigt wird. Das [**HIWORD gibt**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) die y-Koordinate des Punkts an, an dem die QuickInfo für die Nachverfolgung in Bildschirmkoordinaten angezeigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Meldung wird nicht verwendet.

## <a name="remarks"></a>Hinweise

Das QuickInfo-Steuerelement wählt basierend auf den Koordinaten, die Sie mit dieser Nachricht bereitstellen, aus, wo das QuickInfo-Fenster angezeigt werden soll. Dadurch wird das QuickInfo-Fenster neben dem Tool angezeigt, dem es entspricht. Damit QuickInfo-Fenster an bestimmten Koordinaten angezeigt werden, fügen Sie beim Hinzufügen des Tools das TTF ABSOLUTE-Flag in das \_ **uFlags-Element** der [**TOOLINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) ein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**TTM \_ TRACKACTIVATE**](ttm-trackactivate.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Verwenden von QuickInfo-Steuerelementen](using-tooltip-contro.md)
</dt> </dl>

 

