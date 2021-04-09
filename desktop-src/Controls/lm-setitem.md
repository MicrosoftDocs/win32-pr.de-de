---
title: LM_SETITEM Meldung (kommstrg. h)
description: Legt die Zustände und Attribute eines Elements fest.
ms.assetid: 02a68a31-2541-480e-b768-449d40e5e9e0
keywords:
- Windows-Steuerelemente für LM_SETITEM Meldung
topic_type:
- apiref
api_name:
- LM_SETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11888a76b11ccec7e8e659ca3a33bb23a71667ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102915"
---
# <a name="lm_setitem-message"></a>LM- \_ Nachricht

Legt die Zustände und Attribute eines Elements fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss **null** sein. </dd> <dt>

*lParam* 
</dt> <dd>Ein Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LItem</a> -Struktur, die die für den Link gewünschten neuen Zustände und Attribute enthält. </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die Nachricht beim Festlegen der angegebenen Werte und Attribute erfolgreich ist.

## <a name="remarks"></a>Bemerkungen

Bei der [**LM- \_ GetItem**](lm-getitem.md) -Nachricht kann nur über den numerischen Index auf Links zugegriffen werden, die im **iLink** -Member von [**LItem**](/windows/win32/api/commctrl/ns-commctrl-litem)zurückgegeben werden. Der Zugriff auf den Link über den in **szid** zurückgegebenen ID-Namen wird nicht unterstützt.

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comctl32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





