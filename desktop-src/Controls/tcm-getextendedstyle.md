---
title: TCM_GETEXTENDEDSTYLE Meldung (kommstrg. h)
description: Ruft die erweiterten Stile ab, die zurzeit für das Registerkarten-Steuerelement verwendet werden. Sie können diese Nachricht explizit oder mithilfe des tabstrg \_ GetExtendedStyle-Makros senden.
ms.assetid: 983ffcbe-0d8d-4686-83de-fc564744390f
keywords:
- Windows-Steuerelemente für TCM_GETEXTENDEDSTYLE Meldung
topic_type:
- apiref
api_name:
- TCM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8280b7043591dd4fdd0b453c5baea5fe014bd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957039"
---
# <a name="tcm_getextendedstyle-message"></a>TCM \_ GetExtendedStyle-Nachricht

Ruft die erweiterten Stile ab, die zurzeit für das Registerkarten-Steuerelement verwendet werden. Sie können diese Nachricht explizit oder mithilfe des [**tabstrg \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getextendedstyle) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD** -Wert zurück, der die erweiterten Stile darstellt, die zurzeit für das Register Steuerelement verwendet werden. Dieser Wert ist eine Kombination aus [erweiterten](tab-control-extended-styles.md)Formatvorlagen des Register Steuer Elements.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TCM/ \_ textendecodstyle**](tcm-setextendedstyle.md)
</dt> </dl>

 

 





