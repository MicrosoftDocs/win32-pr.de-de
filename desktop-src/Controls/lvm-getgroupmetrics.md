---
title: LVM_GETGROUPMETRICS Meldung (Commctrl.h)
description: Ruft Informationen zur Anzeige von Gruppen ab.
ms.assetid: 75e7da66-50c6-4834-ae66-e43b8f9b0b34
keywords:
- LVM_GETGROUPMETRICS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_GETGROUPMETRICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b99996adfe7f26342dde8967c95973fdb972290367328875257f5615f0a43c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062610"
---
# <a name="lvm_getgroupmetrics-message"></a>LVM \_ GETGROUPMETRICS-Nachricht

Ruft Informationen zur Anzeige von Gruppen ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss **NULL** sein.</dd> <dt>

*lParam* 
</dt> <dd>Ein Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroupmetrics">**LVGROUPMETRICS-Struktur,**</a> die die abgerufenen Metriken empfängt.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um diese Meldung verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





