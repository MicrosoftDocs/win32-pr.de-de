---
title: PSM_INDEXTOID Meldung (prsht. h)
description: Nimmt den Index einer Eigenschaften Blattseite an und gibt die zugehörige Ressourcen-ID zurück. Sie können diese Nachricht explizit senden oder das propsheet- \_ indextoid-Makro verwenden.
ms.assetid: c153675a-360f-4916-aa0b-500636dd9022
keywords:
- Windows-Steuerelemente für PSM_INDEXTOID Meldung
topic_type:
- apiref
api_name:
- PSM_INDEXTOID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643861ecb6dc11d949483defc282d6d65648bdca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040761"
---
# <a name="psm_indextoid-message"></a>PSM- \_ indextoid-Nachricht

Nimmt den Index einer Eigenschaften Blattseite an und gibt die zugehörige Ressourcen-ID zurück. Sie können diese Nachricht explizit senden oder das [**propsheet- \_ indextoid**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) -Makro verwenden.

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

Gibt bei erfolgreicher Ausführung die Ressourcen-ID der Eigenschaften Blattseite zurück, die von *wParam* angegeben wurde. Andernfalls wird 0 (null) zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





