---
title: LB_GETTEXT-Nachricht (Winuser.h)
description: Ruft eine Zeichenfolge aus einem Listenfeld ab.
ms.assetid: 6bf7ec3b-237b-4668-9493-40c098a32428
keywords:
- LB_GETTEXT Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 9b2aa37a2d07e440aac615d1edc1e6f91c6a60e71a96418cd443daff9809ec18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434099"
---
# <a name="lb_gettext-message"></a>LB \_ GETTEXT-Nachricht

Ruft eine Zeichenfolge aus einem Listenfeld ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der nullbasierte Index der abzurufenden Zeichenfolge.

Windows 95/Windows 98/Windows Edition (Windows Me): Der *wParam-Parameter* ist auf 16-Bit-Werte beschränkt. Das bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, ist die Gesamtgröße der Elemente in einem Listenfeld in Byte nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf den Puffer, der die Zeichenfolge empfängt. es ist vom Typ **LPTSTR,** der anschließend in eine **LPARAM-Datei** umgeformt wird. Der Puffer muss über ausreichend Speicherplatz für die Zeichenfolge und ein abschließendes NULL-Zeichen verfügen. Eine [**LB \_ GETTEXTLEN-Nachricht**](lb-gettextlen.md) kann vor der **LB \_ GETTEXT-Nachricht** gesendet werden, um die Länge der Zeichenfolge in **TCHAR** s abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Länge der Zeichenfolge in **TCHAR** s, mit Ausnahme des abschließenden NULL-Zeichens. Wenn *wParam* keinen gültigen Index angibt, lautet der Rückgabewert LB \_ ERR.

## <a name="remarks"></a>Hinweise

Wenn das Listenfeld über einen vom Besitzer gezeichneten Stil, aber nicht über den [**LBS \_ HASSTRINGS-Stil**](list-box-styles.md) verfügt, empfängt der Puffer, auf den der *lParam-Parameter* zeigt, den wert, der dem Element (den Elementdaten) zugeordnet ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**LB \_ GETTEXTLEN**](lb-gettextlen.md)
</dt> </dl>

 

 





