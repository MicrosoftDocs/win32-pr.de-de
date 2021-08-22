---
title: WM_COMPAREITEM (Winuser.h)
description: Wird gesendet, um die relative Position eines neuen Elements in der sortierten Liste eines vom Besitzer gezeichneten Kombinationsfelds oder Listenfelds zu bestimmen.
ms.assetid: 22882730-9fd6-4b45-a563-d7b00ed26564
keywords:
- WM_COMPAREITEM von Windows-Steuerelementen
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
ms.openlocfilehash: 819df3c4dd36c784ef5747d4aa4cdf688b3a48dbd052254192a7c98574bbfa94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655770"
---
# <a name="wm_compareitem-message"></a>WM \_ COMPAREITEM-Meldung

Wird gesendet, um die relative Position eines neuen Elements in der sortierten Liste eines vom Besitzer gezeichneten Kombinationsfelds oder Listenfelds zu bestimmen. Jedes Mal, wenn die Anwendung ein neues Element hinzufügt, sendet das System diese Nachricht an den Besitzer eines Kombinationsfelds oder Listenfelds, das mit dem [**CBS \_ SORT-**](combo-box-styles.md) oder [**LBS \_ SORT-Format erstellt**](list-box-styles.md) wurde.


```C++
WM_COMPAREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Bezeichner des Steuerelements an, das die **WM \_ COMPAREITEM-Nachricht gesendet** hat.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**COMPAREITEMSTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) die die Bezeichner und von der Anwendung bereitgestellten Daten für zwei Elemente im Kombinations- oder Listenfeld enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert gibt die relative Position der beiden Elemente an. Dies kann einer der in der folgenden Tabelle gezeigten Werte sein.



| Rückgabecode                                                                          | Beschreibung                                                  |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**Wert**</dt> </dl> | Bedeutung<br/>                                           |
| <dl> <dt>**-1**</dt> </dl>    | Element 1 ist in der sortierten Reihenfolge vor Element 2.<br/>       |
| <dl> <dt>**0**</dt> </dl>     | Die Elemente 1 und 2 sind in der sortierten Reihenfolge äquivalent.<br/> |
| <dl> <dt>**1**</dt> </dl>     | Element 1 folgt in der sortierten Reihenfolge auf Element 2.<br/>        |



 

## <a name="remarks"></a>Hinweise

Wenn der Besitzer eines vom Besitzer gezeichneten Kombinationsfelds oder Listenfelds diese Meldung empfängt, gibt der Besitzer einen Wert zurück, der angibt, welches der von der [**COMPAREITEMSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-compareitemstruct) angegebenen Elemente vor dem anderen angezeigt wird. In der Regel sendet das System diese Nachricht mehrmals, bis es die genaue Position für das neue Element bestimmt.

Wenn eine Dialogfeldprozedur diese Meldung verarbeitet, sollte sie den gewünschten Rückgabewert in einen **BOOL-Wert** umkehren und den Wert direkt zurückgeben. Der von der \_ [**SetWindowLong-Funktion festgelegte**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) MSGRESULT-DWL-Wert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**COMPAREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-compareitemstruct)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> </dl>

 

