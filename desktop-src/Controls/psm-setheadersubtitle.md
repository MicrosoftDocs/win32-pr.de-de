---
title: PSM_SETHEADERSUBTITLE Meldung (prsht. h)
description: Legt den Untertitel Text für den Header der inneren Seite eines Assistenten fest. Sie können diese Nachricht explizit senden oder das propsheet-unter \_ Titel-Makro verwenden.
ms.assetid: 6ef3017b-8a20-4d62-a604-135410d8bdf7
keywords:
- Windows-Steuerelemente für PSM_SETHEADERSUBTITLE Meldung
topic_type:
- apiref
api_name:
- PSM_SETHEADERSUBTITLE
- PSM_SETHEADERSUBTITLEA
- PSM_SETHEADERSUBTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d73376b5ed35f20b43c743b31a4a78d3a4fa809
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949817"
---
# <a name="psm_setheadersubtitle-message"></a>PSM- \_ abadertitel-Nachricht

Legt den Untertitel Text für den Header der inneren Seite eines Assistenten fest. Sie können diese Nachricht explizit senden oder das [**propsheet-unter \_ Titel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index der Seite des Assistenten.

</dd> <dt>

*lParam* 
</dt> <dd>

Neuer Header Untertitel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Wenn Sie die aktuelle Seite angeben, wird Sie sofort neu gezeichnet, um den neuen Untertitel anzuzeigen.

> [!Note]  
> Diese Meldung wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl>      |
| Unicode- und ANSI-Name<br/>   | **PSM \_ "SDer adersubtitlew** (Unicode)" und "PSM"-"Setup" (ANSI) **\_**<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**PSM \_ hwndumindex**](psm-hwndtoindex.md)
</dt> <dt>

[**PSM \_ idumindex**](psm-idtoindex.md)
</dt> <dt>

[**PSM- \_ pageumindex**](psm-pagetoindex.md)
</dt> </dl>

 

 





