---
title: LVM_SCROLL Nachricht (Commctrl.h)
description: Führt einen Bildlauf durch den Inhalt eines Listenansichtssteuerelements durch. Sie können diese Nachricht explizit oder mithilfe des ListView \_ Scroll-Makros senden.
ms.assetid: 4bf6b74e-8fea-48ca-a151-8fd649fc50f8
keywords:
- LVM_SCROLL Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 604ef35b6d7e62e626aa7cbee32c1563224794781275c470a1b3cd1727b926bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019228"
---
# <a name="lvm_scroll-message"></a>LVM \_ SCROLL-Nachricht

Führt einen Bildlauf durch den Inhalt eines Listenansichtssteuerelements durch. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ Scroll-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Wert vom Typ **int,** der die Menge des horizontalen Bildlaufs in Pixel relativ zur aktuellen Position des Listenansichtsinhalts angibt. Wenn sich das Listenansichtssteuerelement in der Listenansicht befindet, wird dieser Wert auf die nächste Anzahl von Pixeln aufgerundet, die eine ganze Spalte bilden.

</dd> <dt>

*lParam* 
</dt> <dd>

Der Wert vom Typ **int,** der die Menge des vertikalen Bildlaufs in Pixel relativ zur aktuellen Position des Listenansichtsinhalts angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich. Andernfalls **FALSE**.

## <a name="remarks"></a>Hinweise

Wenn sich das Listenansichts-Steuerelement in der Berichtsansicht befindet, kann für das Steuerelement nur ein vertikaler Bildlauf in Ganzzeileninkrementen durchgeführt werden. Daher wird der *lParam-Parameter* auf die nächste Anzahl von Pixeln gerundet, die ein ganzes Zeileninkrement bilden. Wenn die Höhe einer Linie beispielsweise 16 Pixel beträgt und 8 für *lParam* übergeben wird, wird die Liste um 16 Pixel (1 Zeile) gescrollt. Wenn 7 für *lParam* übergeben wird, wird in der Liste ein Bildlauf von 0 Pixeln (0 Zeilen) durchgeführt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





