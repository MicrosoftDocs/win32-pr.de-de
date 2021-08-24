---
title: LVM_SETITEMCOUNT Meldung (Commctrl.h)
description: Bewirkt, dass das Listenansichtssteuerelement Speicher für die angegebene Anzahl von Elementen zuweist oder die virtuelle Anzahl von Elementen in einem virtuellen Listenansichtssteuerelement festlegt.
ms.assetid: 5e794c12-ddcb-44fc-b0d2-677352602503
keywords:
- LVM_SETITEMCOUNT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_SETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be6b35b38c65663d9811a27341cf10d668a9e045641a8ff0871f6b49fe8bcdbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656280"
---
# <a name="lvm_setitemcount-message"></a>LVM \_ SETITEMCOUNT-Nachricht

Bewirkt, dass das Listenansichtssteuerelement Speicher für die angegebene Anzahl von Elementen zuweist, oder legt die virtuelle Anzahl von Elementen in einem [virtuellen Listenansichtssteuerelement fest.](list-view-controls-overview.md)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Anzahl der Elemente, die das Listenansichtssteuerelement letztendlich enthält.

</dd> <dt>

*lParam* 
</dt> <dd>

[Version 4.70.](common-control-versions.md) Werte, die das Verhalten des Listenansichtssteuerelements nach dem Zurücksetzen der Elementanzahl angeben. Dieser Wert kann eine Kombination der folgenden Sein:



| Wert                                                                                                                                                                                    | Bedeutung                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="LVSICF_NOINVALIDATEALL"></span><span id="lvsicf_noinvalidateall"></span><dl> <dt>**LVSICF \_ NOINVALIDATEALL**</dt> </dl> | Das Listenansichtssteuerelement wird nur dann neu maliert, wenn die betroffenen Elemente derzeit angezeigt werden.<br/>    |
| <span id="LVSICF_NOSCROLL"></span><span id="lvsicf_noscroll"></span><dl> <dt>**LVSICF \_ NOSCROLL**</dt> </dl>                      | Das Listenansichtssteuerelement ändert die Bildlaufposition nicht, wenn sich die Elementanzahl ändert.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück. Andernfalls wird 0 (null) zurückgegeben.

## <a name="remarks"></a>Hinweise

Wie der Arbeitsspeicher zugeordnet wird, hängt davon ab, wie das Listenansicht-Steuerelement erstellt wurde. Sie können diese Nachricht explizit senden oder die [**Makros ListView \_ SetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcount) oder [**ListView \_ SetItemCountEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemcountex) verwenden. Weitere Informationen finden Sie unter [Virtual List-View Style](/windows/desktop/Controls/list-view-controls-overview).

Wenn das Listenansichtssteuerelement ohne den [**LVS \_ OWNERDATA-Stil**](list-view-window-styles.md) erstellt wurde, bewirkt das Senden dieser Nachricht, dass das Steuerelement seine internen Datenstrukturen für die angegebene Anzahl von Elementen zuordnet. Dadurch wird verhindert, dass das Steuerelement die Datenstrukturen jedes Mal zuordnen muss, wenn ein Element hinzugefügt wird.

Wenn das Listenansichtssteuerelement mit dem [**LVS \_ OWNERDATA-Stil**](list-view-window-styles.md) (einer virtuellen Listenansicht) erstellt wurde, legt das Senden dieser Meldung die virtuelle Anzahl von Elementen fest, die das Steuerelement enthält.

Der *lParam-Parameter* ist nur für Listenansichtssteuerelemente vorgesehen, die die Formate [**LVS \_ OWNERDATA**](list-view-window-styles.md) und [**LVS \_ REPORT**](list-view-window-styles.md) oder [**LVS \_ LIST**](list-view-window-styles.md) verwenden.

Wenn die Listenansicht des allgemeinen Steuerelements eine virtualisierte Listenansicht [**(LVS \_ OWNERDATA)**](list-view-window-styles.md)ist, gilt für die Listenansicht ein Grenzwert von 100.000.000 Einträgen. In diesem Szenario gibt **LVM \_ SETITEMCOUNT** FALSE zurück, wenn es über eine *wParam* von 100.000.001 verfügt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

