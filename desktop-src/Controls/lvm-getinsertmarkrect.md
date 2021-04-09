---
title: LVM_GETINSERTMARKRECT Meldung (kommstrg. h)
description: Ruft das Rechteck ab, das die Einfügemarke umschließt.
ms.assetid: 7b10229c-73ab-426c-8a8a-71258a33e248
keywords:
- Windows-Steuerelemente für LVM_GETINSERTMARKRECT Meldung
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
ms.openlocfilehash: dd85bfb94f6425d2666372fd141b531fcb238643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956993"
---
# <a name="lvm_getinsertmarkrect-message"></a>LVM \_ getinsertmarkrect-Nachricht

Ruft das Rechteck ab, das die Einfügemarke umschließt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Nicht verwendet; muss 0 (null) sein.</dd> <dt>

*lParam* 
</dt> <dd>Ein Zeiger auf eine <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> -Struktur, die die Koordinaten eines Rechtecks enthält, das die Einfügemarke umschließt.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                      | Beschreibung                          |
|----------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**0**</dt> </dl> | Keine Einfügemarke gefunden.<br/> |
| <dl> <dt>**1**</dt> </dl> | Einfügemarke gefunden.<br/>    |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

