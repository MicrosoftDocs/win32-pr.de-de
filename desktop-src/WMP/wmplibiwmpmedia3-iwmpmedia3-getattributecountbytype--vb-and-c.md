---
title: IWMPMedia3 getAttributeCountByType-Methode
description: Die getAttributeCountByType-Methode gibt die Anzahl der Attribute zurück, die dem angegebenen Attributtyp zugeordnet sind.
ms.assetid: d692635f-f9f1-4d8e-a9c5-9d7fa84f41bd
keywords:
- getAttributeCountByType-Methode Windows Media Player
- getAttributeCountByType-Methode Windows Media Player , IWMPMedia3-Schnittstelle
- IWMPMedia3-Schnittstelle Windows Media Player , getAttributeCountByType-Methode
topic_type:
- apiref
api_name:
- IWMPMedia3.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c8e3fc681ea5471457bd9a80ac3e26dabc08b2112387dd8c5f785bf5f055dfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000110"
---
# <a name="iwmpmedia3getattributecountbytype-method"></a>IWMPMedia3::getAttributeCountByType-Methode

Die **getAttributeCountByType-Methode** gibt die Anzahl der Attribute zurück, die dem angegebenen Attributtyp zugeordnet sind.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 getAttributeCountByType(
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPMedia3.getAttributeCountByType
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrType* \[ In\]
</dt> <dd>

Eine **System.String,die** der Attributtyp ist.

</dd> <dt>

*bstrLanguage* \[ In\]
</dt> <dd>

Eine **System.String-Datei,** die die Sprache ist. Wenn der Wert auf NULL oder eine Zeichenfolge der Länge 0 ("") festgelegt ist, wird die aktuelle Gebietsschemazeichenfolge verwendet. Andernfalls muss der Wert eine gültige RFC 1766-Sprachzeichenfolge wie "en-us" sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine **System.Int32-Datei,** bei der es sich um die Anzahl der Attribute handelt, die dem Typ zugeordnet sind.

## <a name="remarks"></a>Hinweise

Diese Methode wird verwendet, um die Anzahl der Attribute zu ermitteln, die einem bestimmten Attributnamen für ein bestimmtes Medienelement entsprechen. Indexnummern können dann an die **getItemInfoByType-Methode** übergeben werden. Dies ist z. B. nützlich, wenn ein Medienelement unter mehreren Medienobjekten kategorisiert wurde.

Vor dem Aufrufen dieser Methode benötigen Sie Lesezugriff auf die Bibliothek. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player Serie 9 oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPMedia3-Schnittstelle (VB und C#)**](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3.getItemInfoByType (VB und C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





