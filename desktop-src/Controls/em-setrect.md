---
title: EM_SETRECT (Winuser.h)
description: 'EM_SETRECT Meldung: Legt das Formatierungsrechteck eines mehrzweckigen Bearbeitungssteuer steuerelements fest.'
ms.assetid: 4f576e94-3bd3-4416-a960-b7f22da963ea
keywords:
- EM_SETRECT Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- EM_SETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042428a236b8e9a23f03cdcceaf5d76eb977efd8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085968"
---
# <a name="em_setrect-message"></a>EM \_ SETRECT-Nachricht

Legt das [Formatierungsrechteck eines](about-edit-controls.md) mehrzweckigen Bearbeitungssteuer steuerelements fest. Das Formatierungrechteck ist das einschränkende Rechteck, in das das Steuerelement den Text zeichnet. Das einschränkende Rechteck ist unabhängig von der Größe des Bearbeitungssteuerfensters.

Diese Meldung wird nur von mehrline-Bearbeitungssteuerelementen verarbeitet. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

**Rich Edit 2.0 und höher:** Gibt an, *ob lParam* absolute oder relative Koordinaten angibt. Der Wert 0 (null) gibt absolute Koordinaten an. Der Wert 1 gibt Offsets relativ zum aktuellen Formatierungsrechteck an. (Die Offsets können positiv oder negativ sein.)

**Steuerelemente bearbeiten und Rich Edit 1.0:** Dieser Parameter wird nicht verwendet und muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) die die neuen Dimensionen des Rechtecks angibt. Wenn dieser Parameter **NULL ist,** wird das Formatierungsrechteck auf seine Standardwerte festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Das *Festlegen von lParam* auf **NULL** hat keine Auswirkungen, wenn ein Touchgerät installiert ist oder **EM \_ SETRECT** von einem Thread gesendet wird, auf dem ein Hook installiert ist (siehe [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)). In diesen Fällen sollte *lParam* einen gültigen Zeiger auf eine [**RECT-Struktur**](/previous-versions//dd162897(v=vs.85)) enthalten.

Die **EM \_ SETRECT-Meldung** bewirkt, dass der Text des Bearbeitungssteuerfelds neu gezeichnet wird. Verwenden Sie die [**EM \_ SETRECTNP-Meldung,**](em-setrectnp.md) um die Größe des Formatierungsrechtecks zu ändern, ohne den Text neu zu zeichnen.

Wenn ein Bearbeitungssteuerelement zum ersten Mal erstellt wird, wird das Formatierungsrechteck auf eine Standardgröße festgelegt. Sie können die **EM \_ SETRECT-Nachricht** verwenden, um das Formatierungsrechteck größer oder kleiner als das Bearbeitungssteuerelementfenster zu machen.

Wenn das Bearbeitungssteuerelement keine horizontale Bildlaufleiste aufweist und das Formatierungsrechteck größer als das Bearbeitungssteuerelementfenster ist, werden Textzeilen, die die Breite des Bearbeitungssteuerelementfensters überschreiten (aber kleiner als die Breite des Formatierungsrechtecks sind), abgeschnitten und nicht umschlossen.

Wenn das Bearbeitungssteuerelement einen Rahmen enthält, wird das Formatierungsrechteck um die Größe des Rahmens reduziert. Wenn Sie das von einer [**EM \_ GETRECT-Nachricht**](em-getrect.md) zurückgegebene Rechteck anpassen, müssen Sie die Größe des Rahmens entfernen, bevor Sie das Rechteck mit der **EM \_ SETRECT-Nachricht** verwenden.

**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Das Formatierungsrechteck enthält nicht die Auswahlleiste, bei der es sich um einen nicht markierten Bereich links neben jedem Absatz handelt. Wenn der Benutzer auf die Auswahlleiste klickt, wird die entsprechende Zeile ausgewählt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (windows.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ GETRECT**](em-getrect.md)
</dt> <dt>

[**EM \_ SETRECTNP**](em-setrectnp.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

