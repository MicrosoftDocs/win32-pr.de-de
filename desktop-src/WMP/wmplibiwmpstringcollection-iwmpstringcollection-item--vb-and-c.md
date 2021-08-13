---
title: IWMPStringCollection Item-Methode
description: Die Item-Methode gibt die Zeichenfolge am angegebenen Index zurück.
ms.assetid: 77546cb2-eda5-4bb8-97b9-55270461815f
keywords:
- Elementmethoden-Windows Media Player
- Item-Methode Windows Media Player , IWMPStringCollection-Schnittstelle
- IWMPStringCollection-Schnittstelle Windows Media Player , Item-Methode
topic_type:
- apiref
api_name:
- IWMPStringCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47928502dce9ed4deb12461763a499de5d962aa1303b4c9cc5eacb02c7619da5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568426"
---
# <a name="iwmpstringcollectionitem-method"></a>IWMPStringCollection::Item-Methode

Die **Item-Methode** gibt die Zeichenfolge am angegebenen Index zurück.

## <a name="syntax"></a>Syntax


```CSharp
public System.String Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPStringCollection.Item
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*lIndex* \[ In\]
</dt> <dd>

Eine **System.Int32,die** der Index ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **System.String,** die die Zeichenfolge am angegebenen Index ist.

## <a name="remarks"></a>Hinweise

Die **IWMPStringCollection-Schnittstelle** wird verwendet, um den Satz von Werten abzurufen, die für ein Attribut verfügbar sind. Beispielsweise kann die **IWMPMediaCollection.getAttributeStringCollection-Methode** verwendet werden, um eine **IWMPStringCollection-Schnittstelle** abzurufen, die alle Werte für das Genre-Attribut im Audiomedientyp darstellt. Die **Item-Methode** kann dann verwendet werden, um alle möglichen Werte für das Genre-Attribut zu durchlaufen.

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IWMPMediaCollection.getAttributeStringCollection (VB und C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection-Schnittstelle (VB und C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





