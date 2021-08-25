---
title: DTM_GETIDEALSIZE (Commctrl.h)
description: Ruft die Größe ab, die zum Anzeigen des Steuerelements ohne Clipping erforderlich ist. Senden Sie diese Nachricht explizit oder mithilfe des DateTime \_ GetIdealSize-Makros.
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- DTM_GETIDEALSIZE message Windows Controls
topic_type:
- apiref
api_name:
- DTM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 639fbbb25fbf61695f83b54f106f45ff3dd421f528807120be52edd7031e4f66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878230"
---
# <a name="dtm_getidealsize-message"></a>SMS \_ GETIDEALSIZE-Nachricht

Ruft die Größe ab, die zum Anzeigen des Steuerelements ohne Clipping erforderlich ist. Senden Sie diese Nachricht explizit oder mithilfe des [**DateTime \_ GetIdealSize-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wird nicht verwendet. Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**SIZE-Struktur,**](/previous-versions//dd145106(v=vs.85)) um die ideale Größe zu erhalten. Die aufrufende Anwendung ist für die Zuordnung dieser Struktur verantwortlich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

