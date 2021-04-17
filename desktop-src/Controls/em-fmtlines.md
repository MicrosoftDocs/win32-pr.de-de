---
title: EM_FMTLINES Meldung (Winuser. h)
description: Legt ein Flag fest, das bestimmt, ob ein mehrzeilige Bearbeitungs Steuerelement weiche Zeilenumbruch Zeichen einschließt. Ein weicher Zeilenumbruch besteht aus zwei Wagen Rückläufen und einem Zeilenvorschub und wird am Ende einer Zeile eingefügt, die aufgrund von wordwrapping unterbrochen wird.
ms.assetid: bfc08062-b0a7-4ba7-8858-00cb20895c77
keywords:
- Windows-Steuerelemente für EM_FMTLINES Meldung
topic_type:
- apiref
api_name:
- EM_FMTLINES
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c12a22ee8c30ffa74705f670a16caa3651e9b44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477118"
---
# <a name="em_fmtlines-message"></a>EM-Fehler \_ Zeilen Meldung

Legt ein Flag fest, das bestimmt, ob ein mehrzeilige Bearbeitungs Steuerelement weiche Zeilenumbruch Zeichen einschließt. Ein weicher Zeilenumbruch besteht aus zwei Wagen Rückläufen und einem Zeilenvorschub und wird am Ende einer Zeile eingefügt, die aufgrund von wordwrapping unterbrochen wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob weiche Zeilenumbruch Zeichen eingefügt werden sollen. Der Wert **true** fügt die Zeichen ein. bei einem Wert von **false** werden diese entfernt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist identisch mit dem *wParam* -Parameter.

## <a name="remarks"></a>Bemerkungen

Diese Nachricht wirkt sich nur auf den Puffer aus, der von der [**EM \_ GetHandle**](em-gethandle.md) -Nachricht zurückgegeben wird, und auf den Text, der von der [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext) Dies hat keine Auswirkung auf die Anzeige des Texts innerhalb des Bearbeitungs Steuer Elements.

Die **EM- \_ fmtlines** -Nachricht wirkt sich nicht auf eine Zeile aus, die mit einem harten Zeilenumbruch endet. Ein harter Zeilenumbruch besteht aus einem Wagen Rücklauf und einem Zeilenvorschub.

> [!Note]  
> Die Größe des Texts ändert sich, wenn diese Nachricht verarbeitet wird.

 

Umfassende **Bearbeitung:** Die **EM \_** -Meldung wird nicht unterstützt.

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

[**EM \_ GetHandle**](em-gethandle.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

