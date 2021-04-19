---
description: Erstellt ein Enumeratorobjekt, das eine x-Datei liest.
ms.assetid: 86d05eab-601c-4beb-9dbe-c23fa524871c
title: 'ID3DXFile:: kreateendumuject-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a58a3341bacf9b323cc5753f8e9e51c4b703b966
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367383"
---
# <a name="id3dxfilecreateenumobject-method"></a><span data-ttu-id="93c14-103">ID3DXFile:: kreateendumuject-Methode</span><span class="sxs-lookup"><span data-stu-id="93c14-103">ID3DXFile::CreateEnumObject method</span></span>

<span data-ttu-id="93c14-104">Erstellt ein Enumeratorobjekt, das eine x-Datei liest.</span><span class="sxs-lookup"><span data-stu-id="93c14-104">Creates an enumerator object that will read a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="93c14-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="93c14-105">Syntax</span></span>


```C++
HRESULT CreateEnumObject(
  [out] LPCVOID               pvSource,
  [in]  D3DXF_FILELOADOPTIONS loadflags,
  [out] ID3DXFileEnumObject   **ppEnumObj
);
```



## <a name="parameters"></a><span data-ttu-id="93c14-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="93c14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93c14-107">*pvsource* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="93c14-107">*pvSource* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93c14-108">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93c14-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93c14-109">Die Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="93c14-109">The data source.</span></span> <span data-ttu-id="93c14-110">Entweder:</span><span class="sxs-lookup"><span data-stu-id="93c14-110">Either:</span></span>

-   <span data-ttu-id="93c14-111">Ein Dateiname</span><span class="sxs-lookup"><span data-stu-id="93c14-111">A file name</span></span>
-   <span data-ttu-id="93c14-112">Eine [**D3DXF \_ fileloadmemory**](d3dxf-fileloadmemory.md) -Struktur</span><span class="sxs-lookup"><span data-stu-id="93c14-112">A [**D3DXF\_FILELOADMEMORY**](d3dxf-fileloadmemory.md) structure</span></span>
-   <span data-ttu-id="93c14-113">Eine [**D3DXF \_ fileloadresource**](d3dxf-fileloadresource.md) -Struktur</span><span class="sxs-lookup"><span data-stu-id="93c14-113">A [**D3DXF\_FILELOADRESOURCE**](d3dxf-fileloadresource.md) structure</span></span>

<span data-ttu-id="93c14-114">Abhängig vom Wert von loadflags.</span><span class="sxs-lookup"><span data-stu-id="93c14-114">Depending on the value of loadflags.</span></span>

</dd> <dt>

<span data-ttu-id="93c14-115">*loadflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93c14-115">*loadflags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93c14-116">Typ: **[D3DXF \_ fileloadoption](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="93c14-116">Type: **[D3DXF\_FILELOADOPTIONS](d3dxf.md)**</span></span>

<span data-ttu-id="93c14-117">Der-Wert, der die Quelle der Daten angibt.</span><span class="sxs-lookup"><span data-stu-id="93c14-117">Value that specifies the source of the data.</span></span> <span data-ttu-id="93c14-118">Bei diesem Wert kann es sich um eines der [D3DXF \_ fileloadoptions](d3dxf.md) -Flags handeln.</span><span class="sxs-lookup"><span data-stu-id="93c14-118">This value can be one of the [D3DXF\_FILELOADOPTIONS](d3dxf.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="93c14-119">*ppumubj* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="93c14-119">*ppEnumObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93c14-120">Typ: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="93c14-120">Type: **[**ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***</span></span>

<span data-ttu-id="93c14-121">Adresse eines Zeigers auf eine [**ID3DXFileEnumObject**](id3dxfileenumobject.md) -Schnittstelle, die das erstellte Enumeratorobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="93c14-121">Address of a pointer to an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) interface, representing the created enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93c14-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93c14-122">Return value</span></span>

<span data-ttu-id="93c14-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="93c14-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="93c14-124">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="93c14-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="93c14-125">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DXFERR \_ badvalue, D3DXFERR Parameter \_ Error.</span><span class="sxs-lookup"><span data-stu-id="93c14-125">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="93c14-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93c14-126">Remarks</span></span>

<span data-ttu-id="93c14-127">Verwenden Sie nach der Verwendung dieser Methode eine der [**ID3DXFileEnumObject**](id3dxfileenumobject.md) -Methoden, um ein Datenobjekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="93c14-127">After using this method, use one of the [**ID3DXFileEnumObject**](id3dxfileenumobject.md) methods to retrieve a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="93c14-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93c14-128">Requirements</span></span>



| <span data-ttu-id="93c14-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93c14-129">Requirement</span></span> | <span data-ttu-id="93c14-130">Wert</span><span class="sxs-lookup"><span data-stu-id="93c14-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93c14-131">Header</span><span class="sxs-lookup"><span data-stu-id="93c14-131">Header</span></span><br/>  | <dl> <span data-ttu-id="93c14-132"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="93c14-132"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="93c14-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="93c14-133">Library</span></span><br/> | <dl> <span data-ttu-id="93c14-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93c14-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="93c14-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93c14-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93c14-136">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="93c14-136">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="93c14-137">**ID3DXFileEnumObject**</span><span class="sxs-lookup"><span data-stu-id="93c14-137">**ID3DXFileEnumObject**</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 
