---
description: Registriert benutzerdefinierte Vorlagen bei Angabe eines ID3DXFileEnumObject-Enumerationsobjekt.
ms.assetid: 1b0c71db-639b-4836-8a65-7d0a2ed3ba4f
title: 'ID3DXFile:: registerenumtemplates-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterEnumTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 89a8b136bdc0e202fc87ba8fd4d7f013203814eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394178"
---
# <a name="id3dxfileregisterenumtemplates-method"></a>ID3DXFile:: registerenumtemplates-Methode

Registriert benutzerdefinierte Vorlagen bei Angabe eines [**ID3DXFileEnumObject**](id3dxfileenumobject.md) -Enumerationsobjekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterEnumTemplates(
  [in] ID3DXFileEnumObject *pEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

"- *ID* \[ " in\]
</dt> <dd>

Typ: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\***

Zeiger auf ein [**ID3DXFileEnumObject**](id3dxfileenumobject.md) -Enumerationsobjekt, das Vorlagen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.

Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DXFERR \_ badvalue.

## <a name="remarks"></a>Bemerkungen

Wenn diese Methode aufgerufen wird, kopiert Sie Vorlagen, die mit dem ID3DXFileEnumObject, das die Datei darstellt, in den lokalen Vorlagen Speicher des [**ID3DXFile**](id3dxfile.md) -Objekts.

Wenn ein [**ID3DXFileEnumObject**](id3dxfileenumobject.md) -Zeiger nicht verfügbar ist, sollten Sie stattdessen die [**registertemplates**](id3dxfile--registertemplates.md) -Methode aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**Register Templates**](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




