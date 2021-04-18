---
description: Greift auf die x-Datei Daten zu.
ms.assetid: 0e92914b-47b3-4a88-87ba-ce3c14282dbb
title: 'ID3DXFileData:: Lock-Methode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Lock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 27ef18fcb12b00f0b778ee15d582610ffe52fe54
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371925"
---
# <a name="id3dxfiledatalock-method"></a><span data-ttu-id="63172-103">ID3DXFileData:: Lock-Methode</span><span class="sxs-lookup"><span data-stu-id="63172-103">ID3DXFileData::Lock method</span></span>

<span data-ttu-id="63172-104">Greift auf die x-Datei Daten zu.</span><span class="sxs-lookup"><span data-stu-id="63172-104">Accesses the .x file data.</span></span>

## <a name="syntax"></a><span data-ttu-id="63172-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="63172-105">Syntax</span></span>


```C++
HRESULT Lock(
  [in]       SIZE_T *pSize,
  [in] const VOID   **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="63172-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="63172-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63172-107">*Psize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63172-107">*pSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63172-108">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="63172-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="63172-109">Ein Zeiger auf die Größe der x-Datei Daten.</span><span class="sxs-lookup"><span data-stu-id="63172-109">Pointer to the size of the .x file data.</span></span>

</dd> <dt>

<span data-ttu-id="63172-110">*ppData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63172-110">*ppData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63172-111">Typ: Konstante **void \* \***</span><span class="sxs-lookup"><span data-stu-id="63172-111">Type: **const VOID\*\***</span></span>

<span data-ttu-id="63172-112">Adresse eines Zeigers, mit dem der Schnittstellen Zeiger des [**ID3DXFileData**](id3dxfiledata.md) -Datei Datenobjekts empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="63172-112">Address of a pointer to receive the [**ID3DXFileData**](id3dxfiledata.md) file data object's interface pointer.</span></span> <span data-ttu-id="63172-113">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="63172-113">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63172-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63172-114">Return value</span></span>

<span data-ttu-id="63172-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="63172-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="63172-116">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="63172-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="63172-117">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DXFERR \_ badvalue.</span><span class="sxs-lookup"><span data-stu-id="63172-117">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="63172-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63172-118">Remarks</span></span>

<span data-ttu-id="63172-119">Der *ppData* -Zeiger ist nur während der **ID3DXFileData:: Lock** ... [**ID3DXFileData:: Unlock**](id3dxfiledata--unlock.md) -Sequenz.</span><span class="sxs-lookup"><span data-stu-id="63172-119">The *ppData* pointer is only valid during a **ID3DXFileData::Lock** ... [**ID3DXFileData::Unlock**](id3dxfiledata--unlock.md) sequence.</span></span> <span data-ttu-id="63172-120">Sie können mehrere Sperr Aufrufe durchführen.</span><span class="sxs-lookup"><span data-stu-id="63172-120">You can make multiple lock calls.</span></span> <span data-ttu-id="63172-121">Sie müssen jedoch sicherstellen, dass die Anzahl der Sperr Aufrufe mit der Anzahl der entsperrungs Aufrufe übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="63172-121">However, you must ensure that the number of lock calls matches the number of unlock calls.</span></span>

<span data-ttu-id="63172-122">Da es nicht garantiert wird, dass Datei Daten ordnungsgemäß mit Byte-Begrenzungen ausgerichtet werden, sollten Sie mit nicht ausgerichteten Zeigern auf *ppData* zugreifen.</span><span class="sxs-lookup"><span data-stu-id="63172-122">Because file data is not guaranteed to be aligned properly with byte boundaries, you should access *ppData* with UNALIGNED pointers.</span></span>

<span data-ttu-id="63172-123">Die Rückgabe von Parameterwerten ist aufgrund einer möglichen Datei Beschädigung nicht garantiert. Daher sollte der Code die zurückgegebenen Parameterwerte überprüfen.</span><span class="sxs-lookup"><span data-stu-id="63172-123">Returned parameter values are not guaranteed to be valid due to possible file corruption; therefore, your code should verify the returned parameter values.</span></span>

## <a name="requirements"></a><span data-ttu-id="63172-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63172-124">Requirements</span></span>



| <span data-ttu-id="63172-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63172-125">Requirement</span></span> | <span data-ttu-id="63172-126">Wert</span><span class="sxs-lookup"><span data-stu-id="63172-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63172-127">Header</span><span class="sxs-lookup"><span data-stu-id="63172-127">Header</span></span><br/>  | <dl> <span data-ttu-id="63172-128"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="63172-128"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="63172-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="63172-129">Library</span></span><br/> | <dl> <span data-ttu-id="63172-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63172-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="63172-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63172-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63172-132">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="63172-132">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
