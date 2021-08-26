---
title: TCM_REMOVEIMAGE Meldung (Commctrl.h)
description: Entfernt ein Bild aus der Bildliste eines Registerkartensteuerelements. Sie können diese Nachricht explizit oder mithilfe des \_ TabCtrl RemoveImage-Makros senden.
ms.assetid: f2761338-0afa-47d8-9d9c-1d5a4a7f7bcf
keywords:
- TCM_REMOVEIMAGE Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 40d2305386f948e1dc4522124708b31ca360203ba9723241c99262fcdb5d2b20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104840"
---
# <a name="tcm_removeimage-message"></a>TCM \_ REMOVEIMAGE-Nachricht

Entfernt ein Bild aus der Bildliste eines Registerkartensteuerelements. Sie können diese Nachricht explizit oder mithilfe des [**TabCtrl \_ RemoveImage-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index des zu entfernende Bilds.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Das Registerkartensteuerelement aktualisiert den Imageindex jeder Registerkarte, sodass jede Registerkarte demselben Bild wie zuvor zugeordnet bleibt. Wenn eine Registerkarte das entfernte Bild verwendet, wird die Registerkarte auf kein Bild festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





