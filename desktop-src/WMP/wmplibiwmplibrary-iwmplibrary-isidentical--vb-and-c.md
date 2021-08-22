---
title: IWMPLibrary isIdentical-Methode
description: Die isIdentical-Methode gibt einen Wert zurück, der angibt, ob das angegebene Objekt mit dem aktuellen Objekt identisch ist.
ms.assetid: c4eebc46-6a5f-4f9a-8cd4-7421b156670c
keywords:
- isIdentical-Methode Windows Media Player
- isIdentical-Methode Windows Media Player , IWMPLibrary-Schnittstelle
- IWMPLibrary-Schnittstelle Windows Media Player , isIdentical-Methode
topic_type:
- apiref
api_name:
- IWMPLibrary.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ed37725bbda5b170ece8ce71c12499b42f0b361cbac3bbe65f1b875af06fc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506050"
---
# <a name="iwmplibraryisidentical-method"></a>IWMPLibrary::isIdentical-Methode

Die **isIdentical-Methode** gibt einen Wert zurück, der angibt, ob das angegebene Objekt mit dem aktuellen Objekt identisch ist.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean isIdentical(
  IWMPLibrary pIWMPLibrary
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPLibrary As IWMPLibrary _
) As System.Boolean
Implements IWMPLibrary.isIdentical
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*pIWMPLibrary* \[ In\]
</dt> <dd>

Eine **WMPLib.IWMPLibrary-Schnittstelle,** die das Objekt darstellt, das mit der aktuellen verglichen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System.Boolean,** der das Ergebnis des Vergleichs ist. Der Wert **true** gibt an, dass die Objekte identisch sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPLibrary-Schnittstelle (VB und C#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





