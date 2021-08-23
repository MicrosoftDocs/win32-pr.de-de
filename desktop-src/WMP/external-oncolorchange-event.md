---
title: External.OnColorChange-Ereignis
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | External.OnColorChange-Ereignis
ms.assetid: f2cd44b1-c813-479b-b847-96ddb9572697
keywords:
- External.OnColorChange-Windows Media Player
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
ms.openlocfilehash: eae4ca15d4d7035fc342fa20263220560570d902e28b9245a6458ac59c40a4f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648750"
---
# <a name="externaloncolorchange-event"></a>External.OnColorChange-Ereignis

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **OnColorChange-Ereignis** tritt auf, wenn sich die Farbe Windows Media Player Benutzeroberfläche ändert.

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a>Mögliche Werte

Dies ist eine Schreibeigenschaft, die den Namen der Funktion im Skript angibt, Windows Media Player beim Auftreten des Ereignisses aufruft.

## <a name="parameters"></a>Parameter

Die Funktion, die dieses Ereignis behandelt, nimmt keine Parameter an.

## <a name="remarks"></a>Hinweise

Benutzer können die Farbe der Windows Media Player ändern. Sie können dieses Ereignis verwenden, um die Darstellung Ihrer gehosteten Webseite an den Player anzupassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für Onlinespeicher vom Typ 2**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





