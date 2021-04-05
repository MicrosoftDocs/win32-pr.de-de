---
title: EM_LINELENGTH Meldung (Winuser. h)
description: Ruft die Länge einer Zeile in einem Bearbeitungs Steuerelement in Zeichen ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- Windows-Steuerelemente für EM_LINELENGTH Meldung
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
ms.openlocfilehash: ce3cbf59cbe31886e55c34bce9f7c2421e431012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859130"
---
# <a name="em_linelength-message"></a>EM- \_ LineLength-Nachricht

Ruft die Länge einer Zeile in einem Bearbeitungs Steuerelement in Zeichen ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

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

Für mehrzeilige Bearbeitungs Steuerelemente ist der Rückgabewert die Länge in **TCHAR** s der durch den *wParam* -Parameter angegebenen Zeile. Bei ANSI-Text ist dies die Anzahl der Bytes. bei Unicode-Text ist dies die Anzahl der Zeichen. Das Wagen Rücklauf Zeichen am Ende der Zeile ist nicht enthalten.

Für einzeilige Bearbeitungs Steuerelemente ist der Rückgabewert die Länge des Texts im Bearbeitungs Steuerelement in **TCHAR** s.

Wenn *wParam* größer als die Anzahl der Zeichen im-Steuerelement ist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die [**EM \_ lineindex**](em-lineindex.md) -Nachricht, um einen Zeichen Index für eine bestimmte Zeilennummer innerhalb eines mehrzeiligen Bearbeitungs Steuer Elements abzurufen.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ Linan DEX**](em-lineindex.md)
</dt> </dl>

 

 





