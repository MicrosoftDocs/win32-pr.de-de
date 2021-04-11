---
description: Ruft die GUID der Objekt Vorlage ab. Veraltet.
ms.assetid: bb4a4a32-a9e7-4caa-869d-24cfb310d8d1
title: 'Idirectxfiledata:: GetType-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 463391c661b2d166a6fba773e3b01590daf0ebd7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132377"
---
# <a name="idirectxfiledatagettype-method"></a><span data-ttu-id="48e7a-104">Idirectxfiledata:: GetType-Methode</span><span class="sxs-lookup"><span data-stu-id="48e7a-104">IDirectXFileData::GetType method</span></span>

<span data-ttu-id="48e7a-105">Ruft die GUID der Objekt Vorlage ab.</span><span class="sxs-lookup"><span data-stu-id="48e7a-105">Retrieves the GUID of the object's template.</span></span> <span data-ttu-id="48e7a-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="48e7a-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="48e7a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="48e7a-107">Syntax</span></span>


```C++
HRESULT GetType(
  [out, retval] const GUID **ppguid
);
```



## <a name="parameters"></a><span data-ttu-id="48e7a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="48e7a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48e7a-109">*ppGUID* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="48e7a-109">*ppguid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="48e7a-110">Typ: Konstante **[**GUID**](guid.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="48e7a-110">Type: **const [**GUID**](guid.md)\*\***</span></span>

<span data-ttu-id="48e7a-111">Adresse eines Zeigers, der die GUID der Objekt Vorlage empfängt.</span><span class="sxs-lookup"><span data-stu-id="48e7a-111">Address of a pointer to receive the GUID of the object's template.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48e7a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48e7a-112">Return value</span></span>

<span data-ttu-id="48e7a-113">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="48e7a-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="48e7a-114">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="48e7a-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="48e7a-115">Wenn die Methode fehlschlägt, kann der Rückgabewert dxfileerr \_ badvalue lauten.</span><span class="sxs-lookup"><span data-stu-id="48e7a-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="48e7a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48e7a-116">Requirements</span></span>



| <span data-ttu-id="48e7a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48e7a-117">Requirement</span></span> | <span data-ttu-id="48e7a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="48e7a-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48e7a-119">Header</span><span class="sxs-lookup"><span data-stu-id="48e7a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="48e7a-120"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="48e7a-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="48e7a-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="48e7a-121">Library</span></span><br/> | <dl> <span data-ttu-id="48e7a-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48e7a-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48e7a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48e7a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48e7a-124">Idirectxfiledata</span><span class="sxs-lookup"><span data-stu-id="48e7a-124">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> </dl>

 

 




