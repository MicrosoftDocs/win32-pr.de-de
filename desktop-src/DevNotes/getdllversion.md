---
description: Die getdllversion-Funktion Ruft die Versionsnummer Cabinet.dll ab.
ms.assetid: b324d5cd-1ede-473e-a10f-249c95eda057
title: Getdllversion-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDllVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 1b1142bd2ece965a3f2fc58b6bb2f90586a8b391
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351264"
---
# <a name="getdllversion-function"></a><span data-ttu-id="4d4f7-103">Getdllversion-Funktion</span><span class="sxs-lookup"><span data-stu-id="4d4f7-103">GetDllVersion function</span></span>

<span data-ttu-id="4d4f7-104">\[Diese Funktion wird nicht mehr unterstützt, sodass Ihr Verhalten nicht garantiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4d4f7-104">\[This function is no longer supported, so its behavior cannot be guaranteed.</span></span> <span data-ttu-id="4d4f7-105">\]</span><span class="sxs-lookup"><span data-stu-id="4d4f7-105">\]</span></span>

<span data-ttu-id="4d4f7-106">Die **getdllversion** -Funktion Ruft die Versionsnummer Cabinet.dll ab.</span><span class="sxs-lookup"><span data-stu-id="4d4f7-106">The **GetDllVersion** function retrieves the version number of Cabinet.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d4f7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d4f7-107">Syntax</span></span>


```C++
LPCSTR WINAPI GetDllVersion(void);
```



## <a name="parameters"></a><span data-ttu-id="4d4f7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d4f7-108">Parameters</span></span>

<span data-ttu-id="4d4f7-109">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4d4f7-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4d4f7-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d4f7-110">Return value</span></span>

<span data-ttu-id="4d4f7-111">Die Versionsnummer der Datei (siehe [VERSIONINFO-Ressource](../menurc/versioninfo-resource.md)).</span><span class="sxs-lookup"><span data-stu-id="4d4f7-111">The version number of the file (see [VERSIONINFO Resource](../menurc/versioninfo-resource.md)).</span></span>

## <a name="remarks"></a><span data-ttu-id="4d4f7-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d4f7-112">Remarks</span></span>

<span data-ttu-id="4d4f7-113">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4d4f7-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d4f7-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d4f7-114">Requirements</span></span>



| <span data-ttu-id="4d4f7-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d4f7-115">Requirement</span></span> | <span data-ttu-id="4d4f7-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4d4f7-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d4f7-117">DLL</span><span class="sxs-lookup"><span data-stu-id="4d4f7-117">DLL</span></span><br/> | <dl> <span data-ttu-id="4d4f7-118"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d4f7-118"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d4f7-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d4f7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d4f7-120">**Dllgetversion**</span><span class="sxs-lookup"><span data-stu-id="4d4f7-120">**DllGetVersion**</span></span>](dllgetversion.md)
</dt> </dl>

 

 
