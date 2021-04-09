---
title: CB_DELETESTRING Meldung (Winuser. h)
description: Löscht eine Zeichenfolge im Listenfeld eines Kombinations Felds.
ms.assetid: 8d526796-04ef-4c01-94d6-fb50e6fef27b
keywords:
- Windows-Steuerelemente für CB_DELETESTRING Meldung
topic_type:
- apiref
api_name:
- CB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0d3900c86874db1113c219fd9f7967c5f6bb6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106004"
---
# <a name="cb_deletestring-message"></a>CB \_ deletestring-Meldung

Löscht eine Zeichenfolge im Listenfeld eines Kombinations Felds.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index der zu löschenden Zeichenfolge.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Anzahl der Zeichen folgen, die in der Liste verbleiben. Wenn der *wParam* -Parameter einen Index angibt, der größer als die Anzahl der Elemente in der Liste ist, lautet der Rückgabewert CB \_ Err.

## <a name="remarks"></a>Bemerkungen

Wenn Sie das Kombinations Feld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellen, sendet das System eine [**WM \_ DeleteItem**](wm-deleteitem.md) -Meldung an den Besitzer des Kombinations Felds, sodass die Anwendung alle zusätzlichen Daten freigeben kann, die dem Element zugeordnet sind.

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

[**CB \_ resetcontent**](cb-resetcontent.md)
</dt> <dt>

[**WM- \_ DeleteItem**](wm-deleteitem.md)
</dt> </dl>

 

 





