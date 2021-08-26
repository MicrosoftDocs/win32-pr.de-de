---
title: LVM_GETINSERTMARKRECT (Commctrl.h)
description: Ruft das Rechteck ab, das die Einfügemarke umgibt.
ms.assetid: 7b10229c-73ab-426c-8a8a-71258a33e248
keywords:
- LVM_GETINSERTMARKRECT von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5832ce185a579432b341482847400e96d60869a64d3ff0a2cd599e2eecf6b20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062600"
---
# <a name="lvm_getinsertmarkrect-message"></a>LVM \_ GETINSERTMARKRECT-Nachricht

Ruft das Rechteck ab, das die Einfügemarke umgibt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Nicht verwendet; muss 0 (null) sein.</dd> <dt>

*lParam* 
</dt> <dd>Zeiger auf eine <a href="/previous-versions//dd162897(v=vs.85)">**RECT-Struktur,**</a> die die Koordinaten eines Rechtecks enthält, das die Einfügemarke umgibt.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                      | Beschreibung                          |
|----------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**0**</dt> </dl> | Es wurde keine Einfügemarke gefunden.<br/> |
| <dl> <dt>**1**</dt> </dl> | Einfügemarke gefunden.<br/>    |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest angeben, das Comclt32.dll 6.0 an. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

