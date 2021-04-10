---
title: LVM_GETTILEINFO Meldung (kommstrg. h)
description: Ruft Informationen zu einer Kachel in einem Listenansicht-Steuerelement ab.
ms.assetid: e89a3eae-0970-488c-ba95-1072aa85bbf4
keywords:
- Windows-Steuerelemente für LVM_GETTILEINFO Meldung
topic_type:
- apiref
api_name:
- LVM_GETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db5bfd085cd5cbaced0bf90b17e8862a6c0e159b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040887"
---
# <a name="lvm_gettileinfo-message"></a>LVM \_ gettileinfo-Nachricht

Ruft Informationen zu einer Kachel in einem Listenansicht-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Ein Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**lvtileinfo**</a> -Struktur, die die abgerufenen Informationen empfängt.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Die Kachel Ansicht ist eine neue Methode zum Anordnen und Anzeigen von Elementen in einem Listenansicht-Steuerelement. Die anderen Ansichten sind Icon, Small Icon, Details und List.

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





