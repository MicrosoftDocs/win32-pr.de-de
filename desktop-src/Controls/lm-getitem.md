---
title: LM_GETITEM Meldung (kommstrg. h)
description: Ruft die Zustände und Attribute eines Elements ab.
ms.assetid: 75381f28-04d7-4a5c-bc0e-4cc74a06553f
keywords:
- Windows-Steuerelemente für LM_GETITEM Meldung
topic_type:
- apiref
api_name:
- LM_GETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb0e05f896df00f3762c53e6f5f62119cb3645f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102919"
---
# <a name="lm_getitem-message"></a>LM- \_ GetItem-Nachricht

Ruft die Zustände und Attribute eines Elements ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss **null** sein. </dd> <dt>

*lParam* 
</dt> <dd>Ein Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LItem</a> -Struktur, die mit Informationen über das Element aufgefüllt werden soll. </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, wenn die Nachricht erfolgreich die angegebenen Werte und Attribute erhält.

## <a name="remarks"></a>Bemerkungen

Bei der **LM- \_ GetItem** -Nachricht kann nur über den numerischen Index auf Links zugegriffen werden, die im **iLink** -Member von [**LItem**](/windows/win32/api/commctrl/ns-commctrl-litem)zurückgegeben werden. Der Zugriff auf den Link über den in **szid** zurückgegebenen ID-Namen wird nicht unterstützt.

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





