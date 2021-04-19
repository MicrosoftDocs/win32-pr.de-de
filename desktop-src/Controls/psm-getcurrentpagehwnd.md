---
title: PSM_GETCURRENTPAGEHWND Meldung (prsht. h)
description: Ruft ein Handle für das Fenster der aktuellen Seite eines Eigenschaften Blatts ab. Sie können diese Nachricht explizit oder mithilfe des propsheet \_ getcurrentpgehwnd-Makros senden.
ms.assetid: 1f2d0af9-5853-48e7-b827-483be032b6ca
keywords:
- Windows-Steuerelemente für PSM_GETCURRENTPAGEHWND Meldung
topic_type:
- apiref
api_name:
- PSM_GETCURRENTPAGEHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae9ac89e6bc60317f2caf31ea92754d10983e11a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346746"
---
# <a name="psm_getcurrentpagehwnd-message"></a>PSM \_ getcurrentpagehwnd-Meldung

Ruft ein Handle für das Fenster der aktuellen Seite eines Eigenschaften Blatts ab. Sie können diese Nachricht explizit oder mithilfe des [**propsheet \_ getcurrentpgehwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) -Makros senden.

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

Gibt ein Handle für das Fenster der aktuellen Eigenschaften Blattseite zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **PSM \_ getcurrentpagehwnd** -Nachricht mit nicht modalem Eigenschaften Blatt, um zu bestimmen, wann das Dialogfeld zerstört werden soll. Wenn der Benutzer auf die Schaltfläche **OK** oder **Abbrechen** klickt, gibt **PSM \_ getcurrentpagehwnd** **null** zurück, und Sie können dann die [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) -Funktion verwenden, um das Dialogfeld zu zerstören.

> [!Note]  
> Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften Blatt**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

