---
title: TB_SETHOTITEM2-Nachricht (Commctrl.h)
description: 'TB_SETHOTITEM2 Meldung: Legt das heiße Element in einer Symbolleiste fest.'
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- TB_SETHOTITEM2 Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 8f4bb1e560e2be2b6952406d548215d60f2c2974e57b2388580da7453b51c184
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318820"
---
# <a name="tb_sethotitem2-message"></a>TB \_ SETHOTITEM2-Nachricht

Legt das heiße Element in einer Symbolleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index des Elements, das heiß gemacht wird. Wenn dieser Wert -1 ist, ist keines der Elemente heiß.

</dd> <dt>

*lParam* 
</dt> <dd>Eine Kombination von HICF \_ xxx-Flags. Siehe <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des vorherigen heißen Elements oder -1 zurück, wenn kein heißes Element vorhanden war.

## <a name="remarks"></a>Hinweise

Das Verhalten dieser Meldung ist nicht für Symbolleisten definiert, die nicht über den [**TBSTYLE \_ FLAT-Stil**](toolbar-control-and-button-styles.md) verfügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





