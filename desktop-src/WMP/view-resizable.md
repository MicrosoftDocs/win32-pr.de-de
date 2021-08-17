---
title: VIEW.resizable
description: Das Größenänderungsattribut ruft einen Wert ab, der angibt, ob die GRÖßE der VIEW geändert werden kann.
ms.assetid: 4f0e4f31-cf16-498f-823f-da43566043b1
keywords:
- VIEW.resizable Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.resizable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 622c732ce6a1218fa16bbe70c1ef18d53ba4211abfde9d39fc794ec862348033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332908"
---
# <a name="viewresizable"></a>VIEW.resizable

Das Größenänderungsattribut ruft einen Wert ab, der angibt, ob die GRÖßE der **VIEW** geändert werden kann. 

``` syntax
        elementID.resizable
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **schreibgeschützter boolescher** Wert mit einem Standardwert, der dem **Titlebar-Attribut** entspricht.



| Werte | BESCHREIBUNG             |
|--------|-------------------------|
| true   | Die Größe der Ansicht kann geändert werden.    |
| false  | Die Größe der Ansicht kann nicht geändert werden. |



 

## <a name="remarks"></a>Hinweise

Wenn keine **Titelleiste** und daher kein Fenster oder Rahmen vorhanden ist, müssen Sie die **Size-Methode** verwenden, um die Größe des **VIEW-Elements** zu ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**VIEW-Element**](view-element.md)
</dt> </dl>

 

 





