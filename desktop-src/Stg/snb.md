---
title: SNB (objidl. h)
description: Ein String Name Block (SNB) ist ein Zeiger auf ein Array von Zeigern auf Zeichen folgen, die mit einem NULL-Zeiger enden.
ms.assetid: 8428a820-3d8a-41e0-9955-d355440e2ebc
keywords:
- SNB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d6860204d9f232c2ffafa4f1f16a1187fee8de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949650"
---
# <a name="snb"></a>SNB

Ein String Name Block (**SNB**) ist ein Zeiger auf ein Array von Zeigern auf Zeichen folgen, die mit einem **null** -Zeiger enden. Zeichen folgen Namen Blöcke werden von der [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle und von Funktionsaufrufen verwendet, die Speicher Objekte öffnen. Die Zeichen folgen zeigen auf enthaltene Speicher Objekte oder Streams, die in den geöffneten aufrufen ausgeschlossen werden sollen.


```C++
typedef OLESTR** SNB;
```



<dl> <dt>

**SNB**
</dt> <dd>

\[Wire \_ Marshal (wiresnb)\]

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **SNB** sollte durch Zuordnen eines zusammenhängenden Speicherblocks erstellt werden, in dem auf die Zeiger auf Zeichen folgen ein **null** -Zeiger folgt, auf den dann die eigentlichen Zeichen folgen folgen.

Das Marshalling einer **SNB** basiert auf der Annahme, dass die übergebene **SNB** auf diese Weise erstellt wurde. Obwohl es auf andere Weise gespeichert werden kann, hat die auf diese Weise erstellte **SNB** den Vorteil, dass nur ein Belegungs Vorgang und eine Freigabe des Arbeitsspeichers für alle Zeichen folgen erforderlich ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[ Desktop Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Objidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Objidl. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> </dl>

 

 





