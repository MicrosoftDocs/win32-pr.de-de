---
description: Ruft die GUID dieses ID3DXFileSaveData-Dateidatenknotens ab.
ms.assetid: 79413eb4-4889-4148-b1a1-58a0b780403c
title: ID3DXFileSaveData::GetId-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetId
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4e6f502357510cc1c8fc51e9ada844a988a79b1571435639586380929b121c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748500"
---
# <a name="id3dxfilesavedatagetid-method"></a>ID3DXFileSaveData::GetId-Methode

Ruft die GUID dieses [**ID3DXFileSaveData-Dateidatenknotens**](id3dxfilesavedata.md) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetId(
  [out] 
            LPGUID pId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pId* \[ out\]
</dt> <dd>

Typ: **LPGUID**

Zeiger auf eine GUID, um die ID dieses Dateidatenknotens zu empfangen. Wenn das Objekt keine ID hat, ist der zurückgegebene Parameterwert GUID \_ NULL.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 




