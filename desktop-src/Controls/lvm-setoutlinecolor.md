---
title: LVM_SETOUTLINECOLOR-Nachricht (Commctrl.h)
description: Legt die Farbe des Rahmens eines Listenansichtssteuerelements fest, wenn der erweiterte Fensterstil LVS \_ EX \_ BORDERSELECT festgelegt ist.
ms.assetid: c2b606fa-8d47-4192-94b7-d01c3cfdc514
keywords:
- LVM_SETOUTLINECOLOR Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_SETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db9f5d53339ecec19fd6f06fcabd3a0471b1c3a569e8856571a98a99675a232
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119217390"
---
# <a name="lvm_setoutlinecolor-message"></a>LVM \_ SETOUTLINECOLOR-Meldung

Legt die Farbe des Rahmens eines Listenansichtssteuerelements fest, wenn der erweiterte [**Fensterstil LVS \_ EX \_ BORDERSELECT**](extended-list-view-styles.md) festgelegt ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>**COLORREF-Struktur,** die die Farbe zum Festlegen des Rahmens angibt.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die **COLORREF-Struktur** zurück, die die Konturfarbe enthält.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um diese Meldung verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





