---
title: DTM_GETMCFONT Meldung (kommstrg. h)
description: Ruft die Schriftart ab, die das untergeordnete Monatskalender-Steuerelement des Datums-und Zeitauswahl Steuer Elements gegenwärtig verwendet. Sie können diese Nachricht explizit senden oder das "DateTime \_ getmonthcalfont"-Makro verwenden.
ms.assetid: 6687a1dc-6f6d-4684-80b2-f726b08d2f3a
keywords:
- Windows-Steuerelemente für DTM_GETMCFONT Meldung
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
ms.openlocfilehash: d799d5dbbe5e3a4cdf7eede871f9aeac451d17a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859178"
---
# <a name="dtm_getmcfont-message"></a>DTM \_ getmcfont-Nachricht

Ruft die Schriftart ab, die das untergeordnete Monatskalender-Steuerelement des Datums-und Zeitauswahl Steuer Elements gegenwärtig verwendet. Sie können diese Nachricht explizit senden oder das " [**DateTime \_ getmonthcalfont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) "-Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen hFont-Wert zurück, der das Handle der aktuellen Schriftart ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





