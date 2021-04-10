---
title: LVM_SETVIEW Meldung (kommstrg. h)
description: Legt die Ansicht eines Listenansicht-Steuer Elements fest.
ms.assetid: e6d3f16d-52ea-4863-a6c9-9a085d5f794a
keywords:
- Windows-Steuerelemente für LVM_SETVIEW Meldung
topic_type:
- apiref
api_name:
- LVM_SETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a159710b3086bcba5298a5a88f9cab15f76e0d89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105464"
---
# <a name="lvm_setview-message"></a>LVM- \_ Setview-Nachricht

Legt die Ansicht eines Listenansicht-Steuer Elements fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>**DWORD** , das die Ansicht angibt.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 1 zurück, wenn erfolgreich, andernfalls-1. Beispielsweise wird-1 zurückgegeben, wenn die Sicht ungültig ist.

## <a name="remarks"></a>Bemerkungen

Im folgenden werden die Werte für Sichten angezeigt.

-   Details der LV- \_ Ansicht \_
-   Symbol für LV- \_ Ansicht \_
-   LV- \_ Ansichts \_ Liste
-   LV- \_ Ansicht \_ SmallIcon
-   LV- \_ Ansichts \_ Kachel

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comctl32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





