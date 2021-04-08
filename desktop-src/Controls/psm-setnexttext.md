---
title: PSM_SETNEXTTEXT Meldung (prsht. h)
description: Legt den Text der Schaltfläche weiter in einem Assistenten fest. Sie können diese Nachricht explizit oder mithilfe des propsheet- \_ Makros setnexttext senden.
ms.assetid: 4608425e-1724-4d0b-b0f6-9fec147a85f6
keywords:
- Windows-Steuerelemente für PSM_SETNEXTTEXT Meldung
topic_type:
- apiref
api_name:
- PSM_SETNEXTTEXT
- PSM_SETNEXTTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d781a8d76fca5c1e74bcda452b6ab7e03a32aacc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740096"
---
# <a name="psm_setnexttext-message"></a>PSM- \_ setnexttext-Nachricht

Legt den Text der Schaltfläche **weiter** in einem Assistenten fest. Sie können diese Nachricht explizit oder mithilfe des [**propsheet-Makros \_ setnexttext**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf einen Puffer, der den Text enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein aussagekräftiger Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **PSM \_ Setnexttextw** (Unicode)<br/>                                         |



 

 





