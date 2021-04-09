---
title: MCM_GETMAXSELCOUNT Meldung (kommstrg. h)
description: Ruft den maximalen Datumsbereich ab, der in einem Monatskalender-Steuerelement ausgewählt werden kann. Sie können diese Nachricht explizit oder mit dem monthcal \_ getmaxselcount-Makro senden.
ms.assetid: 34204231-3a3c-4eba-913d-b0c27769c338
keywords:
- Windows-Steuerelemente für MCM_GETMAXSELCOUNT Meldung
topic_type:
- apiref
api_name:
- MCM_GETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bddfdad17cc4a0fd6499514023cb499f55f40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040762"
---
# <a name="mcm_getmaxselcount-message"></a>MCM \_ getmaxselcount-Nachricht

Ruft den maximalen Datumsbereich ab, der in einem Monatskalender-Steuerelement ausgewählt werden kann. Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getmaxselcount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen int-Wert zurück, der die Gesamtzahl der Tage darstellt, die für das-Steuerelement ausgewählt werden können.

## <a name="remarks"></a>Bemerkungen

Sie können den maximalen Datumsbereich ändern, der ausgewählt werden kann, indem Sie die [**MCM \_ setmaxselcount**](mcm-setmaxselcount.md) -Nachricht verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





