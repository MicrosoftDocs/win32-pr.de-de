---
title: Closedcaption. getsamistylename-Methode
description: Die getsamistylename-Methode ruft den Namen eines Stils ab, der von der aktuellen Sami-Datei unterstützt wird.
ms.assetid: c2ffedf8-4622-44fe-9d92-b52ed3bf3b9a
keywords:
- getsamistylename-Methode, Windows Media Player
- getsamistylename-Methode, Windows Media Player, closedcaption-Klasse
- Closedcaption-Klasse, Windows Media Player, getsamistylename-Methode
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMIStyleName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96480e28e0341b822aaf6726e63a6038681a577f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359311"
---
# <a name="closedcaptiongetsamistylename-method"></a>Closedcaption. getsamistylename-Methode

Die **getsamistylename** -Methode ruft den Namen eines Stils ab, der von der aktuellen Sami-Datei unterstützt wird.

## <a name="syntax"></a>Syntax


```JScript
strRetVal = ClosedCaption.getSAMIStyleName(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

**Zahl** (**Long**), die den Index des abzurufenden Format namens angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge** zurück, die den Namen des Stils enthält, wie in der Sami-Datei angegeben.

## <a name="remarks"></a>Bemerkungen

Die Stile in einer Sami-Datei werden in der in der Datei gezeigten Reihenfolge indiziert, beginnend mit 0 (null).

Diese Methode kann erst verwendet werden, wenn eine digitale Mediendatei (*Player*) geöffnet ist.**openstate** ist gleich 13).

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Closedcaption-Objekt**](closedcaption-object.md)
</dt> <dt>

[**Closedcaption. samistyle**](closedcaption-samistyle.md)
</dt> </dl>

 

 





