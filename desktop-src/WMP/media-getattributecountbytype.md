---
title: Media.getAttributeCountByType-Methode
description: Die getAttributeCountByType-Methode ruft die Anzahl der Attribute ab, die dem angegebenen Attributnamen und der angegebenen Sprache zugeordnet sind.
ms.assetid: 5644e823-a9b1-4b02-9dd6-015e524fde64
keywords:
- getAttributeCountByType-Methode Windows Media Player
- getAttributeCountByType-Methode Windows Media Player , Media-Klasse
- Medienklasse Windows Media Player , getAttributeCountByType-Methode
topic_type:
- apiref
api_name:
- Media.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 222f92a57ba9fbcd9971a5536be5f31078e2e09373fb1d168a7074911b027d79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123449"
---
# <a name="mediagetattributecountbytype-method"></a>Media.getAttributeCountByType-Methode

Die **getAttributeCountByType-Methode** ruft die Anzahl der Attribute ab, die dem angegebenen Attributnamen und der angegebenen Sprache zugeordnet sind.

## <a name="syntax"></a>Syntax


```JScript
retVal = Media.getAttributeCountByType(
  name,
  language
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*name* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Namen des Attributs enthält. Informationen zu den attributen, die von Windows Media Player unterstützt werden, finden Sie unter Windows Media Player [Attributverweis.](attribute-reference.md)

</dd> <dt>

*Language (Sprache)* \[ In\]
</dt> <dd>

**Zeichenfolge,** die die Sprache darstellt. Wenn der Wert auf NULL oder "" (leere Zeichenfolge) festgelegt ist, wird die aktuelle Gebietsschemazeichenfolge verwendet. Andernfalls muss der Wert eine gültige RFC 1766-Sprachzeichenfolge wie "en-us" sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zahl** (**long**) zurück, die die Attributanzahl enthält.

## <a name="remarks"></a>Hinweise

Diese Methode wird verwendet, um die Anzahl der Attribute zu bestimmen, die einem bestimmten Attributnamen für ein bestimmtes **Media-Objekt** entsprechen. Indexnummern können dann an die **getItemInfoByType-Methode** übergeben werden. Dies ist z. B. nützlich, wenn ein Medienelement unter mehreren Medienobjekten kategorisiert wurde.

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer 0 zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player serie 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MediaObject**](media-object.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





