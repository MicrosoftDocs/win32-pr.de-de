---
description: Legt einen dynamischen .net-CRL-Code auf dem Datenträger für .net als vertrauenswürdig fest.
ms.assetid: 4C8C3EF5-5C3C-4710-8223-D7B5BA86EF47
title: Wldpsetdynamiccodetrust-Funktion (wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpSetDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a266563b40d255fe9e904f02e4e4593d4c4d3f33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393022"
---
# <a name="wldpsetdynamiccodetrust-function"></a><span data-ttu-id="3d6b9-103">Wldpsetdynamiccodetrust-Funktion</span><span class="sxs-lookup"><span data-stu-id="3d6b9-103">WldpSetDynamicCodeTrust function</span></span>

<span data-ttu-id="3d6b9-104">Legt einen dynamischen .net-CRL-Code auf dem Datenträger für .net als vertrauenswürdig fest.</span><span class="sxs-lookup"><span data-stu-id="3d6b9-104">Sets an on-disk .NET CRL Dynamic Code trustable for .NET.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d6b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d6b9-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpSetDynamicCodeTrust(
   HANDLE FileHandle
);
```



## <a name="parameters"></a><span data-ttu-id="3d6b9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d6b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d6b9-107">*File handle*</span><span class="sxs-lookup"><span data-stu-id="3d6b9-107">*FileHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="3d6b9-108">Handle für eine dynamische Codedatei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="3d6b9-108">Handle to a on-disk dynamic code file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d6b9-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d6b9-109">Return value</span></span>

<span data-ttu-id="3d6b9-110">Diese Methode gibt bei Erfolg **S \_ OK** zurück oder andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="3d6b9-110">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d6b9-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d6b9-111">Requirements</span></span>



| <span data-ttu-id="3d6b9-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d6b9-112">Requirement</span></span> | <span data-ttu-id="3d6b9-113">Wert</span><span class="sxs-lookup"><span data-stu-id="3d6b9-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3d6b9-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d6b9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3d6b9-115">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d6b9-115">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3d6b9-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d6b9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3d6b9-117">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d6b9-117">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3d6b9-118">Header</span><span class="sxs-lookup"><span data-stu-id="3d6b9-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d6b9-119"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d6b9-119"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3d6b9-120">DLL</span><span class="sxs-lookup"><span data-stu-id="3d6b9-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d6b9-121"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d6b9-121"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




