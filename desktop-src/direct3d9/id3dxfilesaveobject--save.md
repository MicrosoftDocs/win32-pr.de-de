---
description: Speichert ein Datenobjekt und seine untergeordneten Elemente in einer X-Datei auf dem Datenträger.
ms.assetid: a48cd1b2-d1e7-446b-8482-485ccdd59353
title: ID3DXFileSaveObject::Save-Methode (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.Save
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a49c4776f9ce590d287869436b329ddf9a378e73f04f0127246fc890944ffee3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563960"
---
# <a name="id3dxfilesaveobjectsave-method"></a>ID3DXFileSaveObject::Save-Methode

Speichert ein Datenobjekt und seine untergeordneten Elemente in einer X-Datei auf dem Datenträger.

## <a name="syntax"></a>Syntax


```C++
HRESULT Save();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert wie folgt sein: D3DXFERR \_ BADOBJECT.

## <a name="remarks"></a>Hinweise

Nachdem diese Methode erfolgreich ausgeführt wurde, können [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) und [**ID3DXFileSaveData::AddDataReference**](id3dxfilesavedata--adddatareference.md) nicht mehr aufgerufen werden, bis ein neues [**ID3DXFile-Objekt**](id3dxfile.md) erstellt wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 




