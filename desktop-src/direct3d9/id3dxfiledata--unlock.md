---
description: 'Beendet die Lebensdauer des ppData-Zeigers, der von ID3DXFileData:: Lock zurückgegeben wurde.'
ms.assetid: 6032ea1f-3c73-4157-ba3f-41ce9e73d64c
title: 'ID3DXFileData:: Unlock-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Unlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8371b87152a6184f34a225b24d2de1b0fd21248f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762141"
---
# <a name="id3dxfiledataunlock-method"></a>ID3DXFileData:: Unlock-Methode

Beendet die Lebensdauer des *ppData* -Zeigers, der von [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md)zurückgegeben wurde.

## <a name="syntax"></a>Syntax


```C++
BOOL Unlock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Der Rückgabewert ist "S \_ OK".

## <a name="remarks"></a>Bemerkungen

Sie müssen sicherstellen, dass die Anzahl von [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md) -aufrufen mit der Anzahl von **ID3DXFileData:: Unlock** -aufrufen übereinstimmt. Nach dem Aufrufen von Unlock sollte der von **ID3DXFileData:: Lock** zurückgegebene ppData-Zeiger nicht mehr verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
