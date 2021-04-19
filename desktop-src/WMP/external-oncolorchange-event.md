---
title: Externes. oncolorchange-Ereignis
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Externes. oncolorchange-Ereignis
ms.assetid: f2cd44b1-c813-479b-b847-96ddb9572697
keywords:
- Externe. oncolorchange-Ereignisfenster Media Player
topic_type:
- apiref
api_name:
- External.OnColorChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029c8bb860443ed026737c7413be2bed8862c6d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370126"
---
# <a name="externaloncolorchange-event"></a>Externes. oncolorchange-Ereignis

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das **oncolorchange** -Ereignis tritt auf, wenn sich die Farbe der Windows Media Player-Benutzeroberfläche ändert.

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a>Mögliche Werte

Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die den Namen der Funktion im Skript angibt, die von Windows Media Player bei Auftreten des Ereignisses aufgerufen wird.

## <a name="parameters"></a>Parameter

Die Funktion, die dieses Ereignis behandelt, nimmt keine Parameter an.

## <a name="remarks"></a>Bemerkungen

Benutzer können die Farbe der Windows Media Player-Benutzeroberfläche ändern. Sie können dieses Ereignis verwenden, um die Darstellung der gehosteten Webseite so anzupassen, dass Sie dem Player entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 2-Online Speicher**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





