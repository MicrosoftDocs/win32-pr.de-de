---
title: LB_GETLOCALE Meldung (Winuser. h)
description: Ruft das aktuelle Gebiets Schema des Listen Felds ab. Sie können das Gebiets Schema verwenden, um die richtige Sortierreihenfolge des angezeigten Texts (für Listenfelder mit dem lbs \_ -Sortier Stil) und des von der LB AddString-Nachricht hinzugefügten Texts zu bestimmen \_ .
ms.assetid: ec814b03-5ce2-4b81-a36c-ab4c115f88be
keywords:
- Windows-Steuerelemente für LB_GETLOCALE Meldung
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
ms.openlocfilehash: 57620b62011dba234710caf1b5d1c429da37ace9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477289"
---
# <a name="lb_getlocale-message"></a>\_GetLocale-Nachricht des lb

Ruft das aktuelle Gebiets Schema des Listen Felds ab. Sie können das Gebiets Schema verwenden, um die richtige Sortierreihenfolge des angezeigten Texts (für Listenfelder mit dem [**lbs- \_ Sortier**](list-box-styles.md) Stil) und des von der [**lb \_ AddString**](lb-addstring.md) -Nachricht hinzugefügten Texts zu bestimmen.

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

Der Rückgabewert gibt das aktuelle Gebiets Schema des Listen Felds an. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) enthält den Länder-/Regionscode, und das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den sprach Bezeichner.

## <a name="remarks"></a>Bemerkungen

Die Sprach-ID besteht aus einer unter Sprachen-ID und einem primären sprach Bezeichner. Verwenden Sie das [**primarylangid**](/windows/desktop/api/winnt/nf-winnt-primarylangid) -Makro, um den Bezeichner der Primärsprache aus dem [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) des Rückgabewerts zu extrahieren, und das [**sublangid**](/windows/desktop/api/winnt/nf-winnt-sublangid) -Makro, um die unter Sprachen-ID zu extrahieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**LB- \_ AddString**](lb-addstring.md)
</dt> <dt>

[**LB- \_ setlocale**](lb-setlocale.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Primarylangid**](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[**Sublangid**](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

