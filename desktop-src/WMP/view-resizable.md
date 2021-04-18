---
title: Ansicht. Größenänderung
description: Das in der Größe änderbare Attribut Ruft einen Wert ab, der angibt, ob die Größe der Sicht geändert werden kann.
ms.assetid: 4f0e4f31-cf16-498f-823f-da43566043b1
keywords:
- Ansicht. Größenänderung in Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.resizable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4d61973e34891d336ea5729ea40478c6c32808
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365371"
---
# <a name="viewresizable"></a>Ansicht. Größenänderung

Das in der **Größe** änderbare Attribut Ruft einen Wert ab, der angibt, ob die Größe der **Sicht** geändert werden kann.

``` syntax
        elementID.resizable
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein Schreib geschützter **boolescher** Wert mit einem Standardwert, der dem **TitleBar** -Attribut entspricht.



| Werte | BESCHREIBUNG             |
|--------|-------------------------|
| true   | Die Größe der Sicht kann geändert werden.    |
| false  | Die Größe der Sicht kann nicht geändert werden. |



 

## <a name="remarks"></a>Bemerkungen

Wenn keine **TitleBar** und somit kein Fenster oder Rahmen vorhanden ist, müssen Sie die size-Methode verwenden, um die **Größe** des **Ansichts** Elements zu ändern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**View-Element**](view-element.md)
</dt> </dl>

 

 





