---
title: DASS (Objidl.h)
description: Ein Zeichenfolgennamenblock (STRING Name Block, DOMÄNENNAMEN) ist ein Zeiger auf ein Array von Zeigern auf Zeichenfolgen, das mit einem NULL-Zeiger endet.
ms.assetid: 8428a820-3d8a-41e0-9955-d355440e2ebc
keywords:
- Snb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e49a7868912b9d7d1e3d9f3b1f82805e6e285d815eacbc559c887febd23e9e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682780"
---
# <a name="snb"></a>Snb

Ein Zeichenfolgennamenblock **(CSV)** ist ein Zeiger auf ein Array von Zeigern auf Zeichenfolgen, das mit einem **NULL-Zeiger** endet. Zeichenfolgennamenblöcke werden von der [**IStorage-Schnittstelle**](/windows/desktop/api/Objidl/nn-objidl-istorage) und von Funktionsaufrufen verwendet, die Speicherobjekte öffnen. Die Zeichenfolgen zeigen auf enthaltene Speicherobjekte oder Streams, die in den geöffneten Aufrufen ausgeschlossen werden sollen.


```C++
typedef OLESTR** SNB;
```



<dl> <dt>

**Snb**
</dt> <dd>

\[wire \_ marshal(wireSNB)\]

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **-DATEI** sollte erstellt werden, indem ein zusammenhängender Speicherblock zugewiesen wird, in dem auf die Zeiger auf Zeichenfolgen ein **NULL-Zeiger** folgt, auf den dann die tatsächlichen Zeichenfolgen folgen.

Das Marshalling eines **ERFOLGTEN** basiert auf der Annahme, dass der übergebene **MSI** auf diese Weise erstellt wurde. Obwohl es auf andere Weise gespeichert werden kann, hat das auf diese Weise erstellte **WIEDERUME** den Vorteil, dass nur ein Zuordnungsvorgang und ein speicherfreier Vorgang für alle Zeichenfolgen erforderlich ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Objidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Objidl.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Istorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> </dl>

 

 





