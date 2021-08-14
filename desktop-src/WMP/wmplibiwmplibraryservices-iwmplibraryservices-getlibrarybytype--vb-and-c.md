---
title: IWMPLibraryServices getLibraryByType-Methode
description: Die getLibraryByType-Methode gibt eine IWMPLibrary-Schnittstelle zurück, die die Bibliothek mit dem angegebenen Typ und Index darstellt.
ms.assetid: 2507c764-a2cf-42f9-ad44-eaf040b78891
keywords:
- getLibraryByType-Windows Media Player
- getLibraryByType-Methode Windows Media Player , IWMPLibraryServices-Schnittstelle
- IWMPLibraryServices-Schnittstelle Windows Media Player , getLibraryByType-Methode
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
ms.openlocfilehash: f83d74c8c03f8b08936c3693c77e211cd87a8b42c2d020c26ee5133406a2a042
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746208"
---
# <a name="iwmplibraryservicesgetlibrarybytype-method"></a>IWMPLibraryServices::getLibraryByType-Methode

Die **getLibraryByType-Methode** gibt eine **IWMPLibrary-Schnittstelle zurück,** die die Bibliothek mit dem angegebenen Typ und Index darstellt.

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

*wmplt* \[ In\]
</dt> <dd>

Ein Wert aus der **WMPLib.WMPLibraryType-Enumeration,** der den Typ der abzurufenden Bibliothek angibt.

</dd> <dt>

*lIndex* \[ In\]
</dt> <dd>

Ein **System.Int32,** das der Index der abzurufenden Bibliothek ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **WMPLib.IWMPLibrary-Schnittstelle** für die zurückgegebene Bibliothek.

## <a name="remarks"></a>Hinweise

Es gibt nur eine lokale Bibliothek, und Datenträgerbibliotheken sind nur auf Daten-CDs und DVDs verfügbar, die Medieninhalte enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPLibrary-Schnittstelle (VB und C#)**](iwmplibrary--vb-and-c.md)
</dt> <dt>

[**IWMPLibraryServices-Schnittstelle (VB und C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**WMPLibraryType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





