---
title: LB_GETTEXT Meldung (Winuser. h)
description: Ruft eine Zeichenfolge aus einem Listenfeld ab.
ms.assetid: 6bf7ec3b-237b-4668-9493-40c098a32428
keywords:
- Windows-Steuerelemente für LB_GETTEXT Meldung
topic_type:
- apiref
api_name:
- LB_GETTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dd5e2c7a9e6c1c1aa1b847592555a013766134
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478258"
---
# <a name="lb_gettext-message"></a>LB- \_ gettext-Nachricht

Ruft eine Zeichenfolge aus einem Listenfeld ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index der abzurufenden Zeichenfolge.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf den Puffer, der die Zeichenfolge empfängt. der Typ ist **LPTSTR** , der anschließend in ein **LPARAM** umgewandelt wird. Der Puffer muss über ausreichend Speicherplatz für die Zeichenfolge und ein abschließendes NULL-Zeichen verfügen. Eine [**lb- \_ gettextlen**](lb-gettextlen.md) -Nachricht kann vor der **lb- \_ gettext** -Nachricht gesendet werden, um die Länge der Zeichenfolge in **TCHAR** s abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Länge der Zeichenfolge in **TCHAR** s, wobei das abschließende Null-Zeichen ausgeschlossen wird. Wenn von *wParam* kein gültiger Index angegeben wird, ist der Rückgabewert lb \_ Err.

## <a name="remarks"></a>Bemerkungen

Wenn im Listenfeld ein vom Besitzer gezeichneter Stil, aber nicht der [**lbs \_ hasstrings**](list-box-styles.md) -Stil enthalten ist, erhält der Puffer, auf den der *LPARAM* -Parameter verweist, den Wert, der dem Element zugeordnet ist (die Elementdaten).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LB- \_ gettextlen**](lb-gettextlen.md)
</dt> </dl>

 

 





