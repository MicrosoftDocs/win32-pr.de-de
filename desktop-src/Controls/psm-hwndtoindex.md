---
title: PSM_HWNDTOINDEX Meldung (prsht. h)
description: Nimmt das Fenster Handle der Eigenschaften Blattseite an und gibt dessen Null basierten Index zurück. Sie können diese Nachricht explizit senden oder das propsheet- \_ hwnddeindex-Makro verwenden.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_hwndtoindex.htm
keywords:
- Windows-Steuerelemente für PSM_HWNDTOINDEX Meldung
topic_type:
- apiref
api_name:
- PSM_HWNDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6632d331a6f271e339663a23210d0b399fb669b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104198"
---
# <a name="psm_hwndtoindex-message"></a>PSM \_ hwnddeindex-Meldung

Nimmt das Fenster Handle der Eigenschaften Blattseite an und gibt dessen Null basierten Index zurück. Sie können diese Nachricht explizit senden oder das [**propsheet- \_ hwnddeindex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für das Fenster der Seite.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den NULL basierten Index der von *wParam* angegebenen Eigenschaften Blattseite zurück, wenn erfolgreich. Andernfalls wird –1 zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





