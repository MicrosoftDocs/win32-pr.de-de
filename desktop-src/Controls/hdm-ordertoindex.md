---
title: HDM_ORDERTOINDEX Meldung (kommstrg. h)
description: Ruft einen Indexwert für ein Element auf Grundlage seiner Reihenfolge im Header Steuerelement ab. Sie können diese Nachricht explizit senden oder den Header \_ orderdeindex-Makro verwenden.
ms.assetid: vs|controls|~\controls\header\messages\hdm_ordertoindex.htm
keywords:
- Windows-Steuerelemente für HDM_ORDERTOINDEX Meldung
topic_type:
- apiref
api_name:
- HDM_ORDERTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b65d10fb27c9a07639ebbd5770a53d72cbf0aba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040544"
---
# <a name="hdm_ordertoindex-message"></a>HDM \_ Order$ Index-Meldung

Ruft einen Indexwert für ein Element auf Grundlage seiner Reihenfolge im Header Steuerelement ab. Sie können diese Nachricht explizit senden oder den [**Header \_ orderdeindex**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Reihenfolge, in der das Element im Header Steuerelement angezeigt wird, von links nach rechts. Der Indexwert des Elements in der Spalte ganz links wäre z. b. 0. Der Wert für das nächste Element rechts ist 1 usw.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt int zurück, das den Element Index angibt. Wenn *wParam* ungültig ist (negativ oder zu groß), ist die Rückgabe gleich *wParam*.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





