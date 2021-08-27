---
title: LVM_MAPIDTOINDEX Meldung (Commctrl.h)
description: Karten die ID eines Elements in einen Index ein.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_mapidtoindex.htm
keywords:
- LVM_MAPIDTOINDEX Meldung Windows-Steuerelementen
topic_type:
- apiref
api_name:
- LVM_MAPIDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b5380d52f839f28324b808ed0d3304b6c5e2837869e0f0cfc6ab99d8f00b04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079870"
---
# <a name="lvm_mapidtoindex-message"></a>LVM \_ MAPIDTOINDEX-Nachricht

Karten die ID eines Elements in einen Index ein.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die eindeutige ID eines Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den aktuellen Index zurück.

## <a name="remarks"></a>Hinweise

Listenansichtssteuerelemente verfolgen Elemente intern nach Index. Dies kann probleme verursachen, da sich Indizes während der Lebensdauer des Steuerelements ändern können.

Das Listenansichtssteuerelement kann ein Element mit einer ID markieren, wenn das Element erstellt wird. Sie können diese ID verwenden, um die Eindeutigkeit während der Lebensdauer des Listenansicht-Steuerelements zu gewährleisten.

Um ein Element eindeutig zu identifizieren, verwenden Sie den Index, der von einem Aufruf wie [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) zurückgegeben wird, und rufen Sie [**LVM \_ MAPINDEXTOID**](lvm-mapindextoid.md)auf. Der Rückgabewert ist eine eindeutige ID.

Wenn Sie den Index eines Elements benötigen, nachdem eine ID erstellt wurde, können Sie **LVM \_ MAPIDTOINDEX** mit der eindeutigen ID aufrufen und den aktuellen Index zurückgegeben.

**LVM \_ MAPIDTOINDEX** wird im [**LVS \_ OWNERDATA-Stil**](list-view-window-styles.md) nicht unterstützt.

> [!Note]  
> In einer Multithreadumgebung wird der Index nur für den Thread garantiert, der das Listenansichtssteuerelement hostet, nicht für Hintergrundthreads.

 

> [!Note]  
> Um diese Meldung verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

