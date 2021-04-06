---
title: TB_SETHOTITEM Meldung (kommstrg. h)
description: Legt das heiße Element in einer Symbolleiste fest.
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- Windows-Steuerelemente für TB_SETHOTITEM Meldung
topic_type:
- apiref
api_name:
- TB_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c477a445cb6aae78dd5d31e8d23b8ec3be8c61ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859098"
---
# <a name="tb_sethotitem-message"></a>TB-Nachricht "nach \_ richten"

Legt das heiße Element in einer Symbolleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Elements, das heiß gemacht wird. Wenn dieser Wert-1 ist, ist keines der Elemente heiß.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

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



 

 





