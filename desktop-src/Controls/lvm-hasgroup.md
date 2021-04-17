---
title: LVM_HASGROUP Meldung (kommstrg. h)
description: Bestimmt, ob das Listenansicht-Steuerelement über eine angegebene Gruppe verfügt.
ms.assetid: 0b8a9208-5221-4f66-8b26-7de55afe485f
keywords:
- Windows-Steuerelemente für LVM_HASGROUP Meldung
topic_type:
- apiref
api_name:
- LVM_HASGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb05fed8466188aa0025d2128ce64ad7f1512c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478501"
---
# <a name="lvm_hasgroup-message"></a>LVM- \_ hasgroup-Nachricht

Bestimmt, ob das Listenansicht-Steuerelement über eine angegebene Gruppe verfügt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Die ID der Gruppe.</dd> <dt>

*lParam* 
</dt> <dd>Muss **null** sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn das Listenansicht-Steuerelement über die angegebene Gruppe verfügt, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





