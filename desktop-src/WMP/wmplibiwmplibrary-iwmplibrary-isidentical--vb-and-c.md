---
title: Iwmplibrary (isidentical-Methode)
description: Die isidentical-Methode gibt einen Wert zurück, der angibt, ob das angegebene Objekt mit dem aktuellen-Objekt identisch ist.
ms.assetid: c4eebc46-6a5f-4f9a-8cd4-7421b156670c
keywords:
- isidentical-Methode, Windows Media Player
- isidentical-Methode, Windows Media Player, iwmplibrary-Schnittstelle
- Iwmplibrary-Schnittstelle, Windows Media Player, isidentical-Methode
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
ms.openlocfilehash: 53071caa98b8f8e3ccb95e926969926cc68e7860
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370801"
---
# <a name="iwmplibraryisidentical-method"></a>Iwmplibrary:: isidentical-Methode

Die **isidentical** -Methode gibt einen Wert zurück, der angibt, ob das angegebene Objekt mit dem aktuellen-Objekt identisch ist.

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

*piwmplibrary* \[ in\]
</dt> <dd>

Eine **WMPLib. iwmplibrary** -Schnittstelle, die das Objekt darstellt, das mit dem aktuellen verglichen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System. Boolean** -Wert, der das Ergebnis des Vergleichs ist. Der Wert **true** gibt an, dass die Objekte identisch sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmplibrary-Schnittstelle (VB und c#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





