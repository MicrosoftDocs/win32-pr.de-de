---
title: Externes. onchangeviewonlinelisterror-Ereignis
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Externes. onchangeviewonlinelisterror-Ereignis
ms.assetid: f53dfc80-a7d7-42b1-b390-e90aa108145f
keywords:
- Externes. onchangeviewonlinelisterror-Ereignisfenster Media Player
topic_type:
- apiref
api_name:
- External.OnChangeViewOnlineListError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e9ff854893268a00cb7b5f2fb35409be2e70e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371685"
---
# <a name="externalonchangeviewonlinelisterror-event"></a>Externes. onchangeviewonlinelisterror-Ereignis

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das **onchangeviewonlinelisterror** -Ereignis tritt auf, wenn ein Aufrufen der [externen. changeviewonlinelist](external-changeviewonlinelist.md) -Methode zu einem Fehler führt.

``` syntax
window.external.OnChangeViewOnlineListError = functionname
```

## <a name="possible-values"></a>Mögliche Werte

Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die den Namen der Funktion im Skript angibt, die von Windows Media Player bei Auftreten des Ereignisses aufgerufen wird.

## <a name="parameters"></a>Parameter

Die Funktion, die diesen Fehler behandelt, verfügt über die folgenden Parameter.

<dl> <dt>

<span id="hr"></span><span id="HR"></span>*HR*
</dt> <dd>

Ein **HRESULT** -Fehlercode, der den Grund für den Fehler angibt.

</dd> <dt>

<span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*Librarylocationtype*
</dt> <dd>

Dieselbe Zeichenfolge, die im **librarylocationtype** -Parameter von **changeviewonlinelist** übergeben wurde.

</dd> <dt>

<span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*Librarylocationid*
</dt> <dd>

Dieselbe Zeichenfolge, die im **librarylocationid** -Parameter von **changeviewonlinelist** übergeben wurde.

</dd> <dt>

<span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*
</dt> <dd>

Dieselbe Zeichenfolge, die im Parameter **para** meters von **changeviewonlinelist** übergeben wurde.

</dd> <dt>

<span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*FriendlyName*
</dt> <dd>

Dieselbe Zeichenfolge, die im **FriendlyName** -Parameter von **changeviewonlinelist** übergeben wurde.

</dd> <dt>

<span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*Listentyp*
</dt> <dd>

Dieselbe Zeichenfolge, die im **ListType** -Parameter von **changeviewonlinelist** übergeben wurde.

</dd> <dt>

<span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*
</dt> <dd>

Dieselbe Zeichenfolge, die im **ViewMode** -Parameter von **changeviewonlinelist** übergeben wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





