---
title: CQPM_HELP Meldung (cmnquery. h)
description: Wird an die cqpageproc-Rückruffunktion einer Abfrageformular Erweiterungs Seite gesendet, damit die Seiten Erweiterung die kontextbezogene Hilfe für die Seite anzeigen kann.
ms.assetid: 07f5bd24-bca2-4d87-8e1e-acce552a3bf2
ms.tgt_platform: multiple
keywords:
- CQPM_HELP Meldung Active Directory
topic_type:
- apiref
api_name:
- CQPM_HELP
api_location:
- Cmnquery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7635b87a0ba489c63f87fb32742c37a9f7044860
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103066"
---
# <a name="cqpm_help-message"></a>Cqpm- \_ Hilfe Meldung

Die **cqpm- \_ Hilfe** Nachricht wird an die [**cqpageproc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) -Rückruffunktion einer Abfrageformular Erweiterungs Seite gesendet, damit die Seiten Erweiterung die kontextbezogene Hilfe für die Seite anzeigen kann. Wenn möglich, sollte die Abfrage Seiten Erweiterung eine kontextbezogene Hilfe als Reaktion auf dieses Ereignis anzeigen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**helpinfo**](/windows/win32/api/winuser/ns-winuser-helpinfo) -Struktur, die zusätzliche Daten über das Menü Element, das Steuerelement, das Dialogfeld oder das Fenster enthält, für das die kontextbezogene Hilfe angefordert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cmnquery. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cqpageproc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc)
</dt> <dt>

[**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo)
</dt> </dl>

 

