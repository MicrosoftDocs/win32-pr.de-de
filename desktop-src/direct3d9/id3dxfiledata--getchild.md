---
description: 'ID3DXFileData::GetChild-Methode: Ruft ein untergeordnetes Objekt in diesem Dateidatenobjekt ab.'
ms.assetid: 0c4f1efa-f096-443d-a482-a3c5a9138c3d
title: ID3DXFileData::GetChild-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8442577ab70b3ce4b08229d1b21989e614d8f328d3012042d3b1b5dc524f4604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295336"
---
# <a name="id3dxfiledatagetchild-method"></a>ID3DXFileData::GetChild-Methode

Ruft ein untergeordnetes Objekt in diesem Dateidatenobjekt ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetChild(
  [in] SIZE_T        uiChild,
  [in] ID3DXFileData **ppChild
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uiChild* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

ID des abzurufenden untergeordneten Objekts.

</dd> <dt>

*ppChild* \[ In\]
</dt> <dd>

Typ: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

Adresse eines Zeigers zum Empfangen des Schnittstellenzeigers des untergeordneten Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Werte sein: D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
