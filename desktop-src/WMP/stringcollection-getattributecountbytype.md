---
title: StringCollection.getAttributeCountByType-Methode
description: Die getAttributeCountByType-Methode ruft die Anzahl der Attribute ab, die dem angegebenen StringCollection-Elementindex, attributnamen und der angegebenen Sprache zugeordnet sind.
ms.assetid: 3671b7b7-d6d4-4049-8710-d0f34c740b1e
keywords:
- getAttributeCountByType-Methode Windows Media Player
- getAttributeCountByType-Methode Windows Media Player , StringCollection-Klasse
- StringCollection-Klasse Windows Media Player , getAttributeCountByType-Methode
topic_type:
- apiref
api_name:
- StringCollection.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e10f88a3b8e4847588ff8f7f924333c6649e59c362b3296b54ef8b83368b7af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832427"
---
# <a name="stringcollectiongetattributecountbytype-method"></a>StringCollection.getAttributeCountByType-Methode

Die **getAttributeCountByType-Methode** ruft die Anzahl der Attribute ab, die dem angegebenen **StringCollection-Elementindex,** attributnamen und der angegebenen Sprache zugeordnet sind.

## <a name="syntax"></a>Syntax


```JScript
retVal = StringCollection.getAttributeCountByType(
  index,
  name,
  language
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

**Number** (**long**), die den nullbasierten Index des **StringCollection-Elements** angibt, aus dem das Attribut abzurufen ist.

</dd> <dt>

*name* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Namen des Attributs enthält.

</dd> <dt>

*Language (Sprache)* \[ In\]
</dt> <dd>

**Zeichenfolge,** die die Sprache enthält. Wenn der Wert auf NULL oder die leere Zeichenfolge ("") festgelegt ist, wird die aktuelle Gebietsschemazeichenfolge verwendet. Andernfalls muss der Wert eine gültige RFC 1766-Sprachzeichenfolge wie "en-us" sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**long**) zurück.

## <a name="remarks"></a>Hinweise

Diese Methode wird verwendet, um die Anzahl der Attribute zu bestimmen, die einem bestimmten Attributnamen für ein bestimmtes **StringCollection-Element** entsprechen. Indexnummern können dann an den vierten Parameter der **StringCollection.getItemInfoByType-Methode** übergeben werden.

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**StringCollection-Objekt**](stringcollection-object.md)
</dt> </dl>

 

 





