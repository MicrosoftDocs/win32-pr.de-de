---
title: Externes. onchangeviewerror-Ereignis
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Externes. onchangeviewerror-Ereignis
ms.assetid: d6370629-5f50-434d-8eb5-5b43d1b2f7fe
keywords:
- Externe. onchangeviewerror-Ereignisfenster Media Player
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
ms.openlocfilehash: 91bcbb71e1c5324a9907d735492364561be49a60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354715"
---
# <a name="externalonchangeviewerror-event"></a>Externes. onchangeviewerror-Ereignis

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das **onchangeviewerror** -Ereignis tritt auf, wenn ein Aufrufvorgang der [externen. changeView](external-changeview.md) -Methode zu einem Fehler führt.

``` syntax
window.external.OnChangeViewError = FunctionName
```

## <a name="possible-values"></a>Mögliche Werte

Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die den Namen der Funktion im Skript angibt, die von Windows Media Player bei Auftreten des Ereignisses aufgerufen wird.

## <a name="parameters"></a>Parameter

Die Funktion, die dieses Ereignis behandelt, verfügt über die folgenden Parameter.

<dl> <dt>

<span id="hr"></span><span id="HR"></span>*HR*
</dt> <dd>

Ein **HRESULT** -Fehlercode, der den Grund für den Fehler angibt.

</dd> <dt>

<span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*Librarylocationtype*
</dt> <dd>

Dieselbe Zeichenfolge, die im **librarylocationtype** -Parameter von **changeView** übergeben wurde.

</dd> <dt>

<span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*Librarylocationid*
</dt> <dd>

Dieselbe Zeichenfolge, die im **librarylocationid** -Parameter von **changeView** übergeben wurde.

</dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Filter*
</dt> <dd>

Dieselbe Zeichenfolge, die im **Filter** -Parameter von **changeView** übergeben wurde.

</dd> <dt>

<span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*Viewparametriams*
</dt> <dd>

Dieselbe Zeichenfolge, die in den **viewparameams** -Parameter von **changeView** übergeben wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externalobject für Typ 1 Online Stores**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





