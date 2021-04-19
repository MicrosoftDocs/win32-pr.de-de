---
description: Erstellt eine x-Datei und speichert die Gitter Hierarchie und die dazugehörigen Animationen darin.
ms.assetid: 803926fe-8cb7-422a-9920-56f7d0b0d0ea
title: D3DXSaveMeshHierarchyToFile-Funktion (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshHierarchyToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2de65f9bc2f9e40a5bc07c6f0b4d00112f0df21
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363134"
---
# <a name="d3dxsavemeshhierarchytofile-function"></a><span data-ttu-id="07125-103">D3DXSaveMeshHierarchyToFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="07125-103">D3DXSaveMeshHierarchyToFile function</span></span>

<span data-ttu-id="07125-104">Erstellt eine x-Datei und speichert die Gitter Hierarchie und die dazugehörigen Animationen darin.</span><span class="sxs-lookup"><span data-stu-id="07125-104">Creates a .x file and saves the mesh hierarchy and corresponding animations in it.</span></span>

## <a name="syntax"></a><span data-ttu-id="07125-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="07125-105">Syntax</span></span>


```C++
HRESULT D3DXSaveMeshHierarchyToFile(
  _In_       LPCSTR                    pFilename,
  _In_       DWORD                     XFormat,
  _In_ const D3DXFRAME                 *pFrameRoot,
  _In_       LPD3DXANIMATIONCONTROLLER pAnimController,
  _In_       LPD3DXSAVEUSERDATA        pUserDataSaver
);
```



## <a name="parameters"></a><span data-ttu-id="07125-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="07125-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07125-107">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07125-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07125-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07125-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07125-109">Ein Zeiger auf eine Zeichenfolge, die den Namen der x-Datei angibt, die das gespeicherte Mesh identifiziert.</span><span class="sxs-lookup"><span data-stu-id="07125-109">Pointer to a string that specifies the name of the .x file identifying the saved mesh.</span></span> <span data-ttu-id="07125-110">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="07125-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="07125-111">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="07125-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="07125-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="07125-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="07125-113">*Xformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07125-113">*XFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07125-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07125-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07125-115">Format der x-Datei (Text oder Binär, komprimiert oder nicht).</span><span class="sxs-lookup"><span data-stu-id="07125-115">Format of the .x file (text or binary, compressed or not).</span></span> <span data-ttu-id="07125-116">Siehe D3DXF \_ FileFormat.</span><span class="sxs-lookup"><span data-stu-id="07125-116">See D3DXF\_FILEFORMAT.</span></span> <span data-ttu-id="07125-117">Das \_ komprimierte D3DXF File Format \_ kann mithilfe eines logischen OR-Werts kombiniert werden, entweder mit dem D3DXF \_ File Format \_ binary-oder D3DXF \_ FileFormat- \_ textflags, um die Größe der Ausgabedatei zu verringern.</span><span class="sxs-lookup"><span data-stu-id="07125-117">D3DXF\_FILEFORMAT\_COMPRESSED can be combined (using a logical OR) with either the D3DXF\_FILEFORMAT\_BINARY or D3DXF\_FILEFORMAT\_TEXT flags to reduce the output file size.</span></span>

</dd> <dt>

<span data-ttu-id="07125-118">*pframeroot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07125-118">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07125-119">Typ: **Konstanten [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="07125-119">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="07125-120">Der Stamm Knoten der zu speichernden Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="07125-120">Root node of the hierarchy to be saved.</span></span> <span data-ttu-id="07125-121">Siehe [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="07125-121">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="07125-122">*panimcontroller* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07125-122">*pAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07125-123">Typ: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="07125-123">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="07125-124">Animations Controller, der Animations Sätze enthält, die gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="07125-124">Animation controller that has animation sets to be stored.</span></span> <span data-ttu-id="07125-125">Siehe [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="07125-125">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="07125-126">*puserdatasaver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07125-126">*pUserDataSaver* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07125-127">Typ: **[ **LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="07125-127">Type: **[**LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**</span></span>

<span data-ttu-id="07125-128">Von der Anwendung bereitgestellte Schnittstelle, die das Speichern von Benutzerdaten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="07125-128">Application-provided interface that allows saving of user data.</span></span> <span data-ttu-id="07125-129">Siehe [**ID3DXSaveUserData**](id3dxsaveuserdata.md).</span><span class="sxs-lookup"><span data-stu-id="07125-129">See [**ID3DXSaveUserData**](id3dxsaveuserdata.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07125-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07125-130">Return value</span></span>

<span data-ttu-id="07125-131">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="07125-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="07125-132">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="07125-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="07125-133">Wenn die Funktion fehlschlägt, kann der Rückgabewert lauten: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="07125-133">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="07125-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07125-134">Remarks</span></span>

<span data-ttu-id="07125-135">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="07125-135">The compiler setting also determines the function version.</span></span> <span data-ttu-id="07125-136">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXSaveMeshHierarchyToFileW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="07125-136">If Unicode is defined, the function call resolves to D3DXSaveMeshHierarchyToFileW.</span></span> <span data-ttu-id="07125-137">Andernfalls wird der Funktions aufrufin D3DXSaveMeshHierarchyToFileA aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="07125-137">Otherwise, the function call resolves to D3DXSaveMeshHierarchyToFileA.</span></span>

<span data-ttu-id="07125-138">Diese Funktion speichert keine komprimierten Animations Sätze.</span><span class="sxs-lookup"><span data-stu-id="07125-138">This function does not save compressed animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="07125-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07125-139">Requirements</span></span>



| <span data-ttu-id="07125-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07125-140">Requirement</span></span> | <span data-ttu-id="07125-141">Wert</span><span class="sxs-lookup"><span data-stu-id="07125-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07125-142">Header</span><span class="sxs-lookup"><span data-stu-id="07125-142">Header</span></span><br/>  | <dl> <span data-ttu-id="07125-143"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="07125-143"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="07125-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="07125-144">Library</span></span><br/> | <dl> <span data-ttu-id="07125-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07125-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="07125-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07125-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07125-147">Animations Funktionen</span><span class="sxs-lookup"><span data-stu-id="07125-147">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> <dt>

[<span data-ttu-id="07125-148">Verweis auf X-Datei</span><span class="sxs-lookup"><span data-stu-id="07125-148">X File Reference</span></span>](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 
