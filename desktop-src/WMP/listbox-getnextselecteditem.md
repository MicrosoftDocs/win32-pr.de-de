---
title: LISTBOX.getNextSelectedItem
description: Die getNextSelectedItem-Methode ruft das nächste ausgewählte Element im Listenfeld-Steuerelement ab, beginnend am Element nach dem Element mit dem angegebenen Index.
ms.assetid: 060d196d-2b14-4386-ba01-34256c137db5
keywords:
- LISTBOX.getNextSelectedItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f4a5d95880b1300ebfb7f1732e7c20b6975ad82cf2d15514c58e68b9f9c42cc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003400"
---
# <a name="listboxgetnextselecteditem"></a>LISTBOX.getNextSelectedItem

Die **getNextSelectedItem-Methode** ruft das nächste ausgewählte Element im Listenfeld-Steuerelement ab, beginnend am Element nach dem Element mit dem angegebenen Index.

``` syntax
        elementID.getNextSelectedItem(startIndex)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*Startindex*
</dt> <dd>

**Zahl** (**long**), die den Index des Elements enthält, das dem abzurufenden Element vorausgeht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**long**) zurück, die den Index des nächsten ausgewählten Elements enthält.

## <a name="remarks"></a>Hinweise

Um die Suche von Anfang an zu starten, verwenden Sie 1 für den Startindex.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------|
| Version<br/> | Windows Media Player für Windows XP oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LISTBOX-Element**](listbox-element.md)
</dt> </dl>

 

 





