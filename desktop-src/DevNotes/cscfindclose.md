---
description: Schließt ein Suchhandle.
ms.assetid: 2e6a547f-26a7-401a-b1e4-3f085ce82729
title: Cscfindclose-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindClose
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 69e3ea972ccd67a1db999c186709ef3aeff84be9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354713"
---
# <a name="cscfindclose-function"></a><span data-ttu-id="83934-103">Cscfindclose-Funktion</span><span class="sxs-lookup"><span data-stu-id="83934-103">CSCFindClose function</span></span>

<span data-ttu-id="83934-104">\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="83934-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="83934-105">Schließt ein Suchhandle.</span><span class="sxs-lookup"><span data-stu-id="83934-105">Closes a search handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="83934-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="83934-106">Syntax</span></span>


```C++
BOOL WINAPI CSCFindClose(
  _In_ HANDLE hFind
);
```



## <a name="parameters"></a><span data-ttu-id="83934-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="83934-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83934-108">*hfind* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83934-108">*hFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83934-109">Ein Suchhandle, das von der [**cscfindfirstfilew**](cscfindfirstfilew.md) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="83934-109">A search handle returned by the [**CSCFindFirstFileW**](cscfindfirstfilew.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83934-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83934-110">Return value</span></span>

<span data-ttu-id="83934-111">Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="83934-111">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="83934-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83934-112">Remarks</span></span>

<span data-ttu-id="83934-113">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="83934-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="83934-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83934-114">Requirements</span></span>



| <span data-ttu-id="83934-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83934-115">Requirement</span></span> | <span data-ttu-id="83934-116">Wert</span><span class="sxs-lookup"><span data-stu-id="83934-116">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83934-117">DLL</span><span class="sxs-lookup"><span data-stu-id="83934-117">DLL</span></span><br/> | <dl> <span data-ttu-id="83934-118"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83934-118"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83934-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83934-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83934-120">**Cscfindfirstfilew**</span><span class="sxs-lookup"><span data-stu-id="83934-120">**CSCFindFirstFileW**</span></span>](cscfindfirstfilew.md)
</dt> </dl>

 

 
