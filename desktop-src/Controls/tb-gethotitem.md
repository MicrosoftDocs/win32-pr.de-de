---
title: TB_GETHOTITEM Meldung (kommstrg. h)
description: Ruft den Index des aktiven Elements auf einer Symbolleiste ab.
ms.assetid: a87dbfc3-c6be-4a0a-9b6a-301b900d7929
keywords:
- Windows-Steuerelemente für TB_GETHOTITEM Meldung
topic_type:
- apiref
api_name:
- TB_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829864cc9223ba15b49b1ecc623f294fd4a6b4fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476302"
---
# <a name="tb_gethotitem-message"></a>TB- \_ gethotitem-Nachricht

Ruft den Index des aktiven Elements auf einer Symbolleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des aktiven Elements oder-1 zurück, wenn kein heißes Element festgelegt ist. Symbolleisten-Steuerelemente, die nicht über den [**\_ flachen tbstyle**](toolbar-control-and-button-styles.md) -Stil verfügen, verfügen nicht über heiße Elemente.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





