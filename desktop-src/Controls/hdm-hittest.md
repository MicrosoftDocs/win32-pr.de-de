---
title: HDM_HITTEST-Nachricht (Commctrl.h)
description: Testet einen Punkt, um zu bestimmen, welches Headerelement sich ggf. am angegebenen Punkt befindet.
ms.assetid: ff866bd1-9f2a-457c-921d-549610ab9088
keywords:
- HDM_HITTEST Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- HDM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc219640d9dd9d5d9a4c9537169401f681e37660554266b3edd653365cf8cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544770"
---
# <a name="hdm_hittest-message"></a>\_HDM-HITTEST-Nachricht

Testet einen Punkt, um zu bestimmen, welches Headerelement sich ggf. am angegebenen Punkt befindet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**HDHITTESTINFO-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) die die position zum Testen enthält und Informationen über die Ergebnisse des Tests empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des Elements an der angegebenen Position zurück, sofern vorhanden, oder andernfalls 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





