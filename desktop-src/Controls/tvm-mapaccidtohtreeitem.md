---
title: TVM_MAPACCIDTOHTREEITEM Meldung (kommstrg. h)
description: Ordnet einem HTREEITEM eine Barrierefreiheits-ID zu.
ms.assetid: f4feb7cb-2138-4930-b8ee-b9e2d4b19001
keywords:
- Windows-Steuerelemente für TVM_MAPACCIDTOHTREEITEM Meldung
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
ms.openlocfilehash: b827b18387723fe4792321f7932e1abb3673466e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040346"
---
# <a name="tvm_mapaccidtohtreeitem-message"></a>TVM \_ mapacciddehtreeitem-Meldung

Ordnet einem **HTREEITEM** eine Barrierefreiheits-ID zu.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>**Uint** , das die Barrierefreiheits-ID enthält, die einem **HTREEITEM** zugeordnet werden soll. </dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das **HTREEITEM** -Element zurück, dem die angegebene Barrierefreiheits-ID zugeordnet ist.

## <a name="remarks"></a>Bemerkungen

Wenn Sie ein Element zu einem Strukturansicht-Steuerelement hinzufügen, gibt ein **HTREEITEM** -Objekt zurück, das das Element eindeutig identifiziert.

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

[**TreeView \_ mapaccidto HTREEITEM**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
</dt> </dl>

 

 





