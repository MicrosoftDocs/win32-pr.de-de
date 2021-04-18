---
title: Dropffect-Konstanten (oleidl. h)
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
ms.openlocfilehash: f2b1888aa028d4e047a9a8ec1f54e2497fa28ce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343481"
---
# <a name="dropeffect-constants"></a>Dropffect-Konstanten

Stellt Informationen zu den Auswirkungen eines Drag & Drop-Vorgangs dar. Die [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) -Funktion und viele der Methoden in [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) und [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) verwenden die Werte dieser Enumeration.



| Konstante/Wert                                                                                                                                                                                                                            | BESCHREIBUNG                                                                                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DROPEFFECT_NONE"></span><span id="dropeffect_none"></span><dl> <dt>**Dropffect \_ Keine**</dt> <dt>0</dt> </dl>                | Das Ablage Ziel kann die Daten nicht akzeptieren.<br/>                                                                                      |
| <span id="DROPEFFECT_COPY"></span><span id="dropeffect_copy"></span><dl> <dt>**Dropffect \_ Kopieren**</dt> Sie <dt>1</dt> </dl>                | Löschen Sie die Ergebnisse in einer Kopie. Die ursprünglichen Daten sind von der Zieh Quelle unberührt.<br/>                                               |
| <span id="DROPEFFECT_MOVE"></span><span id="dropeffect_move"></span><dl> <dt>**Dropffect \_ Verschieben**</dt> von <dt>2</dt> </dl>                | Ziehen Sie die Quelle, um die Daten zu entfernen. <br/>                                                                                     |
| <span id="DROPEFFECT_LINK"></span><span id="dropeffect_link"></span><dl> <dt>**Dropffect \_ Link**</dt> <dt>4</dt> </dl>                | Mit Drag Source sollte ein Link zu den ursprünglichen Daten erstellt werden.<br/>                                                                   |
| <span id="DROPEFFECT_SCROLL"></span><span id="dropeffect_scroll"></span><dl> <dt>**Dropffect \_**</dt>Bildlauf <dt>0x80000000</dt> </dl> | Der Bildlauf wird gerade gestartet oder ist gegenwärtig im Ziel. Dieser Wert wird zusätzlich zu den anderen Werten verwendet.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Anwendung sollte immer Werte aus der **drompffect** -Enumeration maskieren, um die Kompatibilität mit zukünftigen Implementierungen sicherzustellen. Zurzeit haben nur einige der Positionen in einem **dropeer ffect** -Wert Bedeutung. In Zukunft werden weitere Interpretationen für die Bits hinzugefügt. Drag Sources und Drop Targets sollten diese Werte vor dem Vergleich sorgfältig maskieren. Sie sollten einen **dropeer-ect** -Vorgang nicht \_ mit dem folgenden Vorgang vergleichen:

``` syntax
if (dwDropEffect == DROPEFFECT_COPY)... 
```

Stattdessen sollte die Anwendung immer für den Wert oder die Werte maskiert werden, die mit einem der folgenden Verfahren gesucht werden:

``` syntax
if (dwDropEffect & DROPEFFECT_COPY) == DROPEFFECT_COPY)...

if (dwDropEffect & DROPEFFECT_COPY)... 
```

Dies ermöglicht die Definition von neuen Drop-Effekten, wobei die Abwärtskompatibilität mit vorhandenem Code beibehalten wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Oleidl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)
</dt> <dt>

[**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)
</dt> <dt>

[**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)
</dt> </dl>

 

 





