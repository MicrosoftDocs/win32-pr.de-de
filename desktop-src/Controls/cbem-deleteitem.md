---
title: CBEM_DELETEITEM Meldung (kommstrg. h)
description: Entfernt ein Element aus einem ComboBoxEx-Steuerelement.
ms.assetid: 688cf388-54ba-4b45-88d7-628da49d8615
keywords:
- Windows-Steuerelemente für CBEM_DELETEITEM Meldung
topic_type:
- apiref
api_name:
- CBEM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa3034f79dffabcd7d7aa780582646e17d30b62f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342670"
---
# <a name="cbem_deleteitem-message"></a>CBEM \_ DeleteItem-Meldung

Entfernt ein Element aus einem ComboBoxEx-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index des zu entfernenden Elements.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen int-Wert zurück, der die Anzahl der im-Steuerelement verbleibenden Elemente darstellt. Wenn *iIndex* ungültig ist, gibt die Nachricht CB \_ Err zurück.

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird der Kombinations Feld-Steuerelement Nachricht [**CB \_ deletestring**](cb-deletestring.md)zugeordnet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





