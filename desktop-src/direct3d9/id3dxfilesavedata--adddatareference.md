---
description: Fügt einen Daten Verweis als untergeordnetes Element dieses ID3DXFileSaveData File Data-Knotens hinzu. Der Daten Verweis verweist auf ein Datei Datenobjekt.
ms.assetid: 75bfe91e-15ea-41f3-b1f7-071fb7f0093f
title: 'ID3DXFileSaveData:: adddatareferenzierungsmethode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataReference
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f4aabf5601ef73f4e1062b1db1a28c1f0deae5fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961656"
---
# <a name="id3dxfilesavedataadddatareference-method"></a><span data-ttu-id="d87cb-104">ID3DXFileSaveData:: adddatareferenzierungsmethode</span><span class="sxs-lookup"><span data-stu-id="d87cb-104">ID3DXFileSaveData::AddDataReference method</span></span>

<span data-ttu-id="d87cb-105">Fügt einen Daten Verweis als untergeordnetes Element dieses [**ID3DXFileSaveData**](id3dxfilesavedata.md) File Data-Knotens hinzu.</span><span class="sxs-lookup"><span data-stu-id="d87cb-105">Adds a data reference as a child of this [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span> <span data-ttu-id="d87cb-106">Der Daten Verweis verweist auf ein Datei Datenobjekt.</span><span class="sxs-lookup"><span data-stu-id="d87cb-106">The data reference points to a file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d87cb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d87cb-107">Syntax</span></span>


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szName,
  [in] const GUID   *pId
);
```



## <a name="parameters"></a><span data-ttu-id="d87cb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d87cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d87cb-109">*szName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d87cb-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d87cb-110">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d87cb-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d87cb-111">Ein Zeiger auf den Namen des Datenobjekts, das als Verweis hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d87cb-111">Pointer to the name of the data object to add by reference.</span></span> <span data-ttu-id="d87cb-112">Geben Sie **null** an, wenn das Datenobjekt keinen Namen hat.</span><span class="sxs-lookup"><span data-stu-id="d87cb-112">Specify **NULL** if the data object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="d87cb-113">*pId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d87cb-113">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d87cb-114">Typ: Konstante **[**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="d87cb-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="d87cb-115">Zeiger auf eine GUID, die das Datenobjekt darstellt, das als Verweis hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d87cb-115">Pointer to a GUID representing the data object to add by reference.</span></span> <span data-ttu-id="d87cb-116">Wenn der Wert **null** ist, wird ein Verweis hinzugefügt, der auf das Datenobjekt mit dem Namen verweist, der von szName angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d87cb-116">If **NULL**, a reference will be added that points to the data object with the name given by szName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d87cb-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d87cb-117">Return value</span></span>

<span data-ttu-id="d87cb-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d87cb-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d87cb-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d87cb-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d87cb-120">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DXFERR \_ badobject, D3DXFERR \_ badvalue, E \_ oudebmemory.</span><span class="sxs-lookup"><span data-stu-id="d87cb-120">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d87cb-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d87cb-121">Remarks</span></span>

<span data-ttu-id="d87cb-122">Das Datei Datenobjekt, auf das verwiesen wird, muss entweder einen Namen oder eine GUID aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d87cb-122">The file data object being referenced must have either a name or a GUID.</span></span> <span data-ttu-id="d87cb-123">Das Datei Datenobjekt muss auch von einem anderen übergeordneten [**ID3DXFileSaveData**](id3dxfilesavedata.md) -Objekt abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="d87cb-123">The file data object must also derive from a different parent [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d87cb-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d87cb-124">Requirements</span></span>



| <span data-ttu-id="d87cb-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d87cb-125">Requirement</span></span> | <span data-ttu-id="d87cb-126">Wert</span><span class="sxs-lookup"><span data-stu-id="d87cb-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d87cb-127">Header</span><span class="sxs-lookup"><span data-stu-id="d87cb-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d87cb-128"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="d87cb-128"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="d87cb-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d87cb-129">Library</span></span><br/> | <dl> <span data-ttu-id="d87cb-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d87cb-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d87cb-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d87cb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d87cb-132">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="d87cb-132">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 
