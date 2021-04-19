---
description: Bestimmt, ob Offlinedateien aktiviert ist.
ms.assetid: c7d3173d-ed51-4de6-ad07-4c5e6906b0f4
title: Csciscscenabled-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCIsCSCEnabled
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 13db7ebbb11f678c00a5a755ffe8114f8684b315
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366828"
---
# <a name="csciscscenabled-function"></a><span data-ttu-id="09e49-103">Csciscscenabled-Funktion</span><span class="sxs-lookup"><span data-stu-id="09e49-103">CSCIsCSCEnabled function</span></span>

<span data-ttu-id="09e49-104">\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="09e49-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="09e49-105">Bestimmt, ob Offlinedateien aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="09e49-105">Determines whether Offline Files is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="09e49-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="09e49-106">Syntax</span></span>


```C++
BOOL WINAPI CSCIsCSCEnabled(void);
```



## <a name="parameters"></a><span data-ttu-id="09e49-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="09e49-107">Parameters</span></span>

<span data-ttu-id="09e49-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="09e49-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="09e49-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09e49-109">Return value</span></span>

<span data-ttu-id="09e49-110">Diese Funktion gibt **true** zurück, wenn Offlinedateien aktiviert ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="09e49-110">This function returns **TRUE** if Offline Files is enabled and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="09e49-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09e49-111">Remarks</span></span>

<span data-ttu-id="09e49-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="09e49-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="09e49-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09e49-113">Requirements</span></span>



| <span data-ttu-id="09e49-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09e49-114">Requirement</span></span> | <span data-ttu-id="09e49-115">Wert</span><span class="sxs-lookup"><span data-stu-id="09e49-115">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09e49-116">DLL</span><span class="sxs-lookup"><span data-stu-id="09e49-116">DLL</span></span><br/> | <dl> <span data-ttu-id="09e49-117"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09e49-117"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09e49-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09e49-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09e49-119">**Cscquerydatabasestatus**</span><span class="sxs-lookup"><span data-stu-id="09e49-119">**CSCQueryDatabaseStatus**</span></span>](cscquerydatabasestatus.md)
</dt> </dl>

 

 
