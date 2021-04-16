---
title: LVM_MAPINDEXTOID Meldung (kommstrg. h)
description: Ordnet den Index eines Elements einer eindeutigen ID zu.
ms.assetid: d0486e21-2703-4289-abb0-f5f9c7b60b40
keywords:
- Windows-Steuerelemente für LVM_MAPINDEXTOID Meldung
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
ms.openlocfilehash: f6a2a5de558b025e61bef26fd20278f125372769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476089"
---
# <a name="lvm_mapindextoid-message"></a>LVM \_ mapindextoid-Meldung

Ordnet den Index eines Elements einer eindeutigen ID zu.

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

## <a name="remarks"></a>Bemerkungen

Listenansicht-Steuerelemente nachverfolgen Elemente intern nach Index. Dies kann Probleme darstellen, da Indizes sich während der Lebensdauer des Steuer Elements ändern können.

Das Listenansicht-Steuerelement kann ein Element mit einer ID markieren, wenn das Element erstellt wird. Sie können diese ID verwenden, um die Eindeutigkeit während der Lebensdauer des Listenansicht-Steuer Elements sicherzustellen.

Wenn Sie ein Element eindeutig identifizieren möchten, nehmen Sie den Index an, der von einem-Befehl wie [**IComponent:: GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) zurückgegeben wird, und nennen Sie **LVM \_ mapindextoid**. Der Rückgabewert ist eine eindeutige ID.

> [!Note]  
> In einer Multithreadumgebung wird der Index nur für den Thread garantiert, der das Listenansicht-Steuerelement hostet, nicht für Hintergrundthreads.

 

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

