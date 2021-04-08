---
description: Erstellt ein Enumeratorobjekt. Veraltet.
ms.assetid: 9e72bb2f-143e-4690-baef-ccded21572ec
title: 'Idirectxfile:: kreatedenumuject-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3d15738b78299441fe08333a41f0652f1b4224d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762249"
---
# <a name="idirectxfilecreateenumobject-method"></a><span data-ttu-id="6841b-104">Idirectxfile:: deateeinumuject-Methode</span><span class="sxs-lookup"><span data-stu-id="6841b-104">IDirectXFile::CreateEnumObject method</span></span>

<span data-ttu-id="6841b-105">Erstellt ein Enumeratorobjekt.</span><span class="sxs-lookup"><span data-stu-id="6841b-105">Creates an enumerator object.</span></span> <span data-ttu-id="6841b-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="6841b-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="6841b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6841b-107">Syntax</span></span>


```C++
HRESULT CreateEnumObject(
  [in]          LPVOID                  pvSource,
  [in]          DXFILELOADOPTIONS       dwLoadOptions,
  [out, retval] LPDIRECTXFILEENUMOBJECT *ppEnumObj
);
```



## <a name="parameters"></a><span data-ttu-id="6841b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6841b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6841b-109">*pvsource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6841b-109">*pvSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6841b-110">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6841b-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6841b-111">Zeiger auf Daten, deren Inhalt vom Wert von dwloadoption abhängt</span><span class="sxs-lookup"><span data-stu-id="6841b-111">Pointer to data whose contents depend on the value of dwLoadOptions</span></span>

</dd> <dt>

<span data-ttu-id="6841b-112">*dwloadoption* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6841b-112">*dwLoadOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6841b-113">Typ: **[ **dxfileloadoptions**](dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="6841b-113">Type: **[**DXFILELOADOPTIONS**](dxfile.md)**</span></span>

<span data-ttu-id="6841b-114">Der-Wert, der die Quelle der Daten angibt.</span><span class="sxs-lookup"><span data-stu-id="6841b-114">Value that specifies the source of the data.</span></span> <span data-ttu-id="6841b-115">Bei diesem Wert kann es sich um eines der dxfileload \_ xxx-Flags in [dxfile-Konstanten](dxfile.md)handeln.</span><span class="sxs-lookup"><span data-stu-id="6841b-115">This value can be one of the DXFILELOAD\_xxx flags in [DXFILE Constants](dxfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="6841b-116">*ppumubj* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6841b-116">*ppEnumObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6841b-117">Typ: **[ **lpdirectxfileerumubject**](idirectxfileenumobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="6841b-117">Type: **[**LPDIRECTXFILEENUMOBJECT**](idirectxfileenumobject.md)\***</span></span>

<span data-ttu-id="6841b-118">Adresse eines Zeigers auf eine [**idirectxfileenumubject**](idirectxfileenumobject.md) -Schnittstelle, die das erstellte Enumeratorobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6841b-118">Address of a pointer to an [**IDirectXFileEnumObject**](idirectxfileenumobject.md) interface, representing the created enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6841b-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6841b-119">Return value</span></span>

<span data-ttu-id="6841b-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6841b-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6841b-121">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="6841b-121">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="6841b-122">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: dxfileerr \_ badzuweisung, dxfileerr \_ badfilefloatsize, dxfileerr \_ badfiletype, dxfileerr \_ badfileversion, dxfileerr \_ badresource, dxfileerr \_ badvalue, dxfileerr file \_ otfound, dxfileerr \_ resourcenotfound, dxfileerr \_ urlnotfound.</span><span class="sxs-lookup"><span data-stu-id="6841b-122">If the method fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADFILEFLOATSIZE, DXFILEERR\_BADFILETYPE, DXFILEERR\_BADFILEVERSION, DXFILEERR\_BADRESOURCE, DXFILEERR\_BADVALUE, DXFILEERR\_FILENOTFOUND, DXFILEERR\_RESOURCENOTFOUND, DXFILEERR\_URLNOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="6841b-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6841b-123">Remarks</span></span>

<span data-ttu-id="6841b-124">Nachdem Sie diese Methode verwendet haben, verwenden Sie eine der idirectxfileenumubject-Methoden, um ein Datenobjekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6841b-124">After using this method, use one of the IDirectXFileEnumObject methods to retrieve a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="6841b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6841b-125">Requirements</span></span>



| <span data-ttu-id="6841b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6841b-126">Requirement</span></span> | <span data-ttu-id="6841b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="6841b-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6841b-128">Header</span><span class="sxs-lookup"><span data-stu-id="6841b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="6841b-129"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="6841b-129"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="6841b-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6841b-130">Library</span></span><br/> | <dl> <span data-ttu-id="6841b-131"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6841b-131"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6841b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6841b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6841b-133">Idirectxfile</span><span class="sxs-lookup"><span data-stu-id="6841b-133">IDirectXFile</span></span>](idirectxfile.md)
</dt> </dl>

 

 
