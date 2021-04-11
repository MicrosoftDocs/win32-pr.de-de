---
title: LVM_GETVIEW Meldung (kommstrg. h)
description: Ruft die aktuelle Ansicht eines Listenansicht-Steuer Elements ab.
ms.assetid: dd63e726-3a7f-40e7-8d46-4680816c02a3
keywords:
- Windows-Steuerelemente für LVM_GETVIEW Meldung
topic_type:
- apiref
api_name:
- LVM_GETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2da295fa5a5b335de60169ce06b777d9e355121
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105483"
---
# <a name="lvm_getview-message"></a>LVM \_ GetView-Nachricht

Ruft die aktuelle Ansicht eines Listenansicht-Steuer Elements ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein **DWORD** zurück, das die aktuelle Ansicht angibt.

## <a name="remarks"></a>Bemerkungen

Im folgenden werden die Werte für Sichten angezeigt.

-   Details der LV- \_ Ansicht \_
-   Symbol für LV- \_ Ansicht \_
-   LV- \_ Ansichts \_ Liste
-   LV- \_ Ansicht \_ SmallIcon
-   LV- \_ Ansichts \_ Kachel

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





