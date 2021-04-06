---
title: LVM_INSERTGROUPSORTED Meldung (kommstrg. h)
description: Fügt eine Gruppe in eine geordnete Liste von Gruppen ein.
ms.assetid: 8ad1660b-8b64-4f02-ac1b-b7edeeea38ab
keywords:
- Windows-Steuerelemente für LVM_INSERTGROUPSORTED Meldung
topic_type:
- apiref
api_name:
- LVM_INSERTGROUPSORTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 485941f803fd5af565d8b40524a9e15968e387cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859149"
---
# <a name="lvm_insertgroupsorted-message"></a>LVM \_ insertgroupsortierte Nachricht

Fügt eine Gruppe in eine geordnete Liste von Gruppen ein.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted">lvinsertgroupsortierte</a> -Struktur, die die einzufügende Gruppe enthält.</dd> <dt>

*lParam* 
</dt> <dd>Muss **null** sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Die Reihenfolge der Liste basiert auf der ID der Gruppe. Die Reihenfolge wird durch die Anwendungs definierte Sortierfunktion " [**lvgroupcompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)" definiert, die durch den *wParam* -Parameter in der [**lvinsertgroupsortierten**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted) -Struktur übergeben wird.

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**"Lvgroupcompare"**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> <dt>

[**Lvinsertgroupsortierbar**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted)
</dt> </dl>

 

