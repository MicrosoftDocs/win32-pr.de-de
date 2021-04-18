---
title: WM_COMPAREITEM Meldung (Winuser. h)
description: Wird gesendet, um die relative Position eines neuen Elements in der sortierten Liste eines von einem Besitzer gezeichneten Kombinations Felds oder Listen Felds zu bestimmen.
ms.assetid: 22882730-9fd6-4b45-a563-d7b00ed26564
keywords:
- Windows-Steuerelemente für WM_COMPAREITEM Meldung
topic_type:
- apiref
api_name:
- WM_COMPAREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f269b90f00e69cce2fb84e6b4efa76e554ad96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475114"
---
# <a name="wm_compareitem-message"></a>WM- \_ compareitem-Meldung

Wird gesendet, um die relative Position eines neuen Elements in der sortierten Liste eines von einem Besitzer gezeichneten Kombinations Felds oder Listen Felds zu bestimmen. Jedes Mal, wenn die Anwendung ein neues Element hinzufügt, sendet das System diese Nachricht an den Besitzer eines Kombinations Felds oder eines Listen Felds, das mit der [**CBS- \_ Sortierung**](combo-box-styles.md) oder dem [**lbs- \_ Sortier**](list-box-styles.md) Stil erstellt wurde.


```C++
WM_COMPAREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Bezeichner des Steuer Elements an, das die **WM \_ compareitem** -Nachricht gesendet hat.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**compareitemstruct**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) -Struktur, die die Bezeichner und die von der Anwendung bereitgestellten Daten für zwei Elemente im Kombinations-oder Listenfeld enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert gibt die relative Position der beiden Elemente an. Dies kann ein beliebiger Wert sein, der in der folgenden Tabelle aufgeführt ist.



| Rückgabecode                                                                          | Beschreibung                                                  |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**Wert**</dt> </dl> | Bedeutung<br/>                                           |
| <dl> <dt>**-1**</dt> </dl>    | Element 1 ist Element 2 in der sortierten Reihenfolge voraus.<br/>       |
| <dl> <dt>**0**</dt> </dl>     | Die Elemente 1 und 2 sind äquivalent in der sortierten Reihenfolge.<br/> |
| <dl> <dt>**1**</dt> </dl>     | Element 1 folgt Element 2 in der sortierten Reihenfolge.<br/>        |



 

## <a name="remarks"></a>Bemerkungen

Wenn der Besitzer eines von einem Besitzer gezeichneten Kombinations Felds oder Listen Felds diese Nachricht empfängt, gibt der Besitzer einen Wert zurück, der angibt, welche der durch die [**compareitemstruct**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) -Struktur angegebenen Elemente vor dem anderen angezeigt werden. Normalerweise sendet das System diese Nachricht mehrmals, bis die genaue Position für das neue Element bestimmt wird.

Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in einen **booleschen** Wert umwandeln und den Wert direkt zurückgeben. Der \_ von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte DWL-msgresult-Wert wird ignoriert.

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

[**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> </dl>

 

