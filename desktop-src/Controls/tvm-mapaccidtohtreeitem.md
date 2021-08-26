---
title: TVM_MAPACCIDTOHTREEITEM Meldung (Commctrl.h)
description: Karten eine Barrierefreiheits-ID an ein HTREEITEM.
ms.assetid: f4feb7cb-2138-4930-b8ee-b9e2d4b19001
keywords:
- TVM_MAPACCIDTOHTREEITEM Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TVM_MAPACCIDTOHTREEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6481d8db806156d10536ac0ec7c66fdeb4693a1133365767b4c3dc37ad8420f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045800"
---
# <a name="tvm_mapaccidtohtreeitem-message"></a>TVM \_ MAPACCIDTOHTREEITEM-Nachricht

Karten einer **HTREEITEM-Datei** eine Barrierefreiheits-ID.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>**UINT,** der die Barrierefreiheits-ID enthält, die einem **HTREEITEM** zugeordnet werden soll. </dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das **HTREEITEM** zurück, dem die angegebene Barrierefreiheits-ID zugeordnet ist.

## <a name="remarks"></a>Hinweise

Wenn Sie einem Strukturansichtssteuerelement ein Element hinzufügen, gibt **ein HTREEITEM** zurück, das das Element eindeutig identifiziert.

> [!Note]  
> Um diese Meldung verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TreeView \_ MapAccIDToHTREEITEM**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
</dt> </dl>

 

 





