---
title: External.OnChangeViewError-Ereignis
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | External.OnChangeViewError-Ereignis
ms.assetid: d6370629-5f50-434d-8eb5-5b43d1b2f7fe
keywords:
- External.OnChangeViewError-Windows Media Player
topic_type:
- apiref
api_name:
- External.OnChangeViewError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa1152c753501b2e2385de8c56af614d62cfb367fcca8468aaa032e9536e8d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648830"
---
# <a name="externalonchangeviewerror-event"></a>External.OnChangeViewError-Ereignis

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **OnChangeViewError-Ereignis** tritt auf, wenn ein Aufruf der [External.changeView-Methode](external-changeview.md) zu einem Fehler führt.

``` syntax
window.external.OnChangeViewError = FunctionName
```

## <a name="possible-values"></a>Mögliche Werte

Dies ist eine Schreibeigenschaft, die den Namen der Funktion im Skript angibt, Windows Media Player beim Auftreten des Ereignisses aufruft.

## <a name="parameters"></a>Parameter

Die Funktion, die dieses Ereignis behandelt, verfügt über die folgenden Parameter.

<dl> <dt>

<span id="hr"></span><span id="HR"></span>*Hr*
</dt> <dd>

Ein **HRESULT-Fehlercode,** der die Ursache des Fehlers angibt.

</dd> <dt>

<span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*
</dt> <dd>

Die gleiche Zeichenfolge, die im **LibraryLocationType-Parameter** von **changeView übergeben wurde.**

</dd> <dt>

<span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*
</dt> <dd>

Dieselbe Zeichenfolge, die im **LibraryLocationID-Parameter** von **changeView übergeben wurde.**

</dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Filter*
</dt> <dd>

Dieselbe Zeichenfolge, die im **Filter-Parameter von** **changeView übergeben wurde.**

</dd> <dt>

<span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*ViewParams*
</dt> <dd>

Dieselbe Zeichenfolge, die im **ViewParams-Parameter** von **changeView übergeben wurde.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ExternalObject für Onlineshops vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





