---
title: TB_SETHOTITEM2 Meldung (kommstrg. h)
description: Legt das heiße Element in einer Symbolleiste fest.
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- Windows-Steuerelemente für TB_SETHOTITEM2 Meldung
topic_type:
- apiref
api_name:
- TB_SETHOTITEM2
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7027920e4363b46fcc0b6d9b0d87129e01843318
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742649"
---
# <a name="tb_sethotitem2-message"></a>TB \_ SETHOTITEM2 Meldung

Legt das heiße Element in einer Symbolleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Elements, das heiß gemacht wird. Wenn dieser Wert-1 ist, ist keines der Elemente heiß.

</dd> <dt>

*lParam* 
</dt> <dd>Eine Kombination von hicf \_ xxx-Flags. Weitere Informationen finden Sie unter <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**nmtbhutitem**</a>.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des vorherigen aktiven Elements oder-1 zurück, wenn kein heißes Element vorhanden war.

## <a name="remarks"></a>Bemerkungen

Das Verhalten dieser Nachricht ist nicht für Symbolleisten definiert, die nicht den [**\_ flachen tbstyle**](toolbar-control-and-button-styles.md) -Stil aufweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





