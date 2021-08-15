---
title: LVM_MAPINDEXTOID (Commctrl.h)
description: Karten index eines Elements in eine eindeutige ID.
ms.assetid: d0486e21-2703-4289-abb0-f5f9c7b60b40
keywords:
- LVM_MAPINDEXTOID meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LVM_MAPINDEXTOID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 254bfff0ee1598b0657b44a967b9e1331b076a462c8703855c5dd23109a8835d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958149"
---
# <a name="lvm_mapindextoid-message"></a>LVM \_ MAPINDEXTOID-Nachricht

Karten index eines Elements in eine eindeutige ID.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index eines Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine eindeutige ID zurück.

## <a name="remarks"></a>Hinweise

Listenansichtssteuerelemente verfolgen Elemente intern nach Index nach. Dies kann zu Problemen führen, da sich Indizes während der Lebensdauer des Steuerelements ändern können.

Das Listenansicht-Steuerelement kann ein Element mit einer ID markieren, wenn das Element erstellt wird. Sie können diese ID verwenden, um die Eindeutigkeit während der Lebensdauer des Listenansicht-Steuerelements zu gewährleisten.

Um ein Element eindeutig zu identifizieren, nehmen Sie den Index, der von einem Aufruf wie [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) zurückgegeben wird, und rufen **LVM \_ MAPINDEXTOID auf.** Der Rückgabewert ist eine eindeutige ID.

> [!Note]  
> In einer Multithreadumgebung ist der Index nur für den Thread garantiert, der das Listenansicht-Steuerelement hostet, nicht für Hintergrundthreads.

 

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest angeben, das Comclt32.dll 6.0 an. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

