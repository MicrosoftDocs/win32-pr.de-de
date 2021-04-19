---
description: Erstellt eine Instanz eines directxfile-Objekts. Veraltet.
ms.assetid: c920d480-2557-491d-87ea-7eea1f470498
title: Directxfilecreate-Funktion (dxfile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DirectXFileCreate
api_type:
- DllExport
api_location:
- d3dxof.dll
ms.openlocfilehash: 8ee1787941bbb902e6f0f50b082867aaf2f0a8bc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363962"
---
# <a name="directxfilecreate-function"></a>Directxfilecreate-Funktion

Erstellt eine Instanz eines directxfile-Objekts. Veraltet.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDAPICALLTYPE DirectXFileCreate(
   LPDIRECTXFILE *lplpDirectXFile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lplpdirectxfile* 
</dt> <dd>

Typ: **[ **lpdirectxfile**](idirectxfile.md)\***

Adresse eines Zeigers auf eine [**idirectxfile**](idirectxfile.md) -Schnittstelle, die das erstellte directxfile-Objekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: dxfileerr \_ badzuzuweisung, dxfileerr \_ badvalue.

## <a name="remarks"></a>Bemerkungen

Nachdem Sie diese Funktion verwendet haben, verwenden Sie [**registertemplates**](idirectxfile--registertemplates.md) , um Vorlagen zu [**registrieren, und erstellen Sie ein**](idirectxfile--createenumobject.md) Enumeratorobjekt mit dem Befehl "" [**, oder erstellen Sie ein**](idirectxfile--createsaveobject.md) "Save"-Objekt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dxfile. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3dxof.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[X-Dateifunktionen](dx9-graphics-reference-x-file-functions.md)
</dt> <dt>

[**"Kreateendumuject"**](idirectxfile--createenumobject.md)
</dt> <dt>

[**"Kreatesaveobject"**](idirectxfile--createsaveobject.md)
</dt> <dt>

[**Register Templates**](idirectxfile--registertemplates.md)
</dt> </dl>

 

 




