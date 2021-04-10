---
description: Fügt einen Daten Verweis als untergeordnetes Element dieses ID3DXFileSaveData File Data-Knotens hinzu. Der Daten Verweis verweist auf ein Datei Datenobjekt.
ms.assetid: 75bfe91e-15ea-41f3-b1f7-071fb7f0093f
title: 'ID3DXFileSaveData:: adddatareferenzierungsmethode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataReference
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f4aabf5601ef73f4e1062b1db1a28c1f0deae5fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961656"
---
# <a name="id3dxfilesavedataadddatareference-method"></a>ID3DXFileSaveData:: adddatareferenzierungsmethode

Fügt einen Daten Verweis als untergeordnetes Element dieses [**ID3DXFileSaveData**](id3dxfilesavedata.md) File Data-Knotens hinzu. Der Daten Verweis verweist auf ein Datei Datenobjekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szName,
  [in] const GUID   *pId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szName* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ein Zeiger auf den Namen des Datenobjekts, das als Verweis hinzugefügt werden soll. Geben Sie **null** an, wenn das Datenobjekt keinen Namen hat.

</dd> <dt>

*pId* \[ in\]
</dt> <dd>

Typ: Konstante **[**GUID**](guid.md) \***

Zeiger auf eine GUID, die das Datenobjekt darstellt, das als Verweis hinzugefügt werden soll. Wenn der Wert **null** ist, wird ein Verweis hinzugefügt, der auf das Datenobjekt mit dem Namen verweist, der von szName angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DXFERR \_ badobject, D3DXFERR \_ badvalue, E \_ oudebmemory.

## <a name="remarks"></a>Bemerkungen

Das Datei Datenobjekt, auf das verwiesen wird, muss entweder einen Namen oder eine GUID aufweisen. Das Datei Datenobjekt muss auch von einem anderen übergeordneten [**ID3DXFileSaveData**](id3dxfilesavedata.md) -Objekt abgeleitet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFileSaveData](id3dxfilesavedata.md)
</dt> </dl>

 

 
