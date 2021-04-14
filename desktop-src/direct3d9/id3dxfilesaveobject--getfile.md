---
description: Ruft die ID3DXFile-Schnittstelle des-Objekts ab, das dieses ID3DXFileSaveObject-Objekt erstellt hat.
ms.assetid: 79249d17-cae3-43d9-9ccb-fa804b02a353
title: 'ID3DXFileSaveObject:: GetFile-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 137f8245b94bb0ebd14e81d5f73a7ba9622a4933
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394174"
---
# <a name="id3dxfilesaveobjectgetfile-method"></a>ID3DXFileSaveObject:: GetFile-Methode

Ruft die [**ID3DXFile**](id3dxfile.md) -Schnittstelle des-Objekts ab, das dieses [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) -Objekt erstellt hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFile(
  [in] ID3DXFile ppFile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppfile* \[ in\]
</dt> <dd>

Typ: **[ **ID3DXFile**](id3dxfile.md)**

Adresse eines Zeigers auf ein [**ID3DXFile**](id3dxfile.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DXFERR \_ badvalue, e \_ nointerface, e- \_ Zeiger.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 




