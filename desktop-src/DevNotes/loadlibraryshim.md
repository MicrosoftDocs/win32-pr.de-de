---
description: Lädt eine angegebene Version einer .NET Framework Bibliotheks-DLL.
ms.assetid: f001774d-ea9a-4820-aec0-99ce958b1e1d
title: LoadLibraryShim-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadLibraryShim
api_type:
- DllExport
api_location:
- Mscoree.dll
ms.openlocfilehash: 3a2fd8ab6aef8d0309748cbbf37d56ccd032b050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365916"
---
# <a name="loadlibraryshim-function"></a><span data-ttu-id="5f61a-103">LoadLibraryShim-Funktion</span><span class="sxs-lookup"><span data-stu-id="5f61a-103">LoadLibraryShim function</span></span>

<span data-ttu-id="5f61a-104">Lädt eine angegebene Version einer .NET Framework Bibliotheks-DLL.</span><span class="sxs-lookup"><span data-stu-id="5f61a-104">Loads a specified version of a .NET Framework library DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f61a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f61a-105">Syntax</span></span>


```C++
HRESULT LoadLibraryShim(
  _In_  LPCWSTR szDllName,
  _In_  LPCWSTR szVersion,
        LPVOID  pvReserved,
  _Out_ HMODULE *phModDll
);
```



## <a name="parameters"></a><span data-ttu-id="5f61a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f61a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f61a-107">*szDllName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f61a-107">*szDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f61a-108">Der Name der dll, die aus dem .NET Framework geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f61a-108">The name of the DLL to be loaded from the .NET Framework.</span></span>

</dd> <dt>

<span data-ttu-id="5f61a-109">*szVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f61a-109">*szVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f61a-110">Die Version der zu ladenden DLL.</span><span class="sxs-lookup"><span data-stu-id="5f61a-110">The version of the DLL to be loaded.</span></span> <span data-ttu-id="5f61a-111">Wenn *szVersion* **null** ist, wird die aktuelle Version der angegebenen DLL geladen.</span><span class="sxs-lookup"><span data-stu-id="5f61a-111">If *szVersion* is **NULL**, the latest version of the specified DLL is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="5f61a-112">*pvReserved*</span><span class="sxs-lookup"><span data-stu-id="5f61a-112">*pvReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="5f61a-113">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="5f61a-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5f61a-114">*phModDll* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5f61a-114">*phModDll* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f61a-115">Ein Handle für das Modul.</span><span class="sxs-lookup"><span data-stu-id="5f61a-115">A handle to the module.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f61a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f61a-116">Return value</span></span>

<span data-ttu-id="5f61a-117">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="5f61a-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5f61a-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5f61a-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f61a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f61a-119">Remarks</span></span>

<span data-ttu-id="5f61a-120">Diese Funktion wird zum Laden von Bibliothek-DLLs verwendet, die in der .NET Framework weitervertreibbaren Pakets enthalten sind, nicht von benutzergenerierten DLLs.</span><span class="sxs-lookup"><span data-stu-id="5f61a-120">This function is used to load library DLLs that are included in the .NET Framework redistributable package, not user-generated DLLs.</span></span>

<span data-ttu-id="5f61a-121">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5f61a-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f61a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f61a-122">Requirements</span></span>



| <span data-ttu-id="5f61a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f61a-123">Requirement</span></span> | <span data-ttu-id="5f61a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5f61a-124">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f61a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5f61a-125">DLL</span></span><br/> | <dl> <span data-ttu-id="5f61a-126"><dt>Mscoree.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f61a-126"><dt>Mscoree.dll</dt></span></span> </dl> |



 

 
