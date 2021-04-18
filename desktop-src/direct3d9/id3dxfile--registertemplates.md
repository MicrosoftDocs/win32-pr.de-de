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
# <a name="id3dxfileregistertemplates-method"></a><span data-ttu-id="47a0b-103">ID3DXFile:: registertemplates-Methode</span><span class="sxs-lookup"><span data-stu-id="47a0b-103">ID3DXFile::RegisterTemplates method</span></span>

<span data-ttu-id="47a0b-104">Registriert benutzerdefinierte Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="47a0b-104">Registers custom templates.</span></span>

## <a name="syntax"></a><span data-ttu-id="47a0b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="47a0b-105">Syntax</span></span>


```C++
HRESULT RegisterTemplates(
  [in] LPCVOID pvData,
  [in] SIZE_T  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="47a0b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="47a0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47a0b-107">*pvData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47a0b-107">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47a0b-108">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47a0b-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47a0b-109">Ein Zeiger auf einen Puffer, der aus einer x-Datei im Text-oder Binärformat besteht, das Vorlagen enthält.</span><span class="sxs-lookup"><span data-stu-id="47a0b-109">Pointer to a buffer consisting of a .x file in text or binary format that contains templates.</span></span>

</dd> <dt>

<span data-ttu-id="47a0b-110">*CBSIZE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47a0b-110">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47a0b-111">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47a0b-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47a0b-112">Größe des Puffers, auf den pvData zeigt (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="47a0b-112">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47a0b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47a0b-113">Return value</span></span>

<span data-ttu-id="47a0b-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="47a0b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="47a0b-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="47a0b-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="47a0b-116">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DXFERR \_ badvalue, D3DXFERR Parameter \_ Error.</span><span class="sxs-lookup"><span data-stu-id="47a0b-116">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="47a0b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47a0b-117">Remarks</span></span>

<span data-ttu-id="47a0b-118">Das folgende Code Fragment stellt einen Beispiel aufzurufen von **Register Templates** und Beispiel Inhalt für den Puffer bereit, in den **pvData** verweist.</span><span class="sxs-lookup"><span data-stu-id="47a0b-118">The following code fragment provides an example call to **RegisterTemplates** And example contents for the buffer to which **pvData** points.</span></span>


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



<span data-ttu-id="47a0b-119">Alle Vorlagen müssen einen Namen und eine UUID angeben.</span><span class="sxs-lookup"><span data-stu-id="47a0b-119">All templates must specify a name and a UUID.</span></span>

<span data-ttu-id="47a0b-120">Diese Methode ruft die [**registerenumtemplates**](id3dxfile--registerenumtemplates.md) -Methode auf und erhält durch Aufrufen von [**createenumubject**](id3dxfile--createenumobject.md) mit **pvData** als ersten Parameter einen [**ID3DXFileEnumObject**](id3dxfileenumobject.md) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="47a0b-120">This method calls the [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) method, obtaining an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) interface pointer by calling [**CreateEnumObject**](id3dxfile--createenumobject.md) with **pvData** as the first parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="47a0b-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47a0b-121">Requirements</span></span>



| <span data-ttu-id="47a0b-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47a0b-122">Requirement</span></span> | <span data-ttu-id="47a0b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="47a0b-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47a0b-124">Header</span><span class="sxs-lookup"><span data-stu-id="47a0b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="47a0b-125"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="47a0b-125"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="47a0b-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="47a0b-126">Library</span></span><br/> | <dl> <span data-ttu-id="47a0b-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47a0b-127"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="47a0b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47a0b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47a0b-129">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="47a0b-129">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="47a0b-130">**Registerenumtemplates**</span><span class="sxs-lookup"><span data-stu-id="47a0b-130">**RegisterEnumTemplates**</span></span>](id3dxfile--registerenumtemplates.md)
</dt> </dl>

 

 
