---
description: Ruft die Vorlagen-ID dieses Dateidatenknotens ab.
ms.assetid: ff0662da-b4f8-4ed2-81d4-6771e91da262
title: ID3DXFileSaveData::GetType-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ec0dddd2106acddc5d09354ba7919eb32a8217a115410a9830803aaae589c891
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987430"
---
# <a name="id3dxfilesavedatagettype-method"></a>ID3DXFileSaveData::GetType-Methode

Ruft die Vorlagen-ID dieses Dateidatenknotens ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetType(
  [in] GUID *type
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*type* \[ In\]
</dt> <dd>

Typ: **[ **GUID**](guid.md)\***

Zeiger auf die GUID, die die Vorlage in diesem Dateidatenknoten darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 




