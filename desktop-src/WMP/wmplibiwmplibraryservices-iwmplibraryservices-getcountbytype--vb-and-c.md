---
title: Methode "iwmplibraryservices getcountrytbytype"
description: Die getfactbytype-Methode gibt die Anzahl der verfügbaren Bibliotheken eines angegebenen Typs zurück.
ms.assetid: 75f22e21-fbaf-45dc-b64f-1f687a3cf241
keywords:
- getzähltbytype-Methode, Windows Media Player
- getzähltbytype-Methode, Windows Media Player, iwmplibraryservices-Schnittstelle
- Iwmplibraryservices-Schnittstelle, Windows Media Player, getzähltbytype-Methode
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbd874c06c2557102011c63ee1abb895d092656
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362096"
---
# <a name="iwmplibraryservicesgetcountbytype-method"></a>Iwmplibraryservices:: getzählbytype-Methode

Die **getfactbytype** -Methode gibt die Anzahl der verfügbaren Bibliotheken eines angegebenen Typs zurück.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 getCountByType(
  WMPLibraryType wmplt
);
```


```VB

Public Function getCountByType( _
  ByVal wmplt As WMPLibraryType _
) As System.Int32
Implements IWMPLibraryServices.getCountByType
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*wmplt* \[ in\]
</dt> <dd>

Ein Wert aus der **WMPLib. wmplibrarytype** -Enumeration, der den Typ der zu zählenden Bibliothek angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System. Int32** -Wert, der die Anzahl der Bibliotheken ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmplibraryservices-Schnittstelle (VB und c#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**Wmplibrarytype**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





