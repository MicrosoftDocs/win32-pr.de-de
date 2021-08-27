---
title: HDM_CREATEDRAGIMAGE (Commctrl.h)
description: Erstellt eine halbtransparente Version des Bilds eines Elements zur Verwendung als Ziehbild. Sie können diese Nachricht explizit senden oder das Makro Header \_ CreateDragImage verwenden.
ms.assetid: 1b9dc515-d327-4634-a424-cc15a32f0f7c
keywords:
- HDM_CREATEDRAGIMAGE meldungssteuerelemente Windows
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
ms.openlocfilehash: 1507f3e72ce75394aaad834fe5c0d876fc579a671ad8f2df00865b2278ad6e32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047230"
---
# <a name="hdm_createdragimage-message"></a>HDM \_ CREATEDRAGIMAGE-Nachricht

Erstellt eine halbtransparente Version des Bilds eines Elements zur Verwendung als Ziehbild. Sie können diese Nachricht explizit senden oder das [**Makro Header \_ CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der nullbasierte Index des Elements innerhalb des Headersteuerelements. Das diesem Element zugewiesene Bild ist die Grundlage für das transparente Bild.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein Handle für eine Bildliste zurück, die das neue Bild als einziges Element enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





