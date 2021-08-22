---
title: VIEW.size
description: Mit der Size-Methode wird die Größe der VIEW-Ansicht an einem angegebenen Rand geändert.
ms.assetid: c15a33b2-3618-41a7-bff1-9d48a566ed4f
keywords:
- VIEW.size Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.size
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0d9bd583b280f39bee38f0e109e6bb2bba6ce08ec0e7cea4c082b4a6db55739
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119615310"
---
# <a name="viewsize"></a>VIEW.size

Mit der **Size-Methode** wird die Größe der **VIEW-Ansicht** an einem angegebenen Rand geändert.

``` syntax
        elementID.size(handle)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="handle"></span><span id="HANDLE"></span>*Behandeln*
</dt> <dd>

Zeichenfolge, die den Rand oder die Ecke angibt, die beim Dimensionieren verschoben werden soll. Diese Zeichenfolge muss einen der folgenden acht Werte aufweisen.



| Edge   | Ecke      |
|--------|-------------|
| top    | Topright    |
| Rechts  | unten rechts |
| bottom | Bottomleft  |
| Linker Join   | Topleft     |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode wird in der Regel innerhalb eines **onmousedown-Handlers** aufgerufen. Sie übernimmt die Größenänderung, während die Maus gezogen wird, und beendet die Größenänderung, wenn die Maustaste losgelassen wird. Wenn die Größe der **VIEW-Ansicht** eingeschränkt ist, können Sie die Größe der **Ansicht** nicht mit der Maus über die eingeschränkten Grenzen hinaus ändern.

## <a name="examples"></a>Beispiele


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="sizer" horizontalAlignment="right" 
        verticalAlignment="bottom" image="Open.png" 
        onmousedown="jscript:View1.size('bottomright')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**VIEW-Element**](view-element.md)
</dt> </dl>

 

 





