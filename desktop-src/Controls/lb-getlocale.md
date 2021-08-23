---
title: LB_GETLOCALE (Winuser.h)
description: Ruft das aktuelle Locale des Listenfelds ab. Sie können das -Locale verwenden, um die richtige Sortierreihenfolge des angezeigten Texts (für Listenfelder mit dem LBS SORT-Format) und des von der \_ LB ADDSTRING-Meldung hinzugefügten Texts \_ zu bestimmen.
ms.assetid: ec814b03-5ce2-4b81-a36c-ab4c115f88be
keywords:
- LB_GETLOCALE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 732bfac72502c38265f7c1651667dc235c440293c8435f16088eaee775a874f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544520"
---
# <a name="lb_getlocale-message"></a>LB \_ GETLOCALE-Nachricht

Ruft das aktuelle Locale des Listenfelds ab. Sie können das -Locale verwenden, um die richtige Sortierreihenfolge des angezeigten Texts (für Listenfelder mit [**dem LBS \_ SORT-Format)**](list-box-styles.md) und des von der [**LB \_ ADDSTRING-Meldung**](lb-addstring.md) hinzugefügten Texts zu bestimmen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert gibt das aktuelle Locale des Listenfelds an. Das [**HIWORD enthält**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) den Länder-/Regioncode und [**das LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) den Sprachbezeichner.

## <a name="remarks"></a>Hinweise

Der Sprachbezeichner besteht aus einem Bezeichner für die Untersprache und einem Bezeichner der primären Sprache. Verwenden Sie [**das PRIMARYLANGID-Makro,**](/windows/desktop/api/winnt/nf-winnt-primarylangid) um den Bezeichner der primären Sprache aus [**dem LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) des Rückgabewerts zu extrahieren, und das [**SUBLANGID-Makro,**](/windows/desktop/api/winnt/nf-winnt-sublangid) um den Bezeichner für die Untersprache zu extrahieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ SETLOCALE**](lb-setlocale.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**PRIMARYLANGID**](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[**SUBLANGID**](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

