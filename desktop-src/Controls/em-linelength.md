---
title: EM_LINELENGTH-Nachricht (Winuser.h)
description: Ruft die Länge einer Zeile in einem Bearbeitungssteuerelement in Zeichen ab. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- EM_LINELENGTH Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_LINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 941a14a40cdc8f0ba0457cff8c789659a4ac3db76e01cd2a1c30047ab888d971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118171389"
---
# <a name="em_linelength-message"></a>EM \_ LINELENGTH-Nachricht

Ruft die Länge einer Zeile in einem Bearbeitungssteuerelement in Zeichen ab. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Zeichenindex eines Zeichens in der Zeile, dessen Länge abgerufen werden soll. Wenn dieser Parameter größer als die Anzahl der Zeichen im Steuerelement ist, ist der Rückgabewert 0 (null).

Dieser Parameter kann -1 sein. In diesem Fall gibt die Nachricht die Anzahl der nicht ausgewählten Zeichen in Zeilen zurück, die ausgewählte Zeichen enthalten. Wenn die Auswahl z. B. vom vierten Zeichen einer Zeile bis zum achten Zeichen vom Ende der nächsten Zeile aus erweitert wird, ist der Rückgabewert 10 (drei Zeichen in der ersten Zeile und sieben in der nächsten).

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei mehrzeiligen Bearbeitungssteuerelementen entspricht der Rückgabewert der Länge der zeile, die vom *wParam-Parameter* angegeben wird, in **TCHAR** s. Für ANSI-Text ist dies die Anzahl von Bytes. Für Unicode-Text ist dies die Anzahl der Zeichen. Das Wagenrücklaufzeichen am Ende der Zeile ist nicht enthalten.

Bei einzeiligen Bearbeitungssteuerelementen ist der Rückgabewert die Länge des Texts im Bearbeitungssteuerelement in **TCHAR** s.

Wenn *wParam* größer als die Anzahl der Zeichen im Steuerelement ist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

Verwenden Sie die [**EM \_ LINEINDEX-Nachricht,**](em-lineindex.md) um einen Zeichenindex für eine bestimmte Zeilennummer innerhalb eines mehrzeiligen Bearbeitungssteuerelements abzurufen.

**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ LINEINDEX**](em-lineindex.md)
</dt> </dl>

 

 





