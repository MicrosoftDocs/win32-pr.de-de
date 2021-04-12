---
title: LVM_SORTGROUPS Meldung (kommstrg. h)
description: Verwendet eine Anwendungs definierte Vergleichsfunktion, um Gruppen nach ID in einem Listenansicht-Steuerelement zu sortieren.
ms.assetid: 553e96d6-a982-4482-8fba-ef11a74fb82e
keywords:
- Windows-Steuerelemente für LVM_SORTGROUPS Meldung
topic_type:
- apiref
api_name:
- LVM_SORTGROUPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c70fd0f343c9efe0215c87f430e5ed1c89a3aed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105459"
---
# <a name="lvm_sortgroups-message"></a>LVM \_ sortgroups-Meldung

Verwendet eine Anwendungs definierte Vergleichsfunktion, um Gruppen nach ID in einem Listenansicht-Steuerelement zu sortieren.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Zeiger auf eine Anwendungs definierte Vergleichsfunktion, " <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">lvgroupcompare</a>".</dd> <dt>

*lParam* 
</dt> <dd>Void-Zeiger auf die Anwendungs definierten Informationen.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 1 zurück, wenn erfolgreich, andernfalls 0.

## <a name="remarks"></a>Bemerkungen

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

[**"Lvgroupcompare"**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> </dl>

