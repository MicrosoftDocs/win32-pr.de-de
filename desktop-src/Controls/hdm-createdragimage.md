---
title: HDM_CREATEDRAGIMAGE Meldung (kommstrg. h)
description: Erstellt eine halbtransparente Version eines Element Bilds, das als Zieh Bild verwendet werden soll. Sie können diese Nachricht explizit senden oder das-Header-präffemage- \_ Makro verwenden.
ms.assetid: 1b9dc515-d327-4634-a424-cc15a32f0f7c
keywords:
- Windows-Steuerelemente für HDM_CREATEDRAGIMAGE Meldung
topic_type:
- apiref
api_name:
- HDM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9e801ad9771205b5f2e6df8e37bb0a0ad7f0bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040766"
---
# <a name="hdm_createdragimage-message"></a>HDM- \_ Meldung "kreatedragimage"

Erstellt eine halbtransparente Version eines Element Bilds, das als Zieh Bild verwendet werden soll. Sie können diese Nachricht explizit senden oder das- [**Header \_**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) -präffemage-Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index des Elements innerhalb des Header Steuer Elements. Das diesem Element zugewiesene Bild ist die Grundlage für das transparente Bild.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein Handle für eine Bildliste zurück, die das neue Bild als einziges Element enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





