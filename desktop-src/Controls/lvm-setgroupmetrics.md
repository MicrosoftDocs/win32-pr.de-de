---
title: LVM_SETGROUPMETRICS Meldung (kommstrg. h)
description: Legt Informationen zur Anzeige von Gruppen fest.
ms.assetid: 268b478d-da1f-4efe-9ee9-af3f12e089ee
keywords:
- Windows-Steuerelemente für LVM_SETGROUPMETRICS Meldung
topic_type:
- apiref
api_name:
- LVM_SETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8215962e6f84aac83a2151b46f489938b575303c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340348"
---
# <a name="lvm_setgroupmetrics-message"></a>LVM- \_ setgroupmetrics-Nachricht

Legt Informationen zur Anzeige von Gruppen fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss **null** sein.</dd> <dt>

*lParam* 
</dt> <dd>Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**lvgroupmetrics**</a> -Struktur, die die festzulegenden Metriken enthält.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





