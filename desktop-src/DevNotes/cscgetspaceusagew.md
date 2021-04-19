---
description: Ruft Informationen über den vom Offlinedateien Cache verwendeten Speicherplatz ab.
ms.assetid: 3a6fa548-0e9a-4138-a5ec-cde0aeb2b811
title: Cscgetspaceusagew-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCGetSpaceUsageW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 608fd7736093ae1f8d131ede777a691e467de9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369189"
---
# <a name="cscgetspaceusagew-function"></a><span data-ttu-id="a5f38-103">Cscgetspaceusagew-Funktion</span><span class="sxs-lookup"><span data-stu-id="a5f38-103">CSCGetSpaceUsageW function</span></span>

<span data-ttu-id="a5f38-104">\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="a5f38-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="a5f38-105">Ruft Informationen über den vom Offlinedateien Cache verwendeten Speicherplatz ab.</span><span class="sxs-lookup"><span data-stu-id="a5f38-105">Retrieves information about the space used by the Offline Files cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5f38-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5f38-106">Syntax</span></span>


```C++
BOOL WINAPI CSCGetSpaceUsageW(
  _Inout_ LPTSTR  lptzLocation,
  _In_    DWORD   dwSize,
  _Inout_ LPDWORD lpdwMaxSpaceHigh,
  _Inout_ LPDWORD lpdwMaxSpaceLow,
  _Inout_ LPDWORD lpdwCurrentSpaceHigh,
  _Inout_ LPDWORD lpdwCurrentSpaceLow,
  _Inout_ LPDWORD lpcntTotalFiles,
  _Inout_ LPDWORD lpcntTotalDirs
);
```



## <a name="parameters"></a><span data-ttu-id="a5f38-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5f38-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5f38-108">*lptzlocation* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a5f38-108">*lptzLocation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f38-109">Der Verzeichnis Speicherort des Caches.</span><span class="sxs-lookup"><span data-stu-id="a5f38-109">The directory location of the cache.</span></span>

</dd> <dt>

<span data-ttu-id="a5f38-110">*dwSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5f38-110">*dwSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f38-111">Die Größe des *lptzlocation* -Puffers in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a5f38-111">The size of the *lptzLocation* buffer, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="a5f38-112">*lpdwmaxspacehigh* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a5f38-112">*lpdwMaxSpaceHigh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f38-113">Das höchst wertige **DWORD** -Wert der maximalen Anzahl von Bytes, die im Cache verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a5f38-113">The high-order **DWORD** of the maximum number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="a5f38-114">*lpdwmaxspacelow* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a5f38-114">*lpdwMaxSpaceLow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f38-115">Das **DWORD** in niedriger Reihenfolge mit der maximalen Anzahl von Bytes, die im Cache verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a5f38-115">The low-order **DWORD** of the maximum number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="a5f38-116">*lpdwcurrentspacehigh* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a5f38-116">*lpdwCurrentSpaceHigh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f38-117">Das höchst wertige **DWORD** der aktuellen Anzahl von Bytes, die im Cache verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a5f38-117">The high-order **DWORD** of the current number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="a5f38-118">*lpdwcurrentspacelow* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a5f38-118">*lpdwCurrentSpaceLow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f38-119">Das **DWORD** mit niedriger Ordnung der aktuellen Anzahl von Bytes, die im Cache verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a5f38-119">The low-order **DWORD** of the current number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="a5f38-120">*lpcnttotalfiles* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a5f38-120">*lpcntTotalFiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f38-121">Die Gesamtanzahl der Dateien im Cache.</span><span class="sxs-lookup"><span data-stu-id="a5f38-121">The total number of files in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="a5f38-122">*lpcnttotaldirs* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a5f38-122">*lpcntTotalDirs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f38-123">Die Gesamtanzahl der Verzeichnisse im Cache.</span><span class="sxs-lookup"><span data-stu-id="a5f38-123">The total number of directories in the cache.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5f38-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5f38-124">Return value</span></span>

<span data-ttu-id="a5f38-125">Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a5f38-125">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5f38-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5f38-126">Remarks</span></span>

<span data-ttu-id="a5f38-127">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a5f38-127">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5f38-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5f38-128">Requirements</span></span>



| <span data-ttu-id="a5f38-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5f38-129">Requirement</span></span> | <span data-ttu-id="a5f38-130">Wert</span><span class="sxs-lookup"><span data-stu-id="a5f38-130">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5f38-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a5f38-131">DLL</span></span><br/> | <dl> <span data-ttu-id="a5f38-132"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5f38-132"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
