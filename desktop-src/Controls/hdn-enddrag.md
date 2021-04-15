---
title: HDN_ENDDRAG Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Header-Steuerelement gesendet, wenn ein Zieh Vorgang auf einem seiner Elemente beendet wurde. Dieser Benachrichtigungs Code wird als WM-Benachrichtigungs \_ Meldung gesendet. Nur Header Steuerelemente, die auf den HDS DragDrop-Stil festgelegt sind, \_ senden diesen Benachrichtigungs Code.
ms.assetid: a28df985-73f1-4fc7-a1db-81a86a131c06
keywords:
- Windows-Steuerelemente für HDN_ENDDRAG Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eef628dd8ff748829542ace76642e20ad97786f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479455"
---
# <a name="hdn_enddrag-notification-code"></a>Hdn- \_ EndDrag-Benachrichtigungs Code

Wird von einem Header-Steuerelement gesendet, wenn ein Zieh Vorgang auf einem seiner Elemente beendet wurde. Dieser Benachrichtigungs Code wird als [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. Nur Header Steuerelemente, die auf den [**HDS \_ DragDrop**](header-control-styles.md) -Stil festgelegt sind, senden diesen Benachrichtigungs Code.


```C++
HDN_ENDDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die Informationen über das Header Element enthält, das gezogen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Damit das Steuerelement das Element automatisch platzieren und neu anordnen kann, wird **false** zurückgegeben. Um zu verhindern, dass das Element platziert wird, wird **true** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn der Besitzer eine externe (manuelle) Drag & Drop-Verwaltung durchführt, muss er **false** zurückgeben. Der Besitzer muss dann die Header Elemente manuell neu anordnen, indem er [**HDM \_**](hdm-setitem.md) -Server oder [**HDM-Server \_ Array**](hdm-setorderarray.md)sendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





