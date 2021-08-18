---
title: LM_HITTEST Meldung (Commctrl.h)
description: Bestimmt, ob der Benutzer auf den angegebenen Link geklickt hat.
ms.assetid: a84c0388-26e7-4eda-9c6c-c5f64142d67a
keywords:
- LM_HITTEST Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- LM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 559ea1500c7270ece1785391777133bdaaeb1e95e5b01fa5ca7d4bb76e40f1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958374"
---
# <a name="lm_hittest-message"></a>LM \_ HITTEST-Nachricht

Bestimmt, ob der Benutzer auf den angegebenen Link geklickt hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss **NULL** sein.</dd> <dt>

*lParam* 
</dt> <dd>Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**LINKITTESTINFO-Struktur,**</a> die mit Informationen über den Link gefüllt werden soll, auf den der Benutzer geklickt hat(sofern vorhanden). </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn der Benutzer auf einen Link geklickt hat, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Wenn die **LM \_ HITTEST-Nachricht** erfolgreich ist, füllt das System [**LITEM.iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) und **LITEM.szID** aus. Wenn die **LM \_ HITTEST-Nachricht** fehlschlägt, gehen Sie nicht davon aus, dass informationen in **LITEM** gültig sind.

> [!Note]  
> Um diese API verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





