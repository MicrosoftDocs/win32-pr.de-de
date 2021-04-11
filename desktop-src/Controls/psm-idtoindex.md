---
title: PSM_IDTOINDEX Meldung (prsht. h)
description: Übernimmt die Ressourcen-ID einer Eigenschaften Blattseite und gibt ihren Null basierten Index zurück. Sie können diese Nachricht explizit senden oder das propsheet- \_ iddeindex-Makro verwenden.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_idtoindex.htm
keywords:
- Windows-Steuerelemente für PSM_IDTOINDEX Meldung
topic_type:
- apiref
api_name:
- PSM_IDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f098c37ba30e33685abedf9dccd3ffc7c303acb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105273"
---
# <a name="psm_idtoindex-message"></a>PSM- \_ idumindex-Meldung

Übernimmt die Ressourcen-ID einer Eigenschaften Blattseite und gibt ihren Null basierten Index zurück. Sie können diese Nachricht explizit senden oder das [**propsheet- \_ iddeindex**](/windows/desktop/api/Prsht/nf-prsht-propsheet_idtoindex) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Die Ressourcen-ID der Seite.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung den NULL basierten Index der Eigenschaften Blattseite zurück, die von *LPARAM* angegeben wird. Andernfalls wird –1 zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





