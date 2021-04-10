---
description: Ruft den Multipurpose Internet Mail Extensions (MIME)-Typ für die Binärdaten ab. Veraltet.
ms.assetid: 57c42ace-4313-40d8-9992-eaf12edf3a30
title: 'Idirectxfilebinary:: getmimetype-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetMimeType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 965006dc6fbad1176307341a19fd1f186e670104
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961588"
---
# <a name="idirectxfilebinarygetmimetype-method"></a><span data-ttu-id="07636-104">Idirectxfilebinary:: getmimetype-Methode</span><span class="sxs-lookup"><span data-stu-id="07636-104">IDirectXFileBinary::GetMimeType method</span></span>

<span data-ttu-id="07636-105">Ruft den Multipurpose Internet Mail Extensions (MIME)-Typ für die Binärdaten ab.</span><span class="sxs-lookup"><span data-stu-id="07636-105">Retrieves the Multipurpose Internet Mail Extensions (MIME) type for the binary data.</span></span> <span data-ttu-id="07636-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="07636-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="07636-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="07636-107">Syntax</span></span>


```C++
HRESULT GetMimeType(
  [out] LPCSTR *pszMimeType
);
```



## <a name="parameters"></a><span data-ttu-id="07636-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="07636-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07636-109">*pszmimetype* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="07636-109">*pszMimeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07636-110">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="07636-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="07636-111">Adresse eines Zeigers, der die MIME-Typzeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="07636-111">Address of a pointer to receive the MIME type string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07636-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07636-112">Return value</span></span>

<span data-ttu-id="07636-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="07636-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="07636-114">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="07636-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="07636-115">Wenn die Methode fehlschlägt, kann der Rückgabewert dxfileerr \_ badvalue lauten.</span><span class="sxs-lookup"><span data-stu-id="07636-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="07636-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07636-116">Remarks</span></span>

<span data-ttu-id="07636-117">Wenn kein MIME-Typ in einer DirectX-Datei für ein binäres Objekt angegeben ist, legt die Funktion pszmimetype auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="07636-117">When there is no MIME type specified in a DirectX file for a binary object, the function will set pszMimeType to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="07636-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07636-118">Requirements</span></span>



| <span data-ttu-id="07636-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07636-119">Requirement</span></span> | <span data-ttu-id="07636-120">Wert</span><span class="sxs-lookup"><span data-stu-id="07636-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07636-121">Header</span><span class="sxs-lookup"><span data-stu-id="07636-121">Header</span></span><br/>  | <dl> <span data-ttu-id="07636-122"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="07636-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="07636-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="07636-123">Library</span></span><br/> | <dl> <span data-ttu-id="07636-124"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07636-124"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07636-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07636-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07636-126">Idirectxfilebinary</span><span class="sxs-lookup"><span data-stu-id="07636-126">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
