---
description: Veraltet. Das PenInputPanel wurde durch den Texteingabebereich (TIP) ersetzt. Tritt ein, wenn sich der Eingabefokus ändert, bevor das PenInputPanel-Objekt Benutzereingaben in das angefügte Steuerelement einfügen konnte.
ms.assetid: a5928f78-29d6-40e8-8f87-17c188e51ba9
title: PenInputPanel.InputFailed-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cc3234c73fc8ba47faa7d1f2ec89477a1bfb86b7c2abda263aff227c5961f1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934760"
---
# <a name="peninputpanelinputfailed-event"></a>PenInputPanel.InputFailed-Ereignis

Veraltet. Das [**PenInputPanel**](peninputpanel-class.md) wurde durch den [Texteingabebereich (TIP) ersetzt.](text-input-panel-reference.md)

Tritt ein, wenn sich der Eingabefokus ändert, bevor das [**PenInputPanel-Objekt**](peninputpanel-class.md) Benutzereingaben in das angefügte Steuerelement einfügen konnte.

## <a name="syntax"></a>Syntax


```C++
HRESULT InputFailed(
  [in] long  hWnd,
  [in] long  Key,
  [in] BSTR  Text,
  [in] short ShiftKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hWnd* \[ In\]
</dt> <dd>

Das Fensterhand handle des Steuerelements, das das [**PenInputPanel-Objekt aufgerufen**](peninputpanel-class.md) hat.

</dd> <dt>

*Schlüssel* \[ In\]
</dt> <dd>

Die virtuelle Taste, die der gedrückten Taste entspricht.

</dd> <dt>

*Text* \[ In\]
</dt> <dd>

Die Zeichenfolge, die in das Steuerelement eingefügt werden sollte, das durch den *hWnd-Parameter* dargestellt wurde, als das **InputFailed-Ereignis** ausgelöst wurde.

Weitere Informationen zum BSTR-Datentyp finden Sie unter [Verwenden der COM-Bibliothek](using-the-com-library.md).

</dd> <dt>

*UMSCHALTTASTETASTE* \[ In\]
</dt> <dd>

Der Zustand der Tastaturmodifizierer, einschließlich UMSCHALT, CAPS, STRG und ALT.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieses Ereignis erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Das **InputFailed-Ereignis** tritt auf, wenn sich der Eingabefokus ändert, bevor die Benutzereingabe in das angefügte Steuerelement eingefügt wurde. Wenn der Benutzer beispielsweise Ink in das Schreibpad ein gibt und dann auf ein anderes Bearbeitungssteuer steuerelement tippt, bevor die Suche abgeschlossen werden konnte, wird dieses Ereignis angezeigt.

Mithilfe des an dieses Ereignis übergebenen Fensterhandpunkts können Sie den Text selbst einfügen, wenn dieses Ereignis eintritt.

> [!Note]  
> Ab Microsoft Windows XP Tablet PC Edition 2005 gilt **das InputFailed-Ereignis** nicht mehr. Text wird immer eingefügt, bevor sich der Fokus ändert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Peninputpanel**](peninputpanel-class.md)
</dt> </dl>

 

 




