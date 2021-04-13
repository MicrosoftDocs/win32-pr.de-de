---
description: Veraltet. Der "tzinputpanel" wurde durch den Text Eingabe Panel (Tip) ersetzt. Tritt auf, wenn sich das Objekt "pinputpanel" zwischen Layouts ändert.
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: "\"Pinputpanel. PanelChanged\"-Ereignis (msink AUT. h)"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6ff0f415e12131221a8dad1c0775a347ef96cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347869"
---
# <a name="peninputpanelpanelchanged-event"></a>"Pinputpanel. PanelChanged"-Ereignis

Veraltet. Der " [**tzinputpanel**](peninputpanel-class.md) " wurde durch den [Text Eingabe Panel (Tip)](text-input-panel-reference.md)ersetzt.

Tritt auf, wenn sich das Objekt " [**pinputpanel**](peninputpanel-class.md) " zwischen Layouts ändert.

## <a name="syntax"></a>Syntax


```C++
HRESULT PanelChanged(
  [in] PanelType NewPanelType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Newpaneltype* \[ in\]
</dt> <dd>

Der neue Panel-Typ, der nach dem Auslösen des **PanelChanged** -Ereignisses für die Eingabe innerhalb des " [**kinputpanel**](peninputpanel-class.md) "-Objekts verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Beim Erstellen eines " [**pinputpanel**](peninputpanel-class.md) "-Objekts ist [**Handschrift**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) der standardmäßige **PanelType**. Wenn Sie den Bereich ändern, indem Sie die [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) -Eigenschaft festlegen, bevor der Stift Eingabebereich zum ersten Mal aktiviert wird, tritt ein **PanelChanged** -Ereignis auf.

Das **PanelChanged** -Ereignis wird nicht ausgelöst, wenn sich der Benutzer zwischen den gepackten und geschachtelten Schreibvorgängen ändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**"Pendel Panel"**](peninputpanel-class.md)
</dt> </dl>

 

 
