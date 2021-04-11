---
title: CB_GETLOCALE Meldung (Winuser. h)
description: Ruft das aktuelle Gebiets Schema des Kombinations Felds ab. Das Gebiets Schema wird verwendet, um die richtige Sortierreihenfolge des angezeigten Texts für Kombinations Felder mit dem CBS \_ -Sortier Stil und Text zu bestimmen, der mithilfe der CB \_ AddString-Nachricht hinzugefügt wurde.
ms.assetid: 57c77ce2-bad0-43f3-8325-f2a7227994ec
keywords:
- Windows-Steuerelemente für CB_GETLOCALE Meldung
topic_type:
- apiref
api_name:
- CB_GETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847d9f73e8bf0b1d533d0b79ba86d939bee0e9b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040599"
---
# <a name="cb_getlocale-message"></a>CB \_ getLocale-Meldung

Ruft das aktuelle Gebiets Schema des Kombinations Felds ab. Das Gebiets Schema wird verwendet, um die richtige Sortierreihenfolge des angezeigten Texts für Kombinations Felder mit dem [**CBS- \_ Sortier**](combo-box-styles.md) Stil und Text zu bestimmen, der mithilfe der [**CB \_ AddString**](cb-addstring.md) -Nachricht hinzugefügt wurde.

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

Der Rückgabewert gibt das aktuelle Gebiets Schema des Kombinations Felds an. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) enthält den Länder-/Regionscode, und das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den sprach Bezeichner.

## <a name="remarks"></a>Bemerkungen

Die Sprach-ID besteht aus einer unter Sprachen-ID und einem primär Sprachen Bezeichner. Das [**primarylangid**](/windows/desktop/api/winnt/nf-winnt-primarylangid) -Makro erhält die primäre Sprachen-ID, und das [**sublangid**](/windows/desktop/api/winnt/nf-winnt-sublangid) -Makro erhält die unter Sprachen-ID.

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

[**CB \_ AddString**](cb-addstring.md)
</dt> <dt>

[**CB \_ setlocale**](cb-setlocale.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**Primarylangid**](/windows/desktop/api/winnt/nf-winnt-primarylangid)
</dt> <dt>

[**Sublangid**](/windows/desktop/api/winnt/nf-winnt-sublangid)
</dt> </dl>

 

