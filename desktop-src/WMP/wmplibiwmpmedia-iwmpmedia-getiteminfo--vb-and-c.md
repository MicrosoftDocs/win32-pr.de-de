---
title: IWMPMedia getItemInfo-Methode
description: Die getItemInfo-Methode gibt den Wert des angegebenen Attributs für das Medienelement zurück.
ms.assetid: b95fa61d-a600-4f31-a930-d80516204034
keywords:
- getItemInfo-Windows Media Player
- getItemInfo-Methode Windows Media Player , IWMPMedia-Schnittstelle
- IWMPMedia-Schnittstelle Windows Media Player , getItemInfo-Methode
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce8fa8b55074781dd835e116b0403391fe9343af30d5236610219dca8aba810b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331990"
---
# <a name="iwmpmediagetiteminfo-method"></a>IWMPMedia::getItemInfo-Methode

Die **getItemInfo-Methode** gibt den Wert des angegebenen Attributs für das Medienelement zurück.

## <a name="syntax"></a>Syntax


```CSharp
public System.String getItemInfo(
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPMedia.getItemInfo
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrItemName* \[ In\]
</dt> <dd>

Eine **System.String,die** den Namen des Attributs ist. Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Attributreferenz.](attribute-reference.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **System.String,** die der Wert des angegebenen Attributs ist.

## <a name="remarks"></a>Hinweise

Diese Methode gibt die Metadaten für ein einzelnes Medienelement oder ein Medienelement zurück, das Teil einer Wiedergabeliste ist.

Die **attributeCount-Eigenschaft** ruft die Anzahl der Attributnamen ab, die für ein bestimmtes Medienelement verfügbar sind. Indexnummern können dann mit der **getAttributeName-Methode** verwendet werden, um den Namen jedes verfügbaren Attributs zu bestimmen. Einzelne Attributnamen können an **getItemInfo übergeben werden.**

Verwenden Sie zum Abrufen von Attributen mit mehreren Werten und Attributen mit komplexen Werten die **getItemInfoByType-Methode.**

Wenn das Medienelement aus einer Bibliothek stammt, die durch Aufrufen von [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)abgerufen wurde, unterscheiden sich die verfügbaren Attribute von den Attributen, die von der lokalen Bibliothek abgefragt werden können, die durch Aufrufen von [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)abgerufen wird. Beispielsweise sind die attributes, die aus der lokalen Bibliothek verfügbar sind, die mithilfe von **IWMPLibrary** abgerufen wurde, eine Teilmenge der Attribute, die aus der lokalen Bibliothek verfügbar sind, die mithilfe von **IWMPCore abgerufen wurde.** Der Satz von Attributen, die aus anderen Quellen (Remotebibliotheken, portable Geräte oder CDs) verfügbar sind, wird von den anderen Quellen definiert.

Bevor Sie diese Methode aufrufen, müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributreferenz**](attribute-reference.md)
</dt> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.attributeCount (VB und C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.getAttributeName (VB und C#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.setItemInfo (VB und C#)**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3.getItemInfoByType (VB und C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





