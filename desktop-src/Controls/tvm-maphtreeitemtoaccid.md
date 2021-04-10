---
title: TVM_MAPHTREEITEMTOACCID Meldung (kommstrg. h)
description: Ordnet ein HTREEITEM einer Barrierefreiheits-ID zu.
ms.assetid: 87ef0785-88c1-49f4-8a05-872577e16fe4
keywords:
- Windows-Steuerelemente für TVM_MAPHTREEITEMTOACCID Meldung
topic_type:
- apiref
api_name:
- TVM_MAPHTREEITEMTOACCID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6267c2040583917283fc444db74ddacbdabd69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103719"
---
# <a name="tvm_maphtreeitemtoaccid-message"></a>TVM- \_ Meldung "maphtreeitemdeaccid"

Ordnet ein **HTREEITEM** einer Barrierefreiheits-ID zu.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>**HTREEITEM** , das einer Barrierefreiheits-ID zugeordnet ist.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine Barrierefreiheits-ID zurück.

## <a name="remarks"></a>Bemerkungen

Wenn Sie ein Element zu einem Strukturansicht-Steuerelement hinzufügen, wird ein **HTREEITEM** -Handle zurückgegeben, das das Element eindeutig identifiziert.

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

[**TreeView \_ maphtreeitemteaccid**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
</dt> </dl>

 

 





