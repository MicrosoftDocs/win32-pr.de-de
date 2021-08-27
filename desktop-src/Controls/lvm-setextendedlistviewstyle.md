---
title: LVM_SETEXTENDEDLISTVIEWSTYLE (Commctrl.h)
description: Legt erweiterte Stile in Listenansichtssteuerelementen fest. Sie können diese Nachricht explizit senden oder das Makro ListView \_ SetExtendedListViewStyle oder ListView \_ SetExtendedListViewStyleEx verwenden.
ms.assetid: eb3f47ed-484a-49a8-94b0-e50ee081bd69
keywords:
- LVM_SETEXTENDEDLISTVIEWSTYLE von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- LVM_SETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 336732b927c7ee6170e777f2f7c1cd57eac6baa2c7706870e681f602e2309c37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077280"
---
# <a name="lvm_setextendedlistviewstyle-message"></a>LVM \_ SETEXTENDEDLISTVIEWSTYLE-Meldung

Legt erweiterte Stile in Listenansichtssteuerelementen fest. Sie können diese Nachricht explizit senden oder das [**Makro ListView \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) oder [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

**DWORD-Wert,** der angibt, welche Stile in *lParam* betroffen sein sollen. Dieser Parameter kann eine Kombination aus erweiterten List-View [**Sein.**](extended-list-view-styles.md) Nur die erweiterten Stile in *wParam* werden geändert. Alle anderen Stile werden so beibehalten, wie sie sind. Wenn dieser Parameter 0 (null) ist, sind alle Stile in *lParam* betroffen.

</dd> <dt>

*lParam* 
</dt> <dd>

**DWORD-Wert,** der die erweiterten Listenansicht-Steuerelementstile angibt, die festgelegt werden. Dieser Parameter kann eine Kombination aus erweiterten List-View [**Sein.**](extended-list-view-styles.md) Stile, die nicht festgelegt, aber in *wParam angegeben* sind, werden entfernt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD-Wert** zurück, der die vorherigen erweiterten Listenansicht-Steuerelementstile enthält.

## <a name="remarks"></a>Hinweise

Mit *dem wParam-Parameter* können Sie einen oder mehrere erweiterte Stile ändern, ohne die vorhandenen Stile zuerst abrufen zu müssen. Wenn Sie beispielsweise [**LVS \_ EX \_ FULLROWSELECT**](extended-list-view-styles.md) für *wParam* und 0 für *lParam* übergeben, wird der **LVS EX \_ \_ FULLROWSELECT-Stil** deaktiviert, aber alle anderen Stile bleiben unverändert.

Aus Gründen der Abwärtskompatibilität wurde das [**\_ ListView-Makro SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) nicht aktualisiert, um *wParam zu verwenden.* Um den *wParam-Wert zu* verwenden, verwenden Sie das [**ListView \_ SetExtendedListViewStyleEx-Makro.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex)

Wenn Sie diese Meldung zum Festlegen des [**LVS \_ EX \_ CHECKBOXES-Stils**](extended-list-view-styles.md) verwenden, werden alle zuvor festgelegten Statusbildindexe verworfen. Alle Kontrollkästchen werden in den nicht aktivierten Zustand initialisiert. Der Statusbildindex ist in bits 12 bis  15 des Zustandsmitglieds der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) enthalten.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





