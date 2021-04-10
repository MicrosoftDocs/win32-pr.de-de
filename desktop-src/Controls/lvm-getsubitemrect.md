---
title: LVM_GETSUBITEMRECT Meldung (kommstrg. h)
description: Ruft Informationen über das umgebende Rechteck für ein Unterelement in einem Listenansicht-Steuerelement ab.
ms.assetid: 985876b2-6eb3-4c96-88ea-ddec67ef5b5a
keywords:
- Windows-Steuerelemente für LVM_GETSUBITEMRECT Meldung
topic_type:
- apiref
api_name:
- LVM_GETSUBITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1184c52d60b86e008685b87c9f5555cf801b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105489"
---
# <a name="lvm_getsubitemrect-message"></a>LVM \_ getsubitemrect-Meldung

Ruft Informationen über das umgebende Rechteck für ein Unterelement in einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ getsubitemrect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) -Makros (empfohlen) senden. Diese Nachricht soll nur mit Listenansicht-Steuerelementen verwendet werden, die den [**LVS- \_ Berichts**](list-view-window-styles.md) Stil verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des übergeordneten Elements des unter Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Informationen zu umschließenden Rechtecks des unter Elements empfängt. Seine Member müssen gemäß den folgenden Element-/Wert-Beziehungen initialisiert werden:



| Wert                                                                                                                             | Bedeutung                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**top**</dt> </dl>    | Der einbasierte Index des unter Elements.<br/>                                                                                    |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**linken**</dt> </dl> | Flagwert (siehe Hinweise). Gibt den Teil des Listen Ansichts unter Elements an, für das das umgebende Rechteck abgerufen werden soll.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Im folgenden finden Sie die Flagwerte, die festgelegt werden können.



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------|
| **Flagwert** | **Bedeutung**                                                                                                         |
| lvir- \_ Begrenzungen   | Gibt das umgebende Rechteck des gesamten Elements zurück, einschließlich des Symbols und der Bezeichnung.                                    |
| lvir- \_ Symbol     | Gibt das umgebende Rechteck des Symbols oder des kleinen Symbols zurück.                                                           |
| lvir- \_ Bezeichnung    | Gibt das umgebende Rechteck des gesamten Elements zurück, einschließlich des Symbols und der Bezeichnung. Dies ist mit lvir- \_ Begrenzungen identisch. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

