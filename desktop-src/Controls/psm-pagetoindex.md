---
title: PSM_PAGETOINDEX Meldung (prsht. h)
description: Nimmt das hpropsheetpage-Handle der Eigenschaften Blattseite an und gibt dessen Null basierten Index zurück. Sie können diese Nachricht explizit senden oder das "propsheet \_ Page$ Index"-Makro verwenden.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_pagetoindex.htm
keywords:
- Windows-Steuerelemente für PSM_PAGETOINDEX Meldung
topic_type:
- apiref
api_name:
- PSM_PAGETOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e3cb6688ab918da0dfae8affed36903e6dcea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344064"
---
# <a name="psm_pagetoindex-message"></a>PSM- \_ pageumindex-Meldung

Nimmt das hpropsheetpage-Handle der Eigenschaften Blattseite an und gibt dessen Null basierten Index zurück. Sie können diese Nachricht explizit senden oder das " [**propsheet \_ Page$ Index**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pagetoindex) "-Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Hpropsheetpage-Handle für die Eigenschaften Blattseite.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung den NULL basierten Index der Eigenschaften Blattseite zurück, die von *LPARAM* angegeben wird. Andernfalls wird –1 zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





