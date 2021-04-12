---
title: HDM_SETITEM Meldung (kommstrg. h)
description: Legt die Attribute des angegebenen Elements in einem Header Steuerelement fest. Sie können diese Nachricht explizit senden oder das Header-"*"- \_ Makro verwenden.
ms.assetid: c8f0d526-3ebe-48c5-8aea-ea3703e2d983
keywords:
- Windows-Steuerelemente für HDM_SETITEM Meldung
topic_type:
- apiref
api_name:
- HDM_SETITEM
- HDM_SETITEMA
- HDM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b03a05b909cf8c7887edd2031f5346c419f1cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478267"
---
# <a name="hdm_setitem-message"></a>HDM- \_ Nachricht

Legt die Attribute des angegebenen Elements in einem Header Steuerelement fest. Sie können diese Nachricht explizit senden oder das Header-"*"-Makro verwenden. [**\_**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der aktuelle Index des Elements, dessen Attribute geändert werden sollen.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) -Struktur, die Element Informationen enthält. Wenn diese Nachricht gesendet wird, muss der **Mask** -Member der-Struktur festgelegt werden, um anzugeben, welche Attribute festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Die [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) -Struktur, die diese Meldung unterstützt, unterstützt Element Reihenfolge-und Bildlisten Informationen Mithilfe dieser Member können Sie die Reihenfolge steuern, in der Elemente angezeigt werden, und Bilder angeben, die mit Elementen angezeigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **HDM \_** "S" (Unicode) und " **HDM \_** " (ANSI)<br/>                   |



 

 





