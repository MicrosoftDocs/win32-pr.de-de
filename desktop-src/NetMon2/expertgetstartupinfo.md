---
description: Die Funktion "expertgetstartupinfo" Ruft die Start Konfigurationsinformationen für den Experten ab.
ms.assetid: 15f080ed-50b7-40c6-b283-dbe416a2b0e9
title: Expertgetstartupinfo-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetStartupInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f34ecc3d0c3eeb085d2a7c0f8c4cb0426663093c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393414"
---
# <a name="expertgetstartupinfo-function"></a><span data-ttu-id="c1542-103">Expertgetstartupinfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="c1542-103">ExpertGetStartupInfo function</span></span>

<span data-ttu-id="c1542-104">Die Funktion " **expertgetstartupinfo** " Ruft die Start Konfigurationsinformationen für den Experten ab.</span><span class="sxs-lookup"><span data-stu-id="c1542-104">The **ExpertGetStartupInfo** function retrieves the startup configuration information for the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1542-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1542-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertGetStartupInfo(
  _In_  HEXPERTKEY         hExpertKey,
  _Out_ PEXPERTSTARTUPINFO pExpertStartupInfo
);
```



## <a name="parameters"></a><span data-ttu-id="c1542-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1542-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1542-107">*hexpertkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1542-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1542-108">Eindeutige expertenkennung.</span><span class="sxs-lookup"><span data-stu-id="c1542-108">Unique expert identifier.</span></span> <span data-ttu-id="c1542-109">Netzwerkmonitor übergibt *hexpertkey* an den Experten, wenn die Funktion [Run](run.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c1542-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="c1542-110">*pexpertstartupinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c1542-110">*pExpertStartupInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1542-111">Zeiger auf eine " [expertstartupinfo](expertstartupinfo.md) "-Struktur, die Startinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="c1542-111">Pointer to an [EXPERTSTARTUPINFO](expertstartupinfo.md) structure that contains startup information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1542-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1542-112">Return value</span></span>

<span data-ttu-id="c1542-113">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c1542-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c1542-114">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert nmerr.</span><span class="sxs-lookup"><span data-stu-id="c1542-114">If the function is unsuccessful, the return value is NMERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1542-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1542-115">Remarks</span></span>

<span data-ttu-id="c1542-116">Die Funktion " **expertgetstartupinfo** " wird verwendet, wenn der Experte die verwendeten Startinformationen bestimmen muss.</span><span class="sxs-lookup"><span data-stu-id="c1542-116">The **ExpertGetStartupInfo** function is used if the expert must determine the startup information that is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1542-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1542-117">Requirements</span></span>



| <span data-ttu-id="c1542-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1542-118">Requirement</span></span> | <span data-ttu-id="c1542-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c1542-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c1542-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1542-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c1542-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1542-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c1542-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1542-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c1542-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1542-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c1542-124">Header</span><span class="sxs-lookup"><span data-stu-id="c1542-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1542-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1542-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="c1542-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c1542-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="c1542-127"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1542-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c1542-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c1542-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1542-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1542-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




