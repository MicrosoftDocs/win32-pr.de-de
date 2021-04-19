---
title: Iwmpstringcollection-Element Methode
description: Die Item-Methode gibt die Zeichenfolge am angegebenen Index zurück.
ms.assetid: 77546cb2-eda5-4bb8-97b9-55270461815f
keywords:
- Element-Methoden Fenster Media Player
- Element-Methode, Windows Media Player, iwmpstringcollection-Schnittstelle
- Iwmpstringcollection-Schnittstelle, Windows Media Player, Element-Methode
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
ms.openlocfilehash: f69bdc63448699a595238b9907f4b1253209ad06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359328"
---
# <a name="iwmpstringcollectionitem-method"></a>Iwmpstringcollection:: Item-Methode

Die **Item** -Methode gibt die Zeichenfolge am angegebenen Index zurück.

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

*Lindex* \[ in\]
</dt> <dd>

Ein **System. Int32** -Wert, der der Index ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **System. String** , bei der es sich um die Zeichenfolge am angegebenen Index handelt.

## <a name="remarks"></a>Bemerkungen

Die **iwmpstringcollection** -Schnittstelle wird verwendet, um den Satz von Werten abzurufen, die für ein Attribut verfügbar sind. Beispielsweise kann die **iwmpmediacollection. getAttributeStringCollection** -Methode zum Abrufen einer **iwmpstringcollection** -Schnittstelle verwendet werden, die alle Werte für das Genre-Attribut innerhalb des audiomedientyps darstellt. Die **Item** -Methode kann dann zum Durchlaufen aller möglichen Werte für das Genre-Attribut verwendet werden.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpmediacollection. getAttributeStringCollection (VB und c#)**](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestmediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[**Iwmpstringcollection-Schnittstelle (VB und c#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





