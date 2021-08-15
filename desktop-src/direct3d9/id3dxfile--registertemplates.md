---
description: Registriert benutzerdefinierte Vorlagen.
ms.assetid: e142a0f2-d0ef-4479-82cd-ba8d5059d1d2
title: ID3DXFile::RegisterTemplates-Methode (D3DX9Xof.h)
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
ms.openlocfilehash: b6dba0b79b7a7baaa6a05daf0b30609a129e76ab80529289a48b9b379426f33c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520785"
---
# <a name="id3dxfileregistertemplates-method"></a>ID3DXFile::RegisterTemplates-Methode

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

*pvData* \[ In\]
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Zeiger auf einen Puffer, der aus einer X-Datei im Text- oder Binärformat besteht, die Vorlagen enthält.

</dd> <dt>

*cbSize* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Größe des Puffers, auf den pvData zeigt, in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.

## <a name="remarks"></a>Hinweise

Das folgende Codefragment enthält einen Beispielaufruf von **RegisterTemplates** und Beispielinhalten für den Puffer, auf **den pvData** zeigt.


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

Diese Methode ruft die [**RegisterEnumTemplates-Methode**](id3dxfile--registerenumtemplates.md) auf und ruft einen [**ID3DXFileEnumObject-Schnittstellenzeiger**](id3dxfileenumobject.md) durch Aufrufen von [**CreateEnumObject**](id3dxfile--createenumobject.md) mit **pvData** als ersten Parameter ab.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md)
</dt> </dl>

 

 
