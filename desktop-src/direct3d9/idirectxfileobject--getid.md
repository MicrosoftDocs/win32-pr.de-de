---
description: Ruft einen Zeiger auf die GUID ab, die ein DirectX-Dateiobjekt identifiziert. Veraltet.
ms.assetid: 74c7a1d9-85e4-43eb-bcd8-1f3ddd713e9f
title: IDirectXFileObject::GetId-Methode (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetId
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 5cb6788afe0b937822b8895790584f6928a7b5aecb564a31540337935763b2f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800181"
---
# <a name="idirectxfileobjectgetid-method"></a>IDirectXFileObject::GetId-Methode

Ruft einen Zeiger auf die GUID ab, die ein DirectX-Dateiobjekt identifiziert. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetId(
  [out, retval] 
            LPGUID pGuid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pGuid* \[ out, retval\]
</dt> <dd>

Typ: **LPGUID**

Zeiger auf eine GUID, um die ID des Objekts zu empfangen. Die Funktion legt die GUID auf eine **NULL-GUID** fest, wenn das Objekt keine ID hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert DXFILE \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert DXFILEERR \_ BADVALUE sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDirectXFileObject](idirectxfileobject.md)
</dt> </dl>

 

 




