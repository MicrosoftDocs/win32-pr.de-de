---
title: View. Size
description: Die size-Methode ändert die Ansicht an einem angegebenen Rand.
ms.assetid: c15a33b2-3618-41a7-bff1-9d48a566ed4f
keywords:
- Ansicht. Größen Fenster Media Player
topic_type:
- apiref
api_name:
- VIEW.size
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: def9b416dfe5eda052ef430b587fa1c6017b4e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369450"
---
# <a name="viewsize"></a>View. Size

Die **size** -Methode ändert die **Ansicht** an einem angegebenen Rand.

``` syntax
        elementID.size(handle)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="handle"></span><span id="HANDLE"></span>*bewältigen*
</dt> <dd>

Eine Zeichenfolge, die den zu Verschieb nden Rand oder die Ecke angibt Diese Zeichenfolge muss einen der folgenden acht Werte aufweisen.



| Edge   | Ecke      |
|--------|-------------|
| top    | oberen rechten    |
| Rechts  | BottomRight |
| bottom | BottomLeft  |
| Linker Join   | TopLeft     |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird in der Regel innerhalb eines **onmouondown** -Handlers aufgerufen. Sie kümmert sich um die Größe der Größe, während der Mauszeiger gezogen wird, und beendet die Größe, wenn die Maustaste losgelassen wird. Wenn die Größe der **Ansicht** eingeschränkt ist, können Sie die Maus nicht ziehen, um die Größe der **Ansicht** über die eingeschränkten Begrenzungen hinaus zu ändern.

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
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**View-Element**](view-element.md)
</dt> </dl>

 

 





