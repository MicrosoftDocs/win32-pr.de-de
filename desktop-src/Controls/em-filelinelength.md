---
title: EM_FILELINELENGTH (CommCtrl.h)
description: Ruft die Länge einer Zeile in einem Bearbeitungssteuerzeichen in Zeichen ab, unabhängig davon, wie Zeilen auf dem Bildschirm angezeigt werden.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- EM_FILELINELENGTH von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- EM_FILELINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cb05b0e2acbfb5049eddefab1dad42ecd7b6db234fa4a3c34d4877ed52b007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915540"
---
# <a name="em_filelinelength-message"></a>EM \_ FILELINELENGTH-Nachricht

Ruft die Länge einer Zeile in einem Bearbeitungssteuerzeichen in Zeichen ab, unabhängig davon, wie Zeilen auf dem Bildschirm angezeigt werden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Zeichenindex eines Zeichens in der Zeile, dessen Länge abgerufen werden soll. Wenn dieser Parameter größer als die Anzahl der Zeichen im Steuerelement ist, ist der Rückgabewert 0 (null).

Dieser Parameter kann -1 sein. In diesem Fall gibt die Meldung die Anzahl der nicht ausgewählten Zeichen in Zeilen zurück, die ausgewählte Zeichen enthalten. Beispiel: Wenn die Auswahl vom vierten Zeichen einer Zeile bis zum achten Zeichen vom Ende der nächsten Zeile erweitert wird, beträgt der Rückgabewert 10 (drei Zeichen in der ersten Zeile und sieben Zeichen in der nächsten Zeile).

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Mehrzeilen-Bearbeitungssteuerelementen ist der Rückgabewert die Länge der durch den *wParam-Parameter* angegebenen Zeile in **TCHAR** s, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden. Das Wagenrücklauf- oder Zeilenumlaufzeichen am Ende der Zeile ist nicht enthalten.

Bei Einzeilen-Bearbeitungssteuerelementen ist der Rückgabewert die Länge des Texts im Bearbeitungssteuerfeld in **TCHAR** s.

Wenn *wParam* größer als die Anzahl der Zeichen im Steuerelement ist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

Verwenden Sie [**die MELDUNG EM \_ FILELINEINDEX,**](em-lineindex.md) um einen Zeichenindex für eine bestimmte Zeilennummer innerhalb eines mehrzeilenigen Bearbeitungssteuerzeichens abzurufen, unabhängig davon, wie Zeilen auf dem Bildschirm angezeigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur 1809 \[ Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2019-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ FILELINEINDEX**](em-filelineindex.md)
</dt> </dl>

 

 





