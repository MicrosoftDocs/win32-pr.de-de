---
title: List-View Element Zustände (kommstrg. h)
description: Der Zustandswert eines Elements besteht aus dem Zustand des Elements, einem optionalen Überlagerungs Masken Index und einem optionalen Status Bildmasken Index.
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
ms.openlocfilehash: 8432760dd4cc7efde30700f837864ddcf04aac31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351314"
---
# <a name="list-view-item-states"></a>List-View Element Zustände

Der Zustandswert eines Elements besteht aus dem Zustand des Elements, einem optionalen Überlagerungs Masken Index und einem optionalen Status Bildmasken Index.

Der Zustand eines Elements bestimmt seine Darstellung und Funktionalität. Der Status kann NULL oder mindestens einen der folgenden Werte aufweisen:



| Konstante                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_ACTIVATING"></span><span id="lvis_activating"></span><dl> <dt>**Aktivieren von LVIS \_**</dt> </dl>             | Wird derzeit nicht unterstützt.<br/>                                                                                                                                  |
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS- \_ Ausschneiden**</dt> </dl>                                  | Das Element ist für einen Ausschneide-und Einfügevorgang gekennzeichnet.<br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS wurde \_ beendet.**</dt> </dl>          | Das Element wird als Drag & Drop-Ziel hervorgehoben.<br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS \_ fokussiert**</dt> </dl>                      | Das Element besitzt den Fokus, sodass es von einem Standard Fokus Rechteck umgeben ist. Obwohl mehr als ein Element ausgewählt werden kann, kann nur ein Element den Fokus haben.<br/> |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**LVIS \_ overlaymask**</dt> </dl>          | Der Index des Überlagerungs Bilds des Elements wird von einer Maske abgerufen.<br/>                                                                                                    |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ ausgewählt**</dt> </dl>                   | Das Element ist ausgewählt. Die Darstellung eines ausgewählten Elements hängt davon ab, ob es den Fokus und die für die Auswahl verwendeten Systemfarben besitzt.<br/>             |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS- \_ Status-magemask**</dt> </dl> | Der Status Bild Index des Elements wird von einer Maske abgerufen.<br/>                                                                                                      |



## <a name="remarks"></a>Bemerkungen

Sie können die **LVIS \_ overlaymask** -Maske verwenden, um den 1-basierten Index des Überlagerungs Bilds zu isolieren. Sie können den 1-basierten Index des Zustands Bilds mithilfe der **LVIS- \_ stateimagemask** -Maske isolieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





