---
title: DTM_GETMCFONT-Nachricht (Commctrl.h)
description: Ruft die Schriftart ab, die das Kalendersteuerelement für untergeordnete Monate des DTP-Steuerelements (Date and Time Picker) derzeit verwendet. Sie können diese Nachricht explizit senden oder das DateTime \_ GetMonthCalFont-Makro verwenden.
ms.assetid: 6687a1dc-6f6d-4684-80b2-f726b08d2f3a
keywords:
- DTM_GETMCFONT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- DTM_GETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2bf60f226e7fe5d309324bc517a7fd215abe4591fd5141ff149b14e162ac9be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878130"
---
# <a name="dtm_getmcfont-message"></a>FEHLERMELDUNG \_ GETMCFONT

Ruft die Schriftart ab, die das Kalendersteuerelement für untergeordnete Monate des DTP-Steuerelements (Date and Time Picker) derzeit verwendet. Sie können diese Nachricht explizit senden oder das [**DateTime \_ GetMonthCalFont-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen HFONT-Wert zurück, der das Handle für die aktuelle Schriftart ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





