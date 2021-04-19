---
title: TCM_REMOVEIMAGE Meldung (kommstrg. h)
description: Entfernt ein Bild aus der Bildliste eines Registerkarten-Steuer Elements. Sie können diese Nachricht explizit oder mithilfe des tabctrl \_ removeimage-Makros senden.
ms.assetid: f2761338-0afa-47d8-9d9c-1d5a4a7f7bcf
keywords:
- Windows-Steuerelemente für TCM_REMOVEIMAGE Meldung
topic_type:
- apiref
api_name:
- TCM_REMOVEIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbc51aa0efed847e39e735443c0d42e288bbaab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346335"
---
# <a name="tcm_removeimage-message"></a>TCM \_ removeimage-Nachricht

Entfernt ein Bild aus der Bildliste eines Registerkarten-Steuer Elements. Sie können diese Nachricht explizit oder mithilfe des [**tabctrl \_ removeimage**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des zu entfernenden Bilds.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Das Registerkarten-Steuerelement aktualisiert den Bildindex jeder Registerkarte, sodass jede Registerkarte dem gleichen Bild wie zuvor zugeordnet bleibt. Wenn eine Registerkarte das zu entfernende Bild verwendet, wird die Registerkarte so festgelegt, dass Sie kein Bild hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





