---
title: IWMPMedia getItemInfoByAtom-Methode
description: Die getItemInfoByAtom-Methode gibt den Wert des Attributs mit der angegebenen Indexnummer zurück.
ms.assetid: d9a4b737-add1-4bbd-8e03-e58f45d65a62
keywords:
- getItemInfoByAtom-Methode Windows Media Player
- getItemInfoByAtom-Methode Windows Media Player , IWMPMedia-Schnittstelle
- IWMPMedia-Schnittstelle Windows Media Player , getItemInfoByAtom-Methode
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfoByAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72a8820618b39418aa7be82faeef15a372e0e0f90c0db025e99c55be49d8c13e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115694"
---
# <a name="iwmpmediagetiteminfobyatom-method"></a>IWMPMedia::getItemInfoByAtom-Methode

Die **getItemInfoByAtom-Methode** gibt den Wert des Attributs mit der angegebenen Indexnummer zurück.

## <a name="syntax"></a>Syntax


```CSharp
public System.String getItemInfoByAtom(
  System.Int32 lAtom
);
```


```VB

Public Function getItemInfoByAtom( _
  ByVal lAtom As System.Int32 _
) As System.String
Implements IWMPMedia.getItemInfoByAtom
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*lAtom* \[ In\]
</dt> <dd>

Eine **System.Int32-Datei,** die den Index angibt, an dem sich das angeforderte Attribut innerhalb des Satzes verfügbarer Attribute befindet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **System.String,** die der Wert des Attributs ist.

## <a name="remarks"></a>Hinweise

Diese Methode kann verwendet werden, um Metadaten für ein bestimmtes Medienelement mithilfe einer Attributindexnummer abzurufen. Die **attributeCount-Eigenschaft** kann verwendet werden, um die Anzahl der für das Medienelement verfügbaren Attribute zu bestimmen.

Die **getMediaAtom-Methode** der **IWMPMediaCollection-Schnittstelle** kann auch verwendet werden, um den Index eines bestimmten Attributs abzurufen. Diese Technik ist im Allgemeinen effizienter als die **getItemInfo-** oder **getItemInfoByType-Methoden** bei der Arbeit mit großen Wiedergabelisten.

Vor dem Aufrufen dieser Methode benötigen Sie Lesezugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPMedia-Schnittstelle (VB und C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.attributeCount (VB und C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.getItemInfo (VB und C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.setItemInfo (VB und C#)**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3.getItemInfoByType (VB und C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection.getMediaAtom (VB und C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)
</dt> </dl>

 

 





