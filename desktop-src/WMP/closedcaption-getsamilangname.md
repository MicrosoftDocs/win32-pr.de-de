---
title: Closedcaption. getsamilangname-Methode
description: Die getsamilangname-Methode ruft den Namen einer Sprache ab, die von der aktuellen Sami-Datei unterstützt wird.
ms.assetid: 20cf8faf-3a8c-4d7b-9bd1-2366672f0e67
keywords:
- getsamilangname-Methode, Windows Media Player
- getsamilangname-Methode, Windows Media Player, closedcaption-Klasse
- Closedcaption-Klasse, Windows Media Player, getsamilangname-Methode
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd4b481de808ac8814e596cfc038aec38c7f19b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359410"
---
# <a name="closedcaptiongetsamilangname-method"></a>Closedcaption. getsamilangname-Methode

Die **getsamilangname** -Methode ruft den Namen einer Sprache ab, die von der aktuellen Sami-Datei unterstützt wird.

## <a name="syntax"></a>Syntax


```JScript
strRetVal = ClosedCaption.getSAMILangName(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

**Number** (**Long**), der den Index des abzurufenden sprach namens angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge** zurück, die den Namen der Sprache enthält, wie in der Sami-Datei angegeben.

## <a name="remarks"></a>Bemerkungen

Die Sprachen in einer Sami-Datei werden in der in der Datei gezeigten Reihenfolge indiziert, beginnend mit 0 (null).

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

[**Closedcaption. samilang**](closedcaption-samilang.md)
</dt> </dl>

 

 





