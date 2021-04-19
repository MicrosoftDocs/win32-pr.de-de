---
title: PSM_SETHEADERTITLE Meldung (prsht. h)
description: Legt den Titeltext für den Header der inneren Seite eines Assistenten fest. Sie können diese Nachricht explizit senden oder das propsheet-" \_ .
ms.assetid: 19d4badf-d99d-4a28-92d4-33bcf5d23944
keywords:
- Windows-Steuerelemente für PSM_SETHEADERTITLE Meldung
topic_type:
- apiref
api_name:
- PSM_SETHEADERTITLE
- PSM_SETHEADERTITLEA
- PSM_SETHEADERTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8140eef4aa09e9dd19d8baaf8193a836b105482e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342403"
---
# <a name="psm_setheadertitle-message"></a>PSM-Einstellungs \_ Titel Meldung

Legt den Titeltext für den Header der inneren Seite eines Assistenten fest. Sie können diese Nachricht explizit senden oder das [**propsheet- \_**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) ".

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

Wenn Sie die aktuelle Seite angeben, wird Sie sofort neu gezeichnet, um den neuen Titel anzuzeigen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **PSM \_ "Sderadertitlew** " (Unicode) und "PSM"-"Setup" (ANSI) **\_**<br/>  |



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

 

 





