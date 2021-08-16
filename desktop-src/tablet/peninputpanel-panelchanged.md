---
description: Veraltet. Das PenInputPanel wurde durch den Texteingabebereich (TIP) ersetzt. Tritt ein, wenn sich das PenInputPanel-Objekt zwischen Layouts ändert.
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: PenInputPanel.PanelChanged-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41f722609ae71761a2a2a05c743aba7bfd83b7d4ff8689333bf2093d4dc21345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856519"
---
# <a name="peninputpanelpanelchanged-event"></a>PenInputPanel.PanelChanged-Ereignis

Veraltet. Das [**PenInputPanel**](peninputpanel-class.md) wurde durch den [Texteingabebereich (TIP) ersetzt.](text-input-panel-reference.md)

Tritt ein, wenn [**sich das PenInputPanel-Objekt**](peninputpanel-class.md) zwischen Layouts ändert.

## <a name="syntax"></a>Syntax


```C++
HRESULT PanelChanged(
  [in] PanelType NewPanelType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewPanelType* \[ In\]
</dt> <dd>

Der neue Paneltyp, der für die Eingabe innerhalb des [**PenInputPanel-Objekts**](peninputpanel-class.md) verwendet wird, nachdem das **PanelChanged-Ereignis** angezeigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieses Ereignis erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Beim Erstellen eines [**PenInputPanel-Objekts**](peninputpanel-class.md) [**ist Handwriting**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) der **Standardmäßige PanelType.** Wenn Sie den Bereich ändern, indem Sie die [**CurrentPanel-Eigenschaft**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) festlegen, bevor der Stifteingabebereich zum ersten Mal aktiv wird, tritt ein **PanelChanged-Ereignis** auf.

Das **PanelChanged-Ereignis** wird nicht ausgelöst, wenn der Benutzer zwischen Lined- und Boxed-Schreibpads wechselt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Peninputpanel**](peninputpanel-class.md)
</dt> </dl>

 

 
