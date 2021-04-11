---
description: Erstellt eine Instanz eines ID3DXFile-Objekts.
ms.assetid: c086cb66-b1dc-4180-b966-e9a3b1f36f22
title: D3DXFileCreate-Funktion (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFileCreate
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 36fd57d15257323e86c0068709c3c73662eb0658
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132341"
---
# <a name="d3dxfilecreate-function"></a>D3DXFileCreate-Funktion

Erstellt eine Instanz eines [**ID3DXFile**](id3dxfile.md) -Objekts.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDAPICALLTYPE D3DXFileCreate(
   ID3DXFile **lplpDirectXFile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lplpdirectxfile* 
</dt> <dd>

Typ: **[ **ID3DXFile**](id3dxfile.md)\*\***

Adresse eines Zeigers auf eine [**ID3DXFile**](id3dxfile.md) -Schnittstelle, die das erstellte x-Datei Objekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: e- \_ Zeiger, e-Ausgabe \_ Speicher.

## <a name="remarks"></a>Bemerkungen

Nachdem Sie diese Funktion verwendet haben, verwenden Sie registertemplates oder registerenumtemplates, um Vorlagen zu [**registrieren, erstellen**](id3dxfile--createenumobject.md) Sie ein Enumeratorobjekt mithilfe von " [**registertemplates**](id3dxfile--registertemplates.md) " oder " [**registerenumtemplates**](id3dxfile--registerenumtemplates.md) " [**, oder erstellen**](id3dxfile--createsaveobject.md) Sie ein "Save"-Objekt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX X-Dateifunktionen](dx9-graphics-reference-d3dx-x-file-functions.md)
</dt> <dt>

[**"Kreateendumuject"**](id3dxfile--createenumobject.md)
</dt> <dt>

[**"Kreatesaveobject"**](id3dxfile--createsaveobject.md)
</dt> <dt>

[**Registerenumtemplates**](id3dxfile--registerenumtemplates.md)
</dt> <dt>

[**Register Templates**](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




