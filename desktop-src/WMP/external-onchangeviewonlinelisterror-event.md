---
title: External.OnChangeViewOnlineListError-Ereignis
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | External.OnChangeViewOnlineListError-Ereignis
ms.assetid: f53dfc80-a7d7-42b1-b390-e90aa108145f
keywords:
- External.OnChangeViewOnlineListError-Ereignis Windows Media Player
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
ms.openlocfilehash: 3ed6191de129bffea0e11abb24f1e271fc0b2873d2b306430a4e7eafe39b214d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648800"
---
# <a name="externalonchangeviewonlinelisterror-event"></a>External.OnChangeViewOnlineListError-Ereignis

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **OnChangeViewOnlineListError-Ereignis** tritt auf, wenn ein Aufruf der [External.changeViewOnlineList-Methode](external-changeviewonlinelist.md) zu einem Fehler führt.

``` syntax
window.external.OnChangeViewOnlineListError = functionname
```

## <a name="possible-values"></a>Mögliche Werte

Dies ist eine Schreibeigenschaft, die den Namen der Funktion im Skript angibt, die aufruft, wenn das Ereignis auftritt, Windows Media Player.

## <a name="parameters"></a>Parameter

Die Funktion, die diesen Fehler behandelt, verfügt über die folgenden Parameter.

<dl> <dt>

<span id="hr"></span><span id="HR"></span>*Hr*
</dt> <dd>

Ein  HRESULT-Fehlercode, der die Ursache des Fehlers angibt.

</dd> <dt>

<span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*
</dt> <dd>

Die gleiche Zeichenfolge, die im **LibraryLocationType-Parameter** von **changeViewOnlineList** übergeben wurde.

</dd> <dt>

<span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*
</dt> <dd>

Die gleiche Zeichenfolge, die im **LibraryLocationID-Parameter** von **changeViewOnlineList** übergeben wurde.

</dd> <dt>

<span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*
</dt> <dd>

Die gleiche Zeichenfolge, die im **Params-Parameter** von **changeViewOnlineList** übergeben wurde.

</dd> <dt>

<span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*Friendlyname*
</dt> <dd>

Die gleiche Zeichenfolge, die im **FriendlyName-Parameter** von **changeViewOnlineList** übergeben wurde.

</dd> <dt>

<span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*ListType*
</dt> <dd>

Die gleiche Zeichenfolge, die im **ListType-Parameter** von **changeViewOnlineList** übergeben wurde.

</dd> <dt>

<span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*Viewmode*
</dt> <dd>

Die gleiche Zeichenfolge, die im **ViewMode-Parameter** von **changeViewOnlineList** übergeben wurde.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für Onlineshops vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





