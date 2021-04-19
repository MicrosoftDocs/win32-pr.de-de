---
description: Ruft die Adresse einer Funktion aus einer DLL ab.
ms.assetid: e425948c-5588-4a4f-994c-4e608af18439
title: _GetProcAddress_ -Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetProcAddress_
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 0d717036b92e79056fd3b1bf69f1fd17784db713
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352087"
---
# <a name="_getprocaddress_-function"></a><span data-ttu-id="1721e-103">\_GetProcAddress- \_ Funktion</span><span class="sxs-lookup"><span data-stu-id="1721e-103">\_GetProcAddress\_ function</span></span>

<span data-ttu-id="1721e-104">\[Diese Funktion ist ein Wrapper über die **GetProcAddress** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="1721e-104">\[This function is a wrapper over the **GetProcAddress** function.</span></span> <span data-ttu-id="1721e-105">Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="1721e-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="1721e-106">Anwendungen sollten **GetProcAddress** direkt aufrufen.\]</span><span class="sxs-lookup"><span data-stu-id="1721e-106">Applications should call **GetProcAddress** directly.\]</span></span>

<span data-ttu-id="1721e-107">Ruft die Adresse einer Funktion aus einer DLL ab.</span><span class="sxs-lookup"><span data-stu-id="1721e-107">Gets the address of a function from a DLL.</span></span> <span data-ttu-id="1721e-108">Siehe [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="1721e-108">See [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

## <a name="syntax"></a><span data-ttu-id="1721e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1721e-109">Syntax</span></span>


```C++
FARPROC _GetProcAddress_(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="1721e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1721e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1721e-111">*...*</span><span class="sxs-lookup"><span data-stu-id="1721e-111">*...*</span></span> 
<span data-ttu-id="1721e-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1721e-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="1721e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1721e-113">Requirements</span></span>



| <span data-ttu-id="1721e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1721e-114">Requirement</span></span> | <span data-ttu-id="1721e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1721e-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1721e-116">DLL</span><span class="sxs-lookup"><span data-stu-id="1721e-116">DLL</span></span><br/> | <dl> <span data-ttu-id="1721e-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1721e-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1721e-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1721e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1721e-119">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="1721e-119">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 
