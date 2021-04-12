---
description: Erstellt ein binäres Objekt und fügt es als untergeordnetes Objekt hinzu. Veraltet.
ms.assetid: 6164951d-dd87-4318-ac08-b97c22f58d45
title: 'Idirectxfiledata:: addbinaryobject-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddBinaryObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 8373b9c4328a8683f32c1fe7ab979cb8d7636f87
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219443"
---
# <a name="idirectxfiledataaddbinaryobject-method"></a><span data-ttu-id="c5f3f-104">Idirectxfiledata:: addbinaryobject-Methode</span><span class="sxs-lookup"><span data-stu-id="c5f3f-104">IDirectXFileData::AddBinaryObject method</span></span>

<span data-ttu-id="c5f3f-105">Erstellt ein binäres Objekt und fügt es als untergeordnetes Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="c5f3f-105">Creates a binary object and adds it as a child object.</span></span> <span data-ttu-id="c5f3f-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c5f3f-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5f3f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5f3f-107">Syntax</span></span>


```C++
HRESULT AddBinaryObject(
  [in]       LPCSTR szName,
  [in] const GUID   *pguid,
  [in]       LPCSTR szMimeType,
  [in]       LPVOID pvData,
  [in]       DWORD  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="c5f3f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5f3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5f3f-109">*szName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5f3f-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f3f-110">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5f3f-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5f3f-111">Zeiger auf den Namen des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c5f3f-111">Pointer to the name of the object.</span></span> <span data-ttu-id="c5f3f-112">Geben Sie **null** an, wenn für das Objekt kein Name erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c5f3f-112">Specify **NULL** if the object does not need a name.</span></span>

</dd> <dt>

<span data-ttu-id="c5f3f-113">*pguid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5f3f-113">*pguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f3f-114">Typ: Konstante **[**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="c5f3f-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="c5f3f-115">Ein Zeiger auf die GUID, die das Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c5f3f-115">Pointer to the GUID representing the object.</span></span> <span data-ttu-id="c5f3f-116">Geben Sie **null** an, wenn das Objekt keine GUID benötigt.</span><span class="sxs-lookup"><span data-stu-id="c5f3f-116">Specify **NULL** if the object does not need a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="c5f3f-117">*szmimetype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5f3f-117">*szMimeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f3f-118">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5f3f-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5f3f-119">Zeiger auf den MIME-Typ des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c5f3f-119">Pointer to the object's MIME type.</span></span>

</dd> <dt>

<span data-ttu-id="c5f3f-120">*pvData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5f3f-120">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f3f-121">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5f3f-121">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5f3f-122">Zeiger auf die Daten des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c5f3f-122">Pointer to the object's data.</span></span>

</dd> <dt>

<span data-ttu-id="c5f3f-123">*CBSIZE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5f3f-123">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f3f-124">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5f3f-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5f3f-125">Größe des Puffers, auf den pvData zeigt (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="c5f3f-125">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5f3f-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5f3f-126">Return value</span></span>

<span data-ttu-id="c5f3f-127">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5f3f-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5f3f-128">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="c5f3f-128">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="c5f3f-129">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein. dxfileerr \_ badzuweisung dxfileerr \_ badvalue</span><span class="sxs-lookup"><span data-stu-id="c5f3f-129">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="c5f3f-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5f3f-130">Requirements</span></span>



| <span data-ttu-id="c5f3f-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5f3f-131">Requirement</span></span> | <span data-ttu-id="c5f3f-132">Wert</span><span class="sxs-lookup"><span data-stu-id="c5f3f-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5f3f-133">Header</span><span class="sxs-lookup"><span data-stu-id="c5f3f-133">Header</span></span><br/>  | <dl> <span data-ttu-id="c5f3f-134"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5f3f-134"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5f3f-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c5f3f-135">Library</span></span><br/> | <dl> <span data-ttu-id="c5f3f-136"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5f3f-136"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5f3f-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5f3f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5f3f-138">Idirectxfiledata</span><span class="sxs-lookup"><span data-stu-id="c5f3f-138">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="c5f3f-139">**Idirectxfilebinary:: getmimetype**</span><span class="sxs-lookup"><span data-stu-id="c5f3f-139">**IDirectXFileBinary::GetMimeType**</span></span>](idirectxfilebinary--getmimetype.md)
</dt> </dl>

 

 
