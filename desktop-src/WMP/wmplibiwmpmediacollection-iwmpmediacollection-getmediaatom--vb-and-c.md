---
title: IWMPMediaCollection getMediaAtom-Methode
description: Die getMediaAtom-Methode gibt den Index eines angegebenen Attributs innerhalb des Sets verfügbarer Attribute zurück.
ms.assetid: 01e3d073-677b-4939-96d3-63ae96eaa25d
keywords:
- getMediaAtom-Windows Media Player
- getMediaAtom-Methode Windows Media Player , IWMPMediaCollection-Schnittstelle
- IWMPMediaCollection-Schnittstelle Windows Media Player , getMediaAtom-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getMediaAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39bd626537defe07fd214c61e29aac67f8c125034817f8a9041a586ab3b24e35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117929773"
---
# <a name="iwmpmediacollectiongetmediaatom-method"></a>IWMPMediaCollection::getMediaAtom-Methode

Die `getMediaAtom` -Methode gibt den Index eines angegebenen Attributs innerhalb der Gruppe verfügbarer Attribute zurück.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 getMediaAtom(
  System.String bstrItemName
);
```


```VB

Public Function getMediaAtom( _
  ByVal bstrItemName As System.String _
) As System.Int32
Implements IWMPMediaCollection.getMediaAtom
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrItemName* \[ In\]
</dt> <dd>

Die **System.String,** die der Name des Elements ist, für das der Index abgerufen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Das **System.Int32,** das der Index ist.

## <a name="remarks"></a>Hinweise

Die mit dieser Methode abgerufene Indexnummer kann an **IWMPMedia.getItemInfoByAtom** übergeben werden, um auf Attributwerte zu zugreifen. Diese Technik ist im Allgemeinen effizienter bei der Arbeit mit großen Wiedergabelisten als der Zugriff auf einen Attributwert über **IWMPMedia.getItemInfo.**

Bevor Sie diese Methode aufrufen, müssen Sie über Lesezugriff auf die Bibliothek verfügen. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPMedia.getItemInfo (VB und C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.getItemInfoByAtom (VB und C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection-Schnittstelle (VB und C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





