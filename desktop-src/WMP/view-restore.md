---
title: Anzeigen. Wiederherstellen
description: Die Restore-Methode stellt die-Sicht wieder her.
ms.assetid: 8005c14e-771b-4f20-8039-fc09869dc726
keywords:
- Anzeigen. Windows Media Player wiederherstellen
topic_type:
- apiref
api_name:
- VIEW.restore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: db92fc5e796acc55fe9c4faf93417d648652415e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367070"
---
# <a name="viewrestore"></a>Anzeigen. Wiederherstellen

Die Restore-Methode stellt die- **Sicht** **wieder her** .

``` syntax
        elementID.restore()
```

## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="examples"></a>Beispiele


```JScript
<THEME>
  <VIEW id="View1">
    <BUTTON id="Open" image="Open.png" 
        onclick="jscript:View1.restore()">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**View-Element**](view-element.md)
</dt> </dl>

 

 





