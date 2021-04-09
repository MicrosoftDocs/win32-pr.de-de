---
title: LM_HITTEST Meldung (kommstrg. h)
description: Bestimmt, ob der Benutzer auf den angegebenen Link geklickt hat.
ms.assetid: a84c0388-26e7-4eda-9c6c-c5f64142d67a
keywords:
- Windows-Steuerelemente für LM_HITTEST Meldung
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
ms.openlocfilehash: c497800369203ac8ea7484371e1038ba15d6cc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858658"
---
# <a name="lm_hittest-message"></a>LM- \_ HitTest-Meldung

Bestimmt, ob der Benutzer auf den angegebenen Link geklickt hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss **null** sein.</dd> <dt>

*lParam* 
</dt> <dd>Ein Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**lhittestinfo**</a> -Struktur, die mit Informationen über den Link gefüllt werden soll, auf den der Benutzer geklickt hat, sofern vorhanden. </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn der Benutzer auf einen Link geklickt hat; andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn die **LM- \_ HitTest** -Nachricht erfolgreich ist, füllt das System [**LItem. iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) und **LItem. szid** aus. Wenn die **LM- \_ HitTest** -Nachricht fehlschlägt, gehen Sie nicht davon aus, dass alle Informationen in **LItem** gültig sind.

> [!Note]  
> Um diese API zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





