---
title: IWMPStringCollection2 isidentical-Methode
description: Die isidentical-Methode gibt einen Wert zurück, der angibt, ob das durch die angegebene Schnittstelle dargestellte Objekt mit dem aktuellen identisch ist.
ms.assetid: 826e7fd8-88f8-4a2a-9ca0-82a500099272
keywords:
- isidentical-Methode, Windows Media Player
- isidentical-Methode, Windows Media Player, IWMPStringCollection2-Schnittstelle
- IWMPStringCollection2 Interface, Windows Media Player, isidentical-Methode
topic_type:
- apiref
api_name:
- IWMPStringCollection2.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb760dae213f28d44fbc707b4430cb151cfe578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365747"
---
# <a name="iwmpstringcollection2isidentical-method"></a>IWMPStringCollection2:: isidentical-Methode

Die **isidentical** -Methode gibt einen Wert zurück, der angibt, ob das durch die angegebene Schnittstelle dargestellte Objekt mit dem aktuellen identisch ist.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean isIdentical(
  IWMPStringCollection2 pIWMPStringCollection2
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPStringCollection2 As IWMPStringCollection2 _
) As System.Boolean
Implements IWMPStringCollection2.isIdentical
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*pIWMPStringCollection2* \[ in\]
</dt> <dd>

Die **WMPLib. IWMPStringCollection2** -Schnittstelle, die das Objekt darstellt, das mit dem aktuellen verglichen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der **System. Boolean** -Wert, der das Ergebnis des Vergleichs ist. Der Wert **true** gibt an, dass die Zeichen folgen Auflistungs Objekte identisch sind.

## <a name="remarks"></a>Bemerkungen

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPStringCollection2-Schnittstelle (VB und c#)**](iwmpstringcollection2--vb-and-c.md)
</dt> </dl>

 

 





