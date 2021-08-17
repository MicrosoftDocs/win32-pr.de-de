---
title: DROPEFFECT-Konstanten (OleIdl.h)
description: Stellt Informationen zu den Auswirkungen eines Drag & Drop-Vorgangs dar.
ms.assetid: d8e46899-3fbf-4012-8dd3-67fa627526d5
topic_type:
- apiref
api_name:
- DROPEFFECT_NONE
- DROPEFFECT_COPY
- DROPEFFECT_MOVE
- DROPEFFECT_LINK
- DROPEFFECT_SCROLL
api_location:
- OleIdl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05c9a4fa961b0da2e654d4672392104b95e718bbb176167c7bb715c39f25cfc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736952"
---
# <a name="dropeffect-constants"></a>DROPEFFECT-Konstanten

Stellt Informationen zu den Auswirkungen eines Drag & Drop-Vorgangs dar. Die [**DoDragDrop-Funktion**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) und viele der Methoden in [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) und [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) verwenden die Werte dieser Enumeration.



| Konstante/Wert                                                                                                                                                                                                                            | Beschreibung                                                                                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DROPEFFECT_NONE"></span><span id="dropeffect_none"></span><dl> <dt>**DROPEFFECT \_ NONE**</dt> <dt>0</dt> </dl>                | Das Ablageziel kann die Daten nicht akzeptieren.<br/>                                                                                      |
| <span id="DROPEFFECT_COPY"></span><span id="dropeffect_copy"></span><dl> <dt>**DROPEFFECT \_ COPY**</dt> <dt>1</dt> </dl>                | Löschen von Ergebnissen in einer Kopie. Die ursprünglichen Daten bleiben von der Ziehquelle unverändert.<br/>                                               |
| <span id="DROPEFFECT_MOVE"></span><span id="dropeffect_move"></span><dl> <dt>**DROPEFFECT \_ MOVE**</dt> <dt>2</dt> </dl>                | Die Quelle mit Ziehen sollte die Daten entfernen. <br/>                                                                                     |
| <span id="DROPEFFECT_LINK"></span><span id="dropeffect_link"></span><dl> <dt>**DROPEFFECT \_ LINK**</dt> <dt>4</dt> </dl>                | Quelle ziehen sollte einen Link zu den ursprünglichen Daten erstellen.<br/>                                                                   |
| <span id="DROPEFFECT_SCROLL"></span><span id="dropeffect_scroll"></span><dl> <dt>**DROPEFFECT \_ SCROLLen**</dt> <dt>0x80000000</dt> </dl> | Das Scrollen wird gestartet oder findet gerade im Ziel statt. Dieser Wert wird zusätzlich zu den anderen Werten verwendet.<br/> |



## <a name="remarks"></a>Hinweise

Ihre Anwendung sollte immer Werte aus der **DROPEFFECT-Enumeration** maskieren, um die Kompatibilität mit zukünftigen Implementierungen sicherzustellen. Derzeit haben nur einige der Positionen in einem **DROPEFFECT-Wert** eine Bedeutung. In Zukunft werden weitere Interpretationen für die Bits hinzugefügt. Ziehen Von Quellen und Ablagezielen sollten diese Werte vor dem Vergleich sorgfältig maskiert werden. Sie sollten **dropeffect** nie mit DROPEFFECT COPY vergleichen, indem sie \_ beispielsweise folgende Schritte ausführen:

``` syntax
if (dwDropEffect == DROPEFFECT_COPY)... 
```

Stattdessen sollte die Anwendung immer für die gesuchten Werte maskieren, indem eine der folgenden Verfahren verwendet wird:

``` syntax
if (dwDropEffect & DROPEFFECT_COPY) == DROPEFFECT_COPY)...

if (dwDropEffect & DROPEFFECT_COPY)... 
```

Dies ermöglicht die Definition neuer Ablageeffekte und behält gleichzeitig die Abwärtskompatibilität mit vorhandenem Code bei.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>OleIdl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Dodragdrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)
</dt> <dt>

[**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)
</dt> <dt>

[**Idroptarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)
</dt> </dl>

 

 





