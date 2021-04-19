---
description: Ruft die Daten für eines der Member des Objekts oder die Daten für alle Elemente ab. Veraltet.
ms.assetid: 2a227705-371e-41f1-af5d-20e652cd07f6
title: 'Idirectxfiledata:: GetData-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: ed52aaf0b4c740b675129c81843c0bd49c7f428e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350711"
---
# <a name="idirectxfiledatagetdata-method"></a><span data-ttu-id="85d58-104">Idirectxfiledata:: GetData-Methode</span><span class="sxs-lookup"><span data-stu-id="85d58-104">IDirectXFileData::GetData method</span></span>

<span data-ttu-id="85d58-105">Ruft die Daten für eines der Member des Objekts oder die Daten für alle Elemente ab.</span><span class="sxs-lookup"><span data-stu-id="85d58-105">Retrieves the data for one of the object's members or the data for all members.</span></span> <span data-ttu-id="85d58-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="85d58-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="85d58-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="85d58-107">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  LPCSTR szMember,
  [out] DWORD  *pcbSize,
  [out] void   **ppvData
);
```



## <a name="parameters"></a><span data-ttu-id="85d58-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="85d58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85d58-109">*szMember* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85d58-109">*szMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85d58-110">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85d58-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85d58-111">Zeiger auf den Namen des Members, für den die Daten abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="85d58-111">Pointer to the name of the member for which to retrieve data.</span></span> <span data-ttu-id="85d58-112">Geben Sie **null** an, um alle erforderlichen Elementdaten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="85d58-112">Specify **NULL** to retrieve all required members' data.</span></span>

</dd> <dt>

<span data-ttu-id="85d58-113">*pcbSize* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="85d58-113">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85d58-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="85d58-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="85d58-115">Zeiger zum Empfangen der ppvData-Puffergröße in Bytes.</span><span class="sxs-lookup"><span data-stu-id="85d58-115">Pointer to receive the ppvData buffer size, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="85d58-116">*ppvData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="85d58-116">*ppvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85d58-117">Typ: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="85d58-117">Type: **void\*\***</span></span>

<span data-ttu-id="85d58-118">Adresse eines Zeigers auf den Puffer, der die mit "szMember" verknüpften Daten empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="85d58-118">Address of a pointer to the buffer to receive the data associated with szMember.</span></span> <span data-ttu-id="85d58-119">Wenn szMember den Wert **null** hat, wird ppvData so festgelegt, dass es auf einen Puffer verweist, der alle erforderlichen Elementdaten in einem zusammenhängenden Speicherblock enthält.</span><span class="sxs-lookup"><span data-stu-id="85d58-119">If szMember is **NULL**, ppvData is set to point to a buffer containing all required members' data in a contiguous block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85d58-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85d58-120">Return value</span></span>

<span data-ttu-id="85d58-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="85d58-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="85d58-122">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="85d58-122">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="85d58-123">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: dxfileerr \_ badarraysize, dxfileerr \_ baddatareferenzierung, dxfileerr \_ badvalue.</span><span class="sxs-lookup"><span data-stu-id="85d58-123">If the method fails, the return value can be one of the following values: DXFILEERR\_BADARRAYSIZE, DXFILEERR\_BADDataReference, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="85d58-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85d58-124">Remarks</span></span>

<span data-ttu-id="85d58-125">Diese Methode ruft die Daten für erforderliche Member eines Datenobjekts ab, aber keine Daten für optionale (untergeordnete) Member.</span><span class="sxs-lookup"><span data-stu-id="85d58-125">This method retrieves the data for required members of a data object but no data for optional (child) members.</span></span> <span data-ttu-id="85d58-126">Verwenden Sie [**idirectxfiledata:: getnextobject**](idirectxfiledata--getnextobject.md) zum Abrufen von untergeordneten Objekten.</span><span class="sxs-lookup"><span data-stu-id="85d58-126">Use [**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md) to retrieve child objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="85d58-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85d58-127">Requirements</span></span>



| <span data-ttu-id="85d58-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85d58-128">Requirement</span></span> | <span data-ttu-id="85d58-129">Wert</span><span class="sxs-lookup"><span data-stu-id="85d58-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85d58-130">Header</span><span class="sxs-lookup"><span data-stu-id="85d58-130">Header</span></span><br/>  | <dl> <span data-ttu-id="85d58-131"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="85d58-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="85d58-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="85d58-132">Library</span></span><br/> | <dl> <span data-ttu-id="85d58-133"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85d58-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85d58-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85d58-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85d58-135">Idirectxfiledata</span><span class="sxs-lookup"><span data-stu-id="85d58-135">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="85d58-136">**Idirectxfiledata:: getnextobject**</span><span class="sxs-lookup"><span data-stu-id="85d58-136">**IDirectXFileData::GetNextObject**</span></span>](idirectxfiledata--getnextobject.md)
</dt> </dl>

 

 
