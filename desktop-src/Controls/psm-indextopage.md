---
title: PSM_INDEXTOPAGE Meldung (prsht. h)
description: Nimmt den Index einer Eigenschaften Blattseite an und gibt das hpropsheetpage-Handle zurück. Sie können diese Nachricht explizit senden oder das propsheet \_ indextopage-Makro verwenden.
ms.assetid: b14b35ad-bae0-4461-a90f-e2bc5e2ccfc2
keywords:
- Windows-Steuerelemente für PSM_INDEXTOPAGE Meldung
topic_type:
- apiref
api_name:
- PSM_INDEXTOPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38f7a5658dbd92f4208e084f1df47a4dc3582156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478240"
---
# <a name="psm_indextopage-message"></a>PSM- \_ indextopage-Nachricht

Nimmt den Index einer Eigenschaften Blattseite an und gibt das hpropsheetpage-Handle zurück. Sie können diese Nachricht explizit senden oder das [**propsheet \_ indextopage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index der Seite.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das hpropsheetpage-Handle der von *wParam* angegebenen Eigenschaften Blattseite zurück, wenn erfolgreich. Andernfalls wird 0 (null) zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





