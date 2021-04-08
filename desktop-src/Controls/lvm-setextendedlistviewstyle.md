---
title: LVM_SETEXTENDEDLISTVIEWSTYLE Meldung (kommstrg. h)
description: Legt erweiterte Stile in Listenansicht-Steuerelementen fest. Sie können diese Nachricht explizit senden oder das "ListView"-und "ListView/ \_ \_ textendedlistviewstyleex"-Makro verwenden.
ms.assetid: eb3f47ed-484a-49a8-94b0-e50ee081bd69
keywords:
- Windows-Steuerelemente für LVM_SETEXTENDEDLISTVIEWSTYLE Meldung
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
ms.openlocfilehash: f7d36869283d863bef7b31187a002125c9cd79bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949423"
---
# <a name="lvm_setextendedlistviewstyle-message"></a>LVM- \_ Meldung "abtextendedlistviewstyle"

Legt erweiterte Stile in Listenansicht-Steuerelementen fest. Sie können diese Nachricht explizit senden oder das " [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) "-und "ListView/ [**\_ textendedlistviewstyleex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) "-Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

**DWORD** -Wert, der angibt, welche Stile in *LPARAM* betroffen sein sollen. Dieser Parameter kann eine Kombination aus [**erweiterten List-View Stilen**](extended-list-view-styles.md)sein. Nur die erweiterten Stile in *wParam* werden geändert. Alle anderen Stile werden unverändert beibehalten. Wenn dieser Parameter 0 (null) ist, werden alle Stile in *LPARAM* beeinträchtigt.

</dd> <dt>

*lParam* 
</dt> <dd>

**DWORD** -Wert, der die festzulegenden erweiterten Listenansicht-Steuerelement Stile angibt. Dieser Parameter kann eine Kombination aus [**erweiterten List-View Stilen**](extended-list-view-styles.md)sein. Stile, die nicht festgelegt sind, aber in *wParam* angegeben sind, werden entfernt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD** -Wert zurück, der die vorherigen erweiterten Listenansicht-Steuerelement Stile enthält.

## <a name="remarks"></a>Bemerkungen

Mit dem *wParam* -Parameter können Sie einen oder mehrere erweiterte Stile ändern, ohne zuerst die vorhandenen Stile abrufen zu müssen. Wenn Sie z. b. [**LVS \_ Ex \_ FullRowSelect**](extended-list-view-styles.md) für *wParam* und 0 für *LPARAM* übergeben, werden die **LVS \_ Ex \_ FullRowSelect** -Stil gelöscht, aber alle anderen Stile bleiben unverändert.

Aus Gründen der Abwärtskompatibilität wurde das ListView-Element " [**\_ abtextendedlistviewstyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) " nicht für die Verwendung von *wParam* aktualisiert. Wenn Sie den *wParam* -Wert verwenden möchten, verwenden Sie das ListView-Makro " [**\_ stextendecodlistviewstyleex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) ".

Wenn Sie diese Meldung verwenden, um die LVS-Zeichen für die [**\_ Post- \_ Kontrollkästchen**](extended-list-view-styles.md) festzulegen, werden alle zuvor festgelegten Status Bild Indizes verworfen. Alle Kontrollkästchen werden mit dem Status "deaktiviert" initialisiert. Der State Image Index ist in Bits 12 bis 15 des **State** -Members der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





