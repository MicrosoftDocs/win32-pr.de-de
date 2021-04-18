---
title: Iwmplibraryservices getlibrarybytype-Methode
description: Die getlibrarybytype-Methode gibt eine iwmplibrary-Schnittstelle zurück, die die Bibliothek mit dem angegebenen Typ und Index darstellt.
ms.assetid: 2507c764-a2cf-42f9-ad44-eaf040b78891
keywords:
- getlibrarybytype-Methode, Windows Media Player
- getlibrarybytype-Methode, Windows Media Player, iwmplibraryservices-Schnittstelle
- Iwmplibraryservices Interface, Windows Media Player, getlibrarybytype-Methode
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getLibraryByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d57fcc71f912fe1ee896ec893ea8f556eeb2277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361019"
---
# <a name="iwmplibraryservicesgetlibrarybytype-method"></a>Iwmplibraryservices:: getlibrarybytype-Methode

Die **getlibrarybytype** -Methode gibt eine **iwmplibrary** -Schnittstelle zurück, die die Bibliothek mit dem angegebenen Typ und Index darstellt.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPLibrary getLibraryByType(
  WMPLibraryType wmplt,
  System.Int32 lIndex
);
```


```VB

Public Function getLibraryByType( _
  ByVal wmplt As WMPLibraryType, _
  ByVal lIndex As System.Int32 _
) As IWMPLibrary
Implements IWMPLibraryServices.getLibraryByType
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*wmplt* \[ in\]
</dt> <dd>

Ein Wert aus der **WMPLib. wmplibrarytype** -Enumeration, der den Typ der abzurufenden Bibliothek angibt.

</dd> <dt>

*Lindex* \[ in\]
</dt> <dd>

Ein **System. Int32** -Wert, der den Index der abzurufenden Bibliothek ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib. iwmplibrary** -Schnittstelle für die Bibliothek, die zurückgegeben wird.

## <a name="remarks"></a>Bemerkungen

Es gibt nur eine lokale Bibliothek, und die Disk-Bibliotheken sind nur auf Daten-CDs und DVDs verfügbar, die Medieninhalte enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmplibrary-Schnittstelle (VB und c#)**](iwmplibrary--vb-and-c.md)
</dt> <dt>

[**Iwmplibraryservices-Schnittstelle (VB und c#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**Wmplibrarytype**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





