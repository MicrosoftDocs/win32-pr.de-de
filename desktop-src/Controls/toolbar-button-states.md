---
title: Symbolleisten-Schaltflächen Zustände (kommstrg. h)
description: In diesem Abschnitt sind die Zustände aufgeführt, die eine Symbolleisten-Schaltfläche haben
ms.assetid: 422e0d81-bd80-45dc-b843-82fc5d5c2a9a
topic_type:
- apiref
api_name:
- TBSTATE_CHECKED
- TBSTATE_ELLIPSES
- TBSTATE_ENABLED
- TBSTATE_HIDDEN
- TBSTATE_INDETERMINATE
- TBSTATE_MARKED
- TBSTATE_PRESSED
- TBSTATE_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45262197c4432d9e3bb5c0884b3f76c986e4acfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371096"
---
# <a name="toolbar-button-states"></a>Symbolleisten Schaltflächen

In diesem Abschnitt sind die Zustände aufgeführt, die eine Symbolleisten-Schaltfläche haben



| Konstante                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBSTATE_CHECKED"></span><span id="tbstate_checked"></span><dl> <dt>**TBSTATE \_ aktiviert**</dt> </dl>                   | Die Schaltfläche hat den [**tbstyle- \_ prüfstil**](toolbar-control-and-button-styles.md) , auf den geklickt wird.<br/>                   |
| <span id="TBSTATE_ELLIPSES"></span><span id="tbstate_ellipses"></span><dl> <dt>**TBSTATE- \_ Ellipsen**</dt> </dl>                | [Version 4,70](common-control-versions.md). Der Text der Schaltfläche wird abgeschnitten, und es wird eine Ellipse angezeigt.<br/>                                    |
| <span id="TBSTATE_ENABLED"></span><span id="tbstate_enabled"></span><dl> <dt>**TBSTATE \_ aktiviert**</dt> </dl>                   | Die Schaltfläche akzeptiert Benutzereingaben. Eine Schaltfläche, die nicht über diesen Zustand verfügt, ist abgeblendet.<br/>                                                           |
| <span id="TBSTATE_HIDDEN"></span><span id="tbstate_hidden"></span><dl> <dt>**TBSTATE \_ ausgeblendet**</dt> </dl>                      | Die Schaltfläche ist nicht sichtbar und kann keine Benutzereingaben empfangen.<br/>                                                                                   |
| <span id="TBSTATE_INDETERMINATE"></span><span id="tbstate_indeterminate"></span><dl> <dt>**TBSTATE \_ unbestimmt**</dt> </dl> | Die Schaltfläche ist abgeblendet.<br/>                                                                                                                      |
| <span id="TBSTATE_MARKED"></span><span id="tbstate_marked"></span><dl> <dt>**TBSTATE \_ markiert**</dt> </dl>                      | [Version 4,71](common-control-versions.md). Die Schaltfläche ist gekennzeichnet. Die Interpretation eines markierten Elements hängt von der Anwendung ab. <br/> |
| <span id="TBSTATE_PRESSED"></span><span id="tbstate_pressed"></span><dl> <dt>**TBSTATE \_ gedrückt**</dt> </dl>                   | Auf die Schaltfläche wird geklickt.<br/>                                                                                                               |
| <span id="TBSTATE_WRAP"></span><span id="tbstate_wrap"></span><dl> <dt>**TBSTATE- \_ Wrap**</dt> </dl>                            | Auf die Schaltfläche folgt ein Zeilenumbruch. Für die Schaltfläche muss außerdem der Status "TBSTATE" \_ aktiviert sein.<br/>                                              |



## <a name="remarks"></a>Bemerkungen

Eine Symbolleiste kann eine Kombination aus Zuständen aufweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





