---
title: CB_SETLOCALE (Winuser.h)
description: Eine Anwendung sendet eine CB \_ SETLOCALE-Nachricht, um das aktuelle Locale des Kombinationsfelds zu festlegen. Wenn das Kombinationsfeld über den CBS SORT-Stil verfügt und Zeichenfolgen mit CB ADDSTRING hinzugefügt werden, wirkt sich das Locale eines Kombinationsfelds darauf aus, wie \_ \_ Listenelemente sortiert werden.
ms.assetid: 06f9c69d-1220-490f-bc67-6e125f696e87
keywords:
- CB_SETLOCALE von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- CB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1647d8ff4c7a4625151a9ec099800549d831f6b55a7ef6cc6b5ead365e80e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063301"
---
# <a name="cb_setlocale-message"></a>CB \_ SETLOCALE-Nachricht

Eine Anwendung sendet eine **CB \_ SETLOCALE-Nachricht,** um das aktuelle Locale des Kombinationsfelds zu festlegen. Wenn das Kombinationsfeld über den [**CBS \_ SORT-Stil**](combo-box-styles.md) verfügt und Zeichenfolgen mit [**CB \_ ADDSTRING**](cb-addstring.md)hinzugefügt werden, wirkt sich das -Locale eines Kombinationsfelds darauf aus, wie Listenelemente sortiert werden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Locale Identifier für das Kombinationsfeld an, das beim Hinzufügen von Text zum Sortieren verwendet werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der vorherige Locale Identifier. Wenn *wParam ein* nicht auf dem System installiertes Locale angibt, ist der Rückgabewert CB ERR, und das aktuelle Kombinationsfeld-Locale \_ wird nicht geändert.

## <a name="remarks"></a>Hinweise

Verwenden Sie [**das MAKELCID-Makro,**](/windows/desktop/api/winnt/nf-winnt-makelcid) um einen Locale Identifier zu erstellen, und das [**MAKELANGID-Makro,**](/windows/desktop/api/winnt/nf-winnt-makelangid) um einen Sprachbezeichner zu erstellen. Der Sprachbezeichner besteht aus einem Bezeichner der primären Sprache und einem Bezeichner für die Untersprache.

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

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ GETLOCALE**](cb-getlocale.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid)
</dt> <dt>

[**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid)
</dt> </dl>

 

