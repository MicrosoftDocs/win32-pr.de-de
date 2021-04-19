---
description: Ruft einen Zeiger auf die GUID ab, mit der ein DirectX-Datei Objekt identifiziert wird. Veraltet.
ms.assetid: 74c7a1d9-85e4-43eb-bcd8-1f3ddd713e9f
title: 'Idirectxfileobject:: GetId-Methode (dxfile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetId
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 336dbde487ecd1b3af7b32d3743f037c235952f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355177"
---
# <a name="idirectxfileobjectgetid-method"></a><span data-ttu-id="df47a-104">Idirectxfileobject:: GetId-Methode</span><span class="sxs-lookup"><span data-stu-id="df47a-104">IDirectXFileObject::GetId method</span></span>

<span data-ttu-id="df47a-105">Ruft einen Zeiger auf die GUID ab, mit der ein DirectX-Datei Objekt identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="df47a-105">Retrieves a pointer to the GUID that identifies a DirectX file object.</span></span> <span data-ttu-id="df47a-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="df47a-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="df47a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="df47a-107">Syntax</span></span>


```C++
HRESULT GetId(
  [out, retval] 
            LPGUID pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="df47a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="df47a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df47a-109">*pguid* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="df47a-109">*pGuid* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="df47a-110">Typ: **lpguid**</span><span class="sxs-lookup"><span data-stu-id="df47a-110">Type: **LPGUID**</span></span>

<span data-ttu-id="df47a-111">Zeiger auf eine GUID, um die Objekt-ID zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="df47a-111">Pointer to a GUID to receive the object's ID.</span></span> <span data-ttu-id="df47a-112">Die-Funktion legt die GUID auf eine **null** -GUID fest, wenn das Objekt nicht über eine ID verfügt.</span><span class="sxs-lookup"><span data-stu-id="df47a-112">The function will set the GUID to a **NULL** GUID if the object does not have an ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df47a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df47a-113">Return value</span></span>

<span data-ttu-id="df47a-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="df47a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="df47a-115">Wenn die Methode erfolgreich ausgeführt wird, ist dxfile OK der Rückgabewert \_ .</span><span class="sxs-lookup"><span data-stu-id="df47a-115">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="df47a-116">Wenn die Methode fehlschlägt, kann der Rückgabewert dxfileerr \_ badvalue lauten.</span><span class="sxs-lookup"><span data-stu-id="df47a-116">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="df47a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df47a-117">Requirements</span></span>



| <span data-ttu-id="df47a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df47a-118">Requirement</span></span> | <span data-ttu-id="df47a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="df47a-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df47a-120">Header</span><span class="sxs-lookup"><span data-stu-id="df47a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="df47a-121"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="df47a-121"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="df47a-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="df47a-122">Library</span></span><br/> | <dl> <span data-ttu-id="df47a-123"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df47a-123"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df47a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df47a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df47a-125">Idirectxfileobject</span><span class="sxs-lookup"><span data-stu-id="df47a-125">IDirectXFileObject</span></span>](idirectxfileobject.md)
</dt> </dl>

 

 




