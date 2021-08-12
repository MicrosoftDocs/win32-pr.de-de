---
description: Ruft die GUID der Vorlage des Objekts ab. Veraltet.
ms.assetid: bb4a4a32-a9e7-4caa-869d-24cfb310d8d1
title: IDirectXFileData::GetType-Methode (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 564d682c606d8b6bc0001f5d430d2d93f36c25210746169af4802512c330da08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292276"
---
# <a name="idirectxfiledatagettype-method"></a>IDirectXFileData::GetType-Methode

Ruft die GUID der Vorlage des Objekts ab. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetType(
  [out, retval] const GUID **ppguid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppguid* \[ out, retval\]
</dt> <dd>

Typ: **const [**GUID**](guid.md) \* \***

Adresse eines Zeigers, der die GUID der Vorlage des Objekts empfangen soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert DXFILE \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert DXFILEERR \_ BADVALUE sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> </dl>

 

 




