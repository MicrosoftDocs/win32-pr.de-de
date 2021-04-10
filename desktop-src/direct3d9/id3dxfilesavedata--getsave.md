---
description: Ruft einen Zeiger auf diesen ID3DXFileSaveObject File Data-Knoten ab.
ms.assetid: 092d1c6f-0a53-4b8e-84ec-bc76f3f647ac
title: 'ID3DXFileSaveData:: getsave-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetSave
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4e23296ad0a866a0ad289a9a587c433411ef9bb8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219691"
---
# <a name="id3dxfilesavedatagetsave-method"></a>ID3DXFileSaveData:: getsave-Methode

Ruft einen Zeiger auf diesen [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) File Data-Knoten ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSave(
  [out] ID3DXFileSaveObject **ppObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppobj* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***

Adresse eines Zeigers auf eine [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) -Schnittstelle, die diesen Datei Datenknoten darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DXFERR \_ badvalue.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 




