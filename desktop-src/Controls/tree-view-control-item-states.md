---
title: Tree-View Steuerelementelementzustände (CommCtrl.h)
description: In diesem Abschnitt werden die Elementzustandsflags aufgeführt, die verwendet werden, um den Zustand eines Elements in einem Strukturansicht-Steuerelement anzugeben.
ms.assetid: 5b11d575-6dfd-47a8-b959-b19aaeeca70e
topic_type:
- apiref
api_name:
- TVIS_BOLD
- TVIS_CUT
- TVIS_DROPHILITED
- TVIS_EXPANDED
- TVIS_EXPANDEDONCE
- TVIS_EXPANDPARTIAL
- TVIS_SELECTED
- TVIS_OVERLAYMASK
- TVIS_STATEIMAGEMASK
- TVIS_USERMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5adb0371e3796c5d512ff3582a5c65850dc6cf8261f138934d46640aa57bf28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045960"
---
# <a name="tree-view-control-item-states"></a>Tree-View Steuerelementelementzustände

In diesem Abschnitt werden die Elementzustandsflags aufgeführt, die verwendet werden, um den Zustand eines Elements in einem Strukturansicht-Steuerelement anzugeben.



| Konstante                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVIS_BOLD"></span><span id="tvis_bold"></span><dl> <dt>**TVIS \_ BOLD**</dt> </dl>                               | Das Element ist fett formatiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_CUT"></span><span id="tvis_cut"></span><dl> <dt>**TVIS \_ CUT**</dt> </dl>                                  | Das Element wird im Rahmen eines Ausschneide- und Einfügevorgang ausgewählt. <br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TVIS_DROPHILITED"></span><span id="tvis_drophilited"></span><dl> <dt>**TVIS \_ DROPHILITED**</dt> </dl>          | Das Element wird als Drag & Drop-Ziel ausgewählt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_EXPANDED"></span><span id="tvis_expanded"></span><dl> <dt>**TVIS \_ EXPANDED**</dt> </dl>                   | Die Liste der untergeordneten Elemente des Elements wird derzeit erweitert. Das heißt, die untergeordneten Elemente sind sichtbar. Dieser Wert gilt nur für übergeordnete Elemente.<br/>                                                                                                                                                                                                                                                                                                                  |
| <span id="TVIS_EXPANDEDONCE"></span><span id="tvis_expandedonce"></span><dl> <dt>**TVIS \_ EXPANDEDONCE**</dt> </dl>       | Die Liste der untergeordneten Elemente des Elements wurde mindestens einmal erweitert. Die [Benachrichtigungscodes TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) und [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) werden nicht für übergeordnete Elemente generiert, deren Status als Reaktion auf eine [**TVM \_ EXPAND-Meldung festgelegt**](tvm-expand.md) ist. Wenn Sie TVE \_ COLLAPSE und TVE \_ COLLAPSERESET mit **TVM EXPAND \_ verwenden,** wird dieser Zustand zurückgesetzt. Dieser Wert gilt nur für übergeordnete Elemente. <br/> |
| <span id="TVIS_EXPANDPARTIAL"></span><span id="tvis_expandpartial"></span><dl> <dt>**TVIS \_ EXPANDPARTIAL**</dt> </dl>    | **Version 4.70**. Ein teilweise erweitertes Strukturansichtselement. In diesem Zustand sind einige, aber nicht alle untergeordneten Elemente sichtbar, und das Pluszeichen des übergeordneten Elements wird angezeigt. <br/>                                                                                                                                                                                                                                                                              |
| <span id="TVIS_SELECTED"></span><span id="tvis_selected"></span><dl> <dt>**TVIS \_ AUSGEWÄHLT**</dt> </dl>                   | Das Element ist ausgewählt. Die Darstellung hängt davon ab, ob sie den Fokus besitzt. Das Element wird mithilfe der Systemfarben für die Auswahl gezeichnet. <br/>                                                                                                                                                                                                                                                                                                              |
| <span id="TVIS_OVERLAYMASK"></span><span id="tvis_overlaymask"></span><dl> <dt>**TVIS \_ OVERLAYMASK**</dt> </dl>          | Maskieren Sie die Bits, die zum Angeben des Überlagerungsbildindexes des Elements verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_STATEIMAGEMASK"></span><span id="tvis_stateimagemask"></span><dl> <dt>**TVIS \_ STATEIMAGEMASK**</dt> </dl> | Maskieren Sie die Bits, die zum Angeben des Statusbildindexes des Elements verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_USERMASK"></span><span id="tvis_usermask"></span><dl> <dt>**TVIS \_ USERMASK**</dt> </dl>                   | Identisch mit **TVIS \_ STATEIMAGEMASK**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="remarks"></a>Hinweise

Wenn Sie den Überlagerungsbildindex oder den Statusbildindex eines Elements festlegen oder abrufen, müssen Sie die folgenden Masken im **stateMask-Element** der [**TVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tvitema) angeben:

-   **TVIS \_ OVERLAYMASK**
-   **TVIS \_ STATEIMAGEMASK**
-   **TVIS \_ USERMASK**

Diese Werte können auch verwendet werden, um die Zustandsbits zu maskieren, die nicht von Interesse sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





