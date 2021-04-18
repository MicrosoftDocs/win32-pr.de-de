---
title: PSM_RECALCPAGESIZES Meldung (prsht. h)
description: Berechnet die Seitengröße eines Standard-oder Assistenten-Eigenschaften Blatts neu, nachdem Seiten hinzugefügt oder entfernt wurden. Sie können diese Nachricht explizit senden oder das propsheet \_ recalcpagesizes-Makro verwenden.
ms.assetid: 42257ea3-0471-4c67-adcd-01cd2669a51e
keywords:
- Windows-Steuerelemente für PSM_RECALCPAGESIZES Meldung
topic_type:
- apiref
api_name:
- PSM_RECALCPAGESIZES
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ae2030f432e8c52ed6208be34d429b4579edb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338779"
---
# <a name="psm_recalcpagesizes-message"></a>PSM- \_ Nachricht "recalcpagesizes"

Berechnet die Seitengröße eines Standard-oder Assistenten-Eigenschaften Blatts neu, nachdem Seiten hinzugefügt oder entfernt wurden. Sie können diese Nachricht explizit senden oder das [**propsheet \_ recalcpagesizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Wenn ein Eigenschaften Blatt erstellt wird, wird es an seine anfängliche Auflistung von Seiten angepasst. Um die Kompatibilität mit früheren Versionen der allgemeinen Steuerelemente aufrechtzuerhalten, ändern sich Eigenschaften Blätter und Assistenten nicht automatisch selbst, wenn Seiten später hinzugefügt oder entfernt werden. Mit der Common Controls- [Version 5,80](common-control-versions.md)sollten Anwendungen nach dem Hinzufügen oder Entfernen von Seiten mit [**PSM \_ addPage**](psm-addpage.md), [**PSM \_ insertpage**](psm-insertpage.md), [**PSM \_ RemovePage**](psm-removepage.md)oder Ihren äquivalenten Makros eine PSM-Nachricht " **\_ recalcpagesizes** " senden. Dadurch wird sichergestellt, dass das Eigenschaften Blatt für die aktuelle Auflistung von Seiten ordnungsgemäß vergrößert wird. Wenn diese Nachricht nicht gesendet wird, können einige Eigenschaften Blattseiten abgeschnitten oder zu groß sein.

> [!Note]  
> Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





