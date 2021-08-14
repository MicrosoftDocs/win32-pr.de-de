---
title: IWMPStringCollection2 isIdentical-Methode
description: Die isIdentical-Methode gibt einen Wert zurück, der angibt, ob das von der angegebenen Schnittstelle dargestellte Objekt mit dem aktuellen identisch ist.
ms.assetid: 826e7fd8-88f8-4a2a-9ca0-82a500099272
keywords:
- isIdentical-Windows Media Player
- isIdentical-Windows Media Player , IWMPStringCollection2-Schnittstelle
- IWMPStringCollection2-Schnittstelle Windows Media Player , isIdentical-Methode
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
ms.openlocfilehash: 4576522c1b6d6834ded5e100a2618dcb45204f887420968a5828fdc5c9bd0fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330904"
---
# <a name="iwmpstringcollection2isidentical-method"></a>IWMPStringCollection2::isIdentical-Methode

Die **isIdentical-Methode** gibt einen Wert zurück, der angibt, ob das von der angegebenen Schnittstelle dargestellte Objekt mit dem aktuellen identisch ist.

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

*pIWMPStringCollection2* \[ In\]
</dt> <dd>

Die **WMPLib.IWMPStringCollection2-Schnittstelle,** die das Objekt darstellt, das mit der aktuellen verglichen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der **Boolesche Wert system.boolean,** der das Ergebnis des Vergleichs ist. Der Wert **true gibt an,** dass die Zeichenfolgensammlungsobjekte identisch sind.

## <a name="remarks"></a>Hinweise

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPStringCollection2-Schnittstelle (VB und C#)**](iwmpstringcollection2--vb-and-c.md)
</dt> </dl>

 

 





