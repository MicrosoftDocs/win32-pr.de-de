---
title: View. returntomediacenter
description: Die returntomediacenter-Methode gibt den Benutzer in den vollständigen Modus von Windows Media Player zurück.
ms.assetid: eebf0679-5704-498c-8eb3-f7710e0cb1fe
keywords:
- Ansicht. returntomediacenter Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.returnToMediaCenter
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c5f0c86bdd15140ba92261d1f5e8c510d77afc7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370162"
---
# <a name="viewreturntomediacenter"></a>View. returntomediacenter

Die **returntomediacenter** -Methode gibt den Benutzer in den vollständigen Modus von Windows Media Player zurück.

``` syntax
        elementID.returnToMediaCenter()
```

## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="examples"></a>Beispiele


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="Open" image="Open.png" 
        onclick="jscript:View1.returnToMediaCenter()">
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

 

 





