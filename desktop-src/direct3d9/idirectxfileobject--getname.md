---
description: Ruft einen Zeiger auf den Namen eines DirectX-Datei Objekts ab. Veraltet.
ms.assetid: feb3faa2-22b9-47ed-8a38-33092821d484
title: 'Idirectxfileobject:: GetName-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 134a1ce61ed1dc0d98a4daf3ba80dd4b0976c372
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367361"
---
# <a name="idirectxfileobjectgetname-method"></a><span data-ttu-id="bad77-104">Idirectxfileobject:: GetName-Methode</span><span class="sxs-lookup"><span data-stu-id="bad77-104">IDirectXFileObject::GetName method</span></span>

<span data-ttu-id="bad77-105">Ruft einen Zeiger auf den Namen eines DirectX-Datei Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="bad77-105">Retrieves a pointer to a DirectX file object's name.</span></span> <span data-ttu-id="bad77-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="bad77-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="bad77-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bad77-107">Syntax</span></span>


```C++
HRESULT GetName(
  [out]     LPSTR   pstrNameBuf,
  [in, out] LPDWORD pdwBufLen
);
```



## <a name="parameters"></a><span data-ttu-id="bad77-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bad77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bad77-109">*pstrinnamebuf* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bad77-109">*pstrNameBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bad77-110">Typ: **[ **LPSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bad77-110">Type: **[**LPSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bad77-111">Zeiger auf den Puffer, in den der Name des DirectX-Datei Objekts kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="bad77-111">Pointer to the buffer in which the DirectX file object's name will be copied.</span></span> <span data-ttu-id="bad77-112">Legen Sie diesen Wert auf **null** fest, wenn nur die Pufferlänge benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="bad77-112">Set to **NULL** if only the buffer length is needed.</span></span>

</dd> <dt>

<span data-ttu-id="bad77-113">*pdwbuschlen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bad77-113">*pdwBufLen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bad77-114">Typ: **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bad77-114">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bad77-115">Ein Zeiger auf ein DWORD, das die Länge des Puffers angibt, auf den pstrinnamebuf zeigt.</span><span class="sxs-lookup"><span data-stu-id="bad77-115">Pointer to a DWORD specifying the length of the buffer pointed to by pstrNameBuf.</span></span> <span data-ttu-id="bad77-116">Der Wert des pdwbuflen-Parameters wird in die Pufferlänge geändert, die für den Namen des Objekts erforderlich ist, auch wenn pstrinnamebuf **null** ist.</span><span class="sxs-lookup"><span data-stu-id="bad77-116">The pdwBufLen parameter value will be modified to the buffer length needed to hold the object's name even if pstrNameBuf is **NULL**.</span></span> <span data-ttu-id="bad77-117">In beiden Fällen gibt die Funktion dxfileerr \_ badvalue zurück, wenn der ursprüngliche Wert von pdwbuflen nicht so groß wie die Länge ist, die zum Speichern des Objekt namens benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="bad77-117">In either case, the function will return DXFILEERR\_BADVALUE if the original value of pdwBufLen is not as large as or larger than the length needed to hold the object's name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bad77-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bad77-118">Return value</span></span>

<span data-ttu-id="bad77-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bad77-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bad77-120">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="bad77-120">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="bad77-121">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein. dxfileerr \_ badzuweisung dxfileerr \_ badvalue</span><span class="sxs-lookup"><span data-stu-id="bad77-121">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="bad77-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bad77-122">Requirements</span></span>



| <span data-ttu-id="bad77-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bad77-123">Requirement</span></span> | <span data-ttu-id="bad77-124">Wert</span><span class="sxs-lookup"><span data-stu-id="bad77-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bad77-125">Header</span><span class="sxs-lookup"><span data-stu-id="bad77-125">Header</span></span><br/>  | <dl> <span data-ttu-id="bad77-126"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="bad77-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="bad77-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bad77-127">Library</span></span><br/> | <dl> <span data-ttu-id="bad77-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bad77-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bad77-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bad77-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bad77-130">Idirectxfileobject</span><span class="sxs-lookup"><span data-stu-id="bad77-130">IDirectXFileObject</span></span>](idirectxfileobject.md)
</dt> </dl>

 

 
