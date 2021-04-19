---
description: Ruft den freien Speicherplatz ab.
ms.assetid: 4b7f4938-9918-4625-b28d-faf22de56976
title: _GetDiskFreeSpaceEx-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetDiskFreeSpaceEx
api_type:
- DllExport
api_location:
- Msmdun80.dll
ms.openlocfilehash: da4a8eefabf03f6330ac9c1f135482f27dd8aa18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366862"
---
# <a name="_getdiskfreespaceex-function"></a><span data-ttu-id="162d4-103">\_GetDiskFreeSpaceEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="162d4-103">\_GetDiskFreeSpaceEx function</span></span>

<span data-ttu-id="162d4-104">\[Diese Funktion ist ein Wrapper über die **GetDiskFreeSpaceEx** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="162d4-104">\[This function is a wrapper over the **GetDiskFreeSpaceEx** function.</span></span> <span data-ttu-id="162d4-105">Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="162d4-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="162d4-106">Anwendungen sollten **GetDiskFreeSpaceEx** direkt aufrufen.\]</span><span class="sxs-lookup"><span data-stu-id="162d4-106">Applications should call **GetDiskFreeSpaceEx** directly.\]</span></span>

<span data-ttu-id="162d4-107">Ruft den freien Speicherplatz ab.</span><span class="sxs-lookup"><span data-stu-id="162d4-107">Gets the free disk space.</span></span> <span data-ttu-id="162d4-108">Weitere Informationen finden Sie unter [**GetDiskFreeSpaceEx**](/windows/win32/api/fileapi/nf-fileapi-getdiskfreespaceexa).</span><span class="sxs-lookup"><span data-stu-id="162d4-108">See [**GetDiskFreeSpaceEx**](/windows/win32/api/fileapi/nf-fileapi-getdiskfreespaceexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="162d4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="162d4-109">Syntax</span></span>


```C++
BOOL _GetDiskFreeSpaceEx(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="162d4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="162d4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="162d4-111">*...*</span><span class="sxs-lookup"><span data-stu-id="162d4-111">*...*</span></span> 
<span data-ttu-id="162d4-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="162d4-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="162d4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="162d4-113">Requirements</span></span>



| <span data-ttu-id="162d4-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="162d4-114">Requirement</span></span> | <span data-ttu-id="162d4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="162d4-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="162d4-116">DLL</span><span class="sxs-lookup"><span data-stu-id="162d4-116">DLL</span></span><br/> | <dl> <span data-ttu-id="162d4-117"><dt>Msmdun80.dll</dt></span><span class="sxs-lookup"><span data-stu-id="162d4-117"><dt>Msmdun80.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="162d4-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="162d4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="162d4-119">**GetDiskFreeSpaceEx**</span><span class="sxs-lookup"><span data-stu-id="162d4-119">**GetDiskFreeSpaceEx**</span></span>](/windows/win32/api/fileapi/nf-fileapi-getdiskfreespaceexa)
</dt> </dl>

 

 
