---
title: LVM_SETINSERTMARKCOLOR Meldung (kommstrg. h)
description: Legt die Farbe der Einfügemarke fest.
ms.assetid: dce2c266-672b-4682-ba23-51d9a8e1102b
keywords:
- Windows-Steuerelemente für LVM_SETINSERTMARKCOLOR Meldung
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260d21d083e2c70d8e82a27628e42596bd1b37eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949419"
---
# <a name="lvm_setinsertmarkcolor-message"></a>LVM- \_ Nachricht

Legt die Farbe der Einfügemarke fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>**COLORREF** -Struktur, die die Farbe zum Festlegen der Einfügemarke angibt.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die auf die vorherige Farbe festgelegte **COLORREF** -Struktur zurück.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





