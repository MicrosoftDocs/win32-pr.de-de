---
title: Tree-View Steuerelement Zustände (kommstrg. h)
description: In diesem Abschnitt sind die elementstatusflags aufgeführt, mit denen der Zustand eines Elements in einem Strukturansicht-Steuerelement angegeben wird.
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
ms.openlocfilehash: ef4a19306855b7f38d03aa00323b26407f108bfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352929"
---
# <a name="tree-view-control-item-states"></a>Status der Tree-View-Steuerelement Zustände

In diesem Abschnitt sind die elementstatusflags aufgeführt, mit denen der Zustand eines Elements in einem Strukturansicht-Steuerelement angegeben wird.



| Konstante                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVIS_BOLD"></span><span id="tvis_bold"></span><dl> <dt>**Tvis \_ Fett**</dt> </dl>                               | Das Element ist fett formatiert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_CUT"></span><span id="tvis_cut"></span><dl> <dt>**Tvis- \_ Ausschneiden**</dt> </dl>                                  | Das Element wird als Teil eines Ausschneide-und Einfügevorgangs ausgewählt. <br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TVIS_DROPHILITED"></span><span id="tvis_drophilited"></span><dl> <dt>**Tvis wurde \_ beendet.**</dt> </dl>          | Das Element ist als Drag & Drop-Ziel ausgewählt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_EXPANDED"></span><span id="tvis_expanded"></span><dl> <dt>**Tvis \_ erweitert**</dt> </dl>                   | Die Liste der untergeordneten Elemente des Elements wird derzeit erweitert. Das heißt, dass die untergeordneten Elemente sichtbar sind. Dieser Wert gilt nur für übergeordnete Elemente.<br/>                                                                                                                                                                                                                                                                                                                  |
| <span id="TVIS_EXPANDEDONCE"></span><span id="tvis_expandedonce"></span><dl> <dt>**Tvis \_ expandebug**</dt> </dl>       | Die Liste der untergeordneten Elemente des Elements wurde mindestens einmal erweitert. Die TVN-Benachrichtigungs Codes [ \_ itemexpandeing](tvn-itemexpanding.md) und [TVN \_ itemexpanded](tvn-itemexpanded.md) werden nicht für übergeordnete Elemente generiert, für die dieser Status als Reaktion auf eine [**TVM \_**](tvm-expand.md) -Erweiterungs Meldung festgelegt wurde. Durch die Verwendung von "TVE \_ Collapse" und "TVE \_ redusereset" mit der **\_ Erweiterung "TVM** " wird dieser Zustand zurückgesetzt. Dieser Wert gilt nur für übergeordnete Elemente. <br/> |
| <span id="TVIS_EXPANDPARTIAL"></span><span id="tvis_expandpartial"></span><dl> <dt>**Tvis \_ expandpartial**</dt> </dl>    | **Version 4,70**. Ein teilweise erweitertes Struktur Ansichts Element. In diesem Zustand sind einige, jedoch nicht alle untergeordneten Elemente sichtbar, und das Pluszeichen des übergeordneten Elements wird angezeigt. <br/>                                                                                                                                                                                                                                                                              |
| <span id="TVIS_SELECTED"></span><span id="tvis_selected"></span><dl> <dt>**Tvis \_ ausgewählt**</dt> </dl>                   | Das Element ist ausgewählt. Das Aussehen hängt davon ab, ob es den Fokus besitzt. Das Element wird mithilfe der Systemfarben für die Auswahl gezeichnet. <br/>                                                                                                                                                                                                                                                                                                              |
| <span id="TVIS_OVERLAYMASK"></span><span id="tvis_overlaymask"></span><dl> <dt>**Tvis- \_ overlaymask**</dt> </dl>          | Maske für die Bits, die zum Angeben des Überlagerungs Bilds des Elements verwendet werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_STATEIMAGEMASK"></span><span id="tvis_stateimagemask"></span><dl> <dt>**Tvis- \_ Status-magemask**</dt> </dl> | Maske für die Bits, die verwendet werden, um den Status Bild Index des Elements anzugeben.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_USERMASK"></span><span id="tvis_usermask"></span><dl> <dt>**Tvis- \_ USERMASK**</dt> </dl>                   | Identisch mit **Tvis- \_ Status-magemask**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="remarks"></a>Bemerkungen

Wenn Sie den Überlagerungs Bild Index oder den Status Bild Index eines Elements festlegen oder abrufen, müssen Sie die folgenden Masken im **statemask** -Member der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur angeben:

-   **Tvis- \_ overlaymask**
-   **Tvis- \_ Status-magemask**
-   **Tvis- \_ USERMASK**

Diese Werte können auch zum Maskieren der Zustands Bits verwendet werden, die nicht von Interesse sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





