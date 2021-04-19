---
description: Die ThunkConnect32-Funktion wird von 16-Bit-Gerätetreibern (für MS-DOS) verwendet, die den 32-Bit-Kernel aufzurufen.
ms.assetid: 3376ca67-04ea-4765-a2f4-15a84d5c84d4
title: ThunkConnect32-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ThunkConnect32
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 7f22d7ceb59732e986c23c873133b11f358364cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367550"
---
# <a name="thunkconnect32-function"></a><span data-ttu-id="d3fe3-103">ThunkConnect32-Funktion</span><span class="sxs-lookup"><span data-stu-id="d3fe3-103">ThunkConnect32 function</span></span>

<span data-ttu-id="d3fe3-104">\[Diese Funktion wurde aus Gründen der Abwärtskompatibilität unterstützt, ist jedoch in den aktuellen Versionen von Windows nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d3fe3-104">\[This function was supported for backward compatibility, but is not present in current versions of Windows.</span></span> <span data-ttu-id="d3fe3-105">Neue Gerätetreiber sollten 32-oder 64-Bit sein und benötigen diese Funktion nicht.\]</span><span class="sxs-lookup"><span data-stu-id="d3fe3-105">New device drivers should be 32- or 64-bit and do not need this function.\]</span></span>

<span data-ttu-id="d3fe3-106">Die **ThunkConnect32** -Funktion wird von 16-Bit-Gerätetreibern (für MS-DOS) verwendet, die den 32-Bit-Kernel aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d3fe3-106">The **ThunkConnect32** function is used by 16-bit device drivers (for MS-DOS) that call into the 32-bit kernel.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3fe3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3fe3-107">Syntax</span></span>


```C++
BOOL ThunkConnect32(
   LPVOID lpThunkData32,
   LPSTR  pszThunkData16Name,
   LPSTR  pszDll16,
   LPSTR  pszDll32,
   HANDLE hInstance,
   DWORD  dwReason
);
```



## <a name="parameters"></a><span data-ttu-id="d3fe3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3fe3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3fe3-109">*lpThunkData32*</span><span class="sxs-lookup"><span data-stu-id="d3fe3-109">*lpThunkData32*</span></span> 
</dt> <dd>

<span data-ttu-id="d3fe3-110">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d3fe3-110">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="d3fe3-111">*pszThunkData16Name*</span><span class="sxs-lookup"><span data-stu-id="d3fe3-111">*pszThunkData16Name*</span></span> 
</dt> <dd>

<span data-ttu-id="d3fe3-112">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d3fe3-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="d3fe3-113">*pszDll16*</span><span class="sxs-lookup"><span data-stu-id="d3fe3-113">*pszDll16*</span></span> 
</dt> <dd>

<span data-ttu-id="d3fe3-114">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d3fe3-114">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="d3fe3-115">*pszDll32*</span><span class="sxs-lookup"><span data-stu-id="d3fe3-115">*pszDll32*</span></span> 
</dt> <dd>

<span data-ttu-id="d3fe3-116">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d3fe3-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="d3fe3-117">*hInstance*</span><span class="sxs-lookup"><span data-stu-id="d3fe3-117">*hInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="d3fe3-118">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d3fe3-118">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="d3fe3-119">*dwReason*</span><span class="sxs-lookup"><span data-stu-id="d3fe3-119">*dwReason*</span></span> 
</dt> <dd>

<span data-ttu-id="d3fe3-120">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d3fe3-120">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3fe3-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3fe3-121">Return value</span></span>

<span data-ttu-id="d3fe3-122">Gibt immer **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="d3fe3-122">Always returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3fe3-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3fe3-123">Requirements</span></span>



| <span data-ttu-id="d3fe3-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3fe3-124">Requirement</span></span> | <span data-ttu-id="d3fe3-125">Wert</span><span class="sxs-lookup"><span data-stu-id="d3fe3-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3fe3-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d3fe3-126">DLL</span></span><br/> | <dl> <span data-ttu-id="d3fe3-127"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3fe3-127"><dt>Kernel32.dll</dt></span></span> </dl> |



 

 




