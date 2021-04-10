---
title: EM_SETRECT Meldung (Winuser. h)
description: Legt das Formatierungs Rechteck eines mehrzeiligen Bearbeitungs Steuer Elements fest.
ms.assetid: 4f576e94-3bd3-4416-a960-b7f22da963ea
keywords:
- Windows-Steuerelemente für EM_SETRECT Meldung
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
ms.openlocfilehash: a12b171478b0cb9d47496d20d4d1b6b1e8ddd29a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040545"
---
# <a name="em_setrect-message"></a>EM- \_ SetRect-Nachricht

Legt das [Formatierungs Rechteck](about-edit-controls.md) eines mehrzeiligen Bearbeitungs Steuer Elements fest. Das Formatierungs Rechteck ist das einschränkende Rechteck, in das das Steuerelement den Text zeichnet. Das Begrenzungs Rechteck ist unabhängig von der Größe des Bearbeitungs Steuer Elements.

Diese Meldung wird nur von mehrzeiligen Bearbeitungs Steuerelementen verarbeitet. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

**Rich Edit 2,0 und höher:** Gibt an, ob *LPARAM* absolute oder relative Koordinaten angibt. Der Wert 0 (null) gibt absolute Koordinaten an. Der Wert 1 gibt Offsets relativ zum aktuellen Formatierungs Rechteck an. (Die Offsets können positiv oder negativ sein.)

**Bearbeitungs Steuerelemente und umfangreiche Bearbeitung 1,0:** Dieser Parameter wird nicht verwendet und muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die neuen Abmessungen des Rechtecks angibt. Wenn dieser Parameter **null** ist, wird das Formatierungs Rechteck auf seine Standardwerte festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Das Festlegen von *LPARAM* auf **null** hat keine Auswirkungen, wenn ein Finger Eingabegerät installiert ist, oder wenn **EM \_ SetRect** von einem Thread gesendet wird, auf dem ein Hook installiert ist (siehe [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa)). In diesen Fällen sollte *LPARAM* einen gültigen Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur enthalten.

Die **EM- \_ SetRect** -Meldung bewirkt, dass der Text des Bearbeitungs Steuer Elements neu gezeichnet wird. Um die Größe des Formatierungs Rechtecks zu ändern, ohne den Text neu zu zeichnen, verwenden Sie die Nachricht [**EM \_ setrectnp**](em-setrectnp.md) .

Wenn ein Bearbeitungs Steuerelement erstmalig erstellt wird, wird das Formatierungs Rechteck auf eine Standardgröße festgelegt. Sie können die Nachricht **EM \_ SetRect** verwenden, um das Formatierungs Rechteck größer oder kleiner als das Bearbeitungs Steuerelement Fenster zu machen.

Wenn das Bearbeitungs Steuerelement keine horizontale Schiebe Leiste hat und das Formatierungs Rechteck auf größer als das Bearbeitungs Steuerelement festgelegt ist, werden Textzeilen, die die Breite des Bearbeitungs Steuer Elements überschreiten (jedoch kleiner als die Breite des Formatierungs Rechtecks), abgeschnitten anstatt umschließen.

Wenn das Bearbeitungs Steuerelement einen Rahmen enthält, wird das Formatierungs Rechteck um die Größe des Rahmens reduziert. Wenn Sie das von einer [**EM \_ GetRect**](em-getrect.md) -Nachricht zurückgegebene Rechteck anpassen, müssen Sie die Größe des Rahmens entfernen, bevor Sie das Rechteck mit der **EM- \_ SetRect** -Nachricht verwenden.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Das Formatierungs Rechteck enthält nicht die Auswahl Leiste, bei der es sich um einen nicht markierten Bereich links neben den einzelnen Absätzen handelt. Wenn der Benutzer in der Auswahl Leiste auf klickt, wird die entsprechende Zeile ausgewählt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

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

[**EM \_ GetRect**](em-getrect.md)
</dt> <dt>

[**EM \_ setrectnp**](em-setrectnp.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

