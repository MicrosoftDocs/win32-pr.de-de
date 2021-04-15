---
description: Speichert ein Datenobjekt und seine untergeordneten Elemente in einer x-Datei auf dem Datenträger.
ms.assetid: a48cd1b2-d1e7-446b-8482-485ccdd59353
title: 'ID3DXFileSaveObject:: Save-Methode (D3DX9Xof. h)'
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
ms.openlocfilehash: c97c2ccf6c509aec1d217e3179c927fe2bb5a797
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394125"
---
# <a name="id3dxfilesaveobjectsave-method"></a>ID3DXFileSaveObject:: Save-Methode

Speichert ein Datenobjekt und seine untergeordneten Elemente in einer x-Datei auf dem Datenträger.

## <a name="syntax"></a>Syntax


```C++
HRESULT Save();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DXFERR \_ badobject.

## <a name="remarks"></a>Bemerkungen

Nachdem diese Methode erfolgreich ausgeführt wurde, können [**ID3DXFileSaveObject:: adddataobject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData:: adddataobject**](id3dxfilesavedata--adddataobject.md) und [**ID3DXFileSaveData:: adddatareferenzierungsart**](id3dxfilesavedata--adddatareference.md) nicht mehr aufgerufen werden, bis ein neues [**ID3DXFile**](id3dxfile.md) -Objekt erstellt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 




