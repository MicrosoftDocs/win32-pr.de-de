---
title: LVM_MAPIDTOINDEX Meldung (kommstrg. h)
description: Ordnet die ID eines Elements einem Index zu.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_mapidtoindex.htm
keywords:
- Windows-Steuerelemente für LVM_MAPIDTOINDEX Meldung
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
ms.openlocfilehash: fb4cb8aa49b37186ef689ed8cb319bbb92b62d75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343461"
---
# <a name="lvm_mapidtoindex-message"></a>LVM- \_ mapiddeindex-Meldung

Ordnet die ID eines Elements einem Index zu.

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

## <a name="remarks"></a>Bemerkungen

Listenansicht-Steuerelemente nachverfolgen Elemente intern nach Index. Dies kann Probleme darstellen, da Indizes sich während der Lebensdauer des Steuer Elements ändern können.

Das Listenansicht-Steuerelement kann ein Element mit einer ID markieren, wenn das Element erstellt wird. Sie können diese ID verwenden, um die Eindeutigkeit während der Lebensdauer des Listenansicht-Steuer Elements sicherzustellen.

Wenn Sie ein Element eindeutig identifizieren möchten, nehmen Sie den Index an, der von einem-Befehl wie [**IComponent:: GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) zurückgegeben wird, und nennen Sie [**LVM \_ mapindextoid**](lvm-mapindextoid.md). Der Rückgabewert ist eine eindeutige ID.

Wenn Sie den Index eines Elements benötigen, nachdem eine ID erstellt wurde, können Sie **LVM \_ mapidtoindex** mit der eindeutigen ID aufrufen und den aktuellen Index zurückgegeben.

**LVM \_ Mapidumindex** wird unter dem [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Stil nicht unterstützt.

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



 

