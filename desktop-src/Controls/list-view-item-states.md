---
title: List-View Elementzustände (CommCtrl.h)
description: Der Zustandswert eines Elements besteht aus dem Zustand des Elements, einem optionalen Index für die Überlagerungsmaske und einem optionalen Index für die Statusbildmaske.
ms.assetid: 21827f4a-f133-489b-bbd2-6979d1928b40
topic_type:
- apiref
api_name:
- LVIS_ACTIVATING
- LVIS_CUT
- LVIS_DROPHILITED
- LVIS_FOCUSED
- LVIS_OVERLAYMASK
- LVIS_SELECTED
- LVIS_STATEIMAGEMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9040272afc16f500806a3d7a90a0b062018d2f4dec8510e4abe57b24cbc75e88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958389"
---
# <a name="list-view-item-states"></a>List-View Elementzustände

Der Zustandswert eines Elements besteht aus dem Zustand des Elements, einem optionalen Index für die Überlagerungsmaske und einem optionalen Index für die Statusbildmaske.

Der Zustand eines Elements bestimmt seine Darstellung und Funktionalität. Der Zustand kann 0 (null) oder mindestens einer der folgenden Werte sein:



| Konstante                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_ACTIVATING"></span><span id="lvis_activating"></span><dl> <dt>**\_LVIS-AKTIVIERUNG**</dt> </dl>             | Derzeit nicht unterstützt.<br/>                                                                                                                                  |
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ CUT**</dt> </dl>                                  | Das Element ist für einen Ausschneide- und Einfügevorgang markiert.<br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | Das Element wird als Drag & Drop-Ziel hervorgehoben.<br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**\_LVIS-FOKUS**</dt> </dl>                      | Das Element hat den Fokus, sodass es von einem Standardfokusrechteck umgeben ist. Obwohl mehr als ein Element ausgewählt werden kann, kann nur ein Element den Fokus haben.<br/> |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**LVIS \_ OVERLAYMASK**</dt> </dl>          | Der Überlagerungsbildindex des Elements wird durch eine Maske abgerufen.<br/>                                                                                                    |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ SELECTED**</dt> </dl>                   | Das Element ist ausgewählt. Die Darstellung eines ausgewählten Elements hängt davon ab, ob es den Fokus besitzt, und auch von den Systemfarben, die für die Auswahl verwendet werden.<br/>             |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | Der Statusbildindex des Elements wird durch eine Maske abgerufen.<br/>                                                                                                      |



## <a name="remarks"></a>Hinweise

Sie können die **LVIS \_ OVERLAYMASK-Maske verwenden,** um den 1-basierten Index des Überlagerungsbilds zu isolieren. Sie können die **LVIS \_ STATEIMAGEMASK-Maske** verwenden, um den einbasierten Index des Statusbilds zu isolieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





