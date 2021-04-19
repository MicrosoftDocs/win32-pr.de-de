---
description: Lädt eine Bibliothek.
ms.assetid: 191fcbd8-4542-4cad-955e-6951f3005fc5
title: _LoadLibrary-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _LoadLibrary
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: ce4502813c1ca2a292486a18f1946f4c605c96cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369988"
---
# <a name="_loadlibrary-function"></a><span data-ttu-id="7beac-103">\_LoadLibrary-Funktion</span><span class="sxs-lookup"><span data-stu-id="7beac-103">\_LoadLibrary function</span></span>

<span data-ttu-id="7beac-104">\[Diese Funktion ist ein Wrapper über die **LoadLibrary** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7beac-104">\[This function is a wrapper over the **LoadLibrary** function.</span></span> <span data-ttu-id="7beac-105">Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="7beac-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="7beac-106">Anwendungen sollten **LoadLibrary** direkt aufzurufen.\]</span><span class="sxs-lookup"><span data-stu-id="7beac-106">Applications should call **LoadLibrary** directly.\]</span></span>

<span data-ttu-id="7beac-107">Lädt eine Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="7beac-107">Loads a library.</span></span> <span data-ttu-id="7beac-108">Siehe [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span><span class="sxs-lookup"><span data-stu-id="7beac-108">See [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span>

## <a name="syntax"></a><span data-ttu-id="7beac-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7beac-109">Syntax</span></span>


```C++
HMODULE _LoadLibrary(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="7beac-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7beac-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7beac-111">*...*</span><span class="sxs-lookup"><span data-stu-id="7beac-111">*...*</span></span> 
<span data-ttu-id="7beac-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7beac-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7beac-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7beac-113">Requirements</span></span>



| <span data-ttu-id="7beac-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7beac-114">Requirement</span></span> | <span data-ttu-id="7beac-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7beac-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7beac-116">DLL</span><span class="sxs-lookup"><span data-stu-id="7beac-116">DLL</span></span><br/> | <dl> <span data-ttu-id="7beac-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7beac-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7beac-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7beac-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7beac-119">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="7beac-119">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
