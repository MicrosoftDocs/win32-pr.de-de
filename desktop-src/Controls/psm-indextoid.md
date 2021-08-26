---
title: PSM_INDEXTOID-Nachricht (Prsht.h)
description: Übernimmt den Index einer Eigenschaftenblattseite und gibt dessen Ressourcen-ID zurück. Sie können diese Nachricht explizit senden oder das \_ PropSheet IndexToId-Makro verwenden.
ms.assetid: c153675a-360f-4916-aa0b-500636dd9022
keywords:
- PSM_INDEXTOID Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: bc7a26cd97d324ae9bb4cfee85df00387c59293c7de8817b67da5605a207f07f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985720"
---
# <a name="psm_indextoid-message"></a>PSM \_ INDEXTOID-Nachricht

Übernimmt den Index einer Eigenschaftenblattseite und gibt dessen Ressourcen-ID zurück. Sie können diese Nachricht explizit senden oder das [**PropSheet \_ IndexToId-Makro**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index der Seite.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Ressourcen-ID der Eigenschaftenblattseite zurück, die von *wParam* angegeben wird, falls erfolgreich. Andernfalls wird 0 (null) zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





