---
title: EM_FILELINELENGTH Meldung (kommstrg. h)
description: Ruft die Länge einer Zeile in einem Bearbeitungs Steuerelement (in Zeichen) unabhängig von der Anzeige von Linien auf dem Bildschirm ab.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- Windows-Steuerelemente für EM_FILELINELENGTH Meldung
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
ms.openlocfilehash: 4aa50f4d9b49253a558095be78e0e781d7d4c7f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517984"
---
# <a name="em_filelinelength-message"></a>EM \_ filelinelength-Meldung

Ruft die Länge einer Zeile in einem Bearbeitungs Steuerelement (in Zeichen) unabhängig von der Anzeige von Linien auf dem Bildschirm ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Zeichen Index eines Zeichens in der Zeile, deren Länge abgerufen werden soll. Wenn dieser Parameter größer als die Anzahl der Zeichen im-Steuerelement ist, ist der Rückgabewert 0 (null).

Dieser Parameter kann-1 sein. In diesem Fall gibt die Nachricht die Anzahl der nicht ausgewählten Zeichen in Zeilen zurück, die ausgewählte Zeichen enthalten. Wenn die Auswahl z. b. vom vierten Zeichen einer Zeile bis zum achten Zeichen vom Ende der nächsten Zeile aus verlängert wird, wäre der Rückgabewert 10 (drei Zeichen in der ersten Zeile und sieben bei der nächsten Zeile).

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Für mehrzeilige Bearbeitungs Steuerelemente ist der Rückgabewert die Länge in **TCHAR** s der durch den *wParam* -Parameter angegebenen Zeile, unabhängig davon, wie Zeilen auf dem Bildschirm angezeigt werden. Das Wagen Rücklauf Zeichen oder das Zeilenvorschub Zeichen am Ende der Zeile ist nicht enthalten.

Für einzeilige Bearbeitungs Steuerelemente ist der Rückgabewert die Länge des Texts im Bearbeitungs Steuerelement in **TCHAR** s.

Wenn *wParam* größer als die Anzahl der Zeichen im-Steuerelement ist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die [**EM \_ filelineindex**](em-lineindex.md) -Nachricht, um einen Zeichen Index für eine bestimmte Zeilennummer innerhalb eines mehrzeiligen Bearbeitungs Steuer Elements abzurufen, unabhängig davon, wie Linien auf dem Bildschirm angezeigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10, 1809 \[ Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2019 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ filelineingedex**](em-filelineindex.md)
</dt> </dl>

 

 





