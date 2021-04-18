---
description: Registriert benutzerdefinierte Vorlagen.
ms.assetid: e142a0f2-d0ef-4479-82cd-ba8d5059d1d2
title: 'ID3DXFile:: registertemplates-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7864b63d55ba219c5076920acc809f824bc1820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361220"
---
# <a name="id3dxfileregistertemplates-method"></a>ID3DXFile:: registertemplates-Methode

Registriert benutzerdefinierte Vorlagen.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterTemplates(
  [in] LPCVOID pvData,
  [in] SIZE_T  cbSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvData* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**

Ein Zeiger auf einen Puffer, der aus einer x-Datei im Text-oder Binärformat besteht, das Vorlagen enthält.

</dd> <dt>

*CBSIZE* \[ in\]
</dt> <dd>

Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**

Größe des Puffers, auf den pvData zeigt (in Bytes).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DXFERR \_ badvalue, D3DXFERR Parameter \_ Error.

## <a name="remarks"></a>Bemerkungen

Das folgende Code Fragment stellt einen Beispiel aufzurufen von **Register Templates** und Beispiel Inhalt für den Puffer bereit, in den **pvData** verweist.


```
#define XSKINEXP_TEMPLATES \
    "xof 0303txt 0032\
    template XSkinMeshHeader \
    { \
        <3CF169CE-FF7C-44ab-93C0-F78F62D172E2> \
        WORD nMaxSkinWeightsPerVertex; \
        WORD nMaxSkinWeightsPerFace; \
        WORD nBones; \
    } \
    template VertexDuplicationIndices \
    { \
        <B8D65549-D7C9-4995-89CF-53A9A8B031E3> \
        DWORD nIndices; \
        DWORD nOriginalVertices; \
        array DWORD indices[nIndices]; \
    } \
    template SkinWeights \
    { \
        <6F0D123B-BAD2-4167-A0D0-80224F25FABB> \
        STRING transformNodeName;\
        DWORD nWeights; \
        array DWORD vertexIndices[nWeights]; \
        array float weights[nWeights]; \
        Matrix4x4 matrixOffset; \
    }"
.
.
.
        
LPD3DXFILE pD3DXFile = NULL;

if ( FAILED 
        (hr = pD3DXFile->RegisterTemplates( 
            (LPVOID)XSKINEXP_TEMPLATES,
            sizeof( XSKINEXP_TEMPLATES ) - 1 ) ) )
goto End;
```



Alle Vorlagen müssen einen Namen und eine UUID angeben.

Diese Methode ruft die [**registerenumtemplates**](id3dxfile--registerenumtemplates.md) -Methode auf und erhält durch Aufrufen von [**createenumubject**](id3dxfile--createenumobject.md) mit **pvData** als ersten Parameter einen [**ID3DXFileEnumObject**](id3dxfileenumobject.md) -Schnittstellen Zeiger.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**Registerenumtemplates**](id3dxfile--registerenumtemplates.md)
</dt> </dl>

 

 
