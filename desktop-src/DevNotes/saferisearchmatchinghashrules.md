---
description: Ruft die Ebene einer Hash Identifikations Regel ab, die dem angegebenen Hash entspricht.
ms.assetid: 1592c8da-31c0-45fb-b832-d439dd53c277
title: Saferisearchmatchinghashrules-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SaferiSearchMatchingHashRules
api_type:
- DllExport
api_location:
- Advapi32.dll
- Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
ms.openlocfilehash: 2d1b7a2b2ce3f0f0e45d87a46219f3ee4d999bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483646"
---
# <a name="saferisearchmatchinghashrules-function"></a><span data-ttu-id="dfbbb-103">Saferisearchmatchinghashrules-Funktion</span><span class="sxs-lookup"><span data-stu-id="dfbbb-103">SaferiSearchMatchingHashRules function</span></span>

<span data-ttu-id="dfbbb-104">Ruft die Ebene einer Hash Identifikations Regel ab, die dem angegebenen Hash entspricht.</span><span class="sxs-lookup"><span data-stu-id="dfbbb-104">Gets the level of a hash identification rule that matches the specified hash.</span></span>

<span data-ttu-id="dfbbb-105">Diese Funktion verfügt über keine zugeordnete Import Bibliothek und ist nicht in einem öffentlichen Header deklariert.</span><span class="sxs-lookup"><span data-stu-id="dfbbb-105">This function has no associated import library and is not declared in a public header.</span></span> <span data-ttu-id="dfbbb-106">Sie müssen einen Funktionszeiger mit der Signatur dieser Funktion definieren, und Sie müssen die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Advapi32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="dfbbb-106">You must define a function pointer with the signature of this function, and you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Advapi32.dll.</span></span>

<span data-ttu-id="dfbbb-107">Es wird empfohlen, die Funktion " [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) " zum Auswerten von Software Einschränkungs Richtlinien zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="dfbbb-107">We recommend using the [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) function to evaluate software restriction policies.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfbbb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfbbb-108">Syntax</span></span>


```C++
BOOL WINAPI SaferiSearchMatchingHashRules(
  _In_opt_ ALG_ID HashAlgorithm,
  _In_     PBYTE  pHashBytes,
  _In_     DWORD  dwHashSize,
  _In_opt_ DWORD  dwOriginalImageSize,
  _Out_    PDWORD pdwFoundLevel,
           PDWORD pdwSaferFlags
);
```



## <a name="parameters"></a><span data-ttu-id="dfbbb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfbbb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfbbb-110">*HashAlgorithm* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="dfbbb-110">*HashAlgorithm* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dfbbb-111">Der Bezeichner des Algorithmus, der zum Erstellen des Hashwerts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dfbbb-111">The identifier of the algorithm used to create the hash.</span></span>

</dd> <dt>

<span data-ttu-id="dfbbb-112">*phashbytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfbbb-112">*pHashBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfbbb-113">Ein Zeiger auf ein Bytearray, das den Hash enthält.</span><span class="sxs-lookup"><span data-stu-id="dfbbb-113">A pointer to an array of bytes that contains the hash.</span></span>

</dd> <dt>

<span data-ttu-id="dfbbb-114">*dwhashsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfbbb-114">*dwHashSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfbbb-115">Die Größe des *phashbytes* -Arrays in Bytes.</span><span class="sxs-lookup"><span data-stu-id="dfbbb-115">The size, in bytes, of the *pHashBytes* array.</span></span>

</dd> <dt>

<span data-ttu-id="dfbbb-116">*dworiginalimagesize* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="dfbbb-116">*dwOriginalImageSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dfbbb-117">Die Größe des ursprünglichen Bilds (in Bytes), aus dem der Hash berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="dfbbb-117">The size, in bytes, of the original image from which the hash was computed.</span></span>

</dd> <dt>

<span data-ttu-id="dfbbb-118">*pdwfoundlevel* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dfbbb-118">*pdwFoundLevel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfbbb-119">Ein Zeiger auf den Bezeichner der Ebene für die entsprechende Hash Identifikations Regel.</span><span class="sxs-lookup"><span data-stu-id="dfbbb-119">A pointer to the level identifier for the matching hash identification rule.</span></span>

</dd> <dt>

<span data-ttu-id="dfbbb-120">*pdwsaferflags*</span><span class="sxs-lookup"><span data-stu-id="dfbbb-120">*pdwSaferFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="dfbbb-121">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="dfbbb-121">Reserved.</span></span> <span data-ttu-id="dfbbb-122">Legen Sie diesen Wert auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="dfbbb-122">Set this value to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfbbb-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dfbbb-123">Return value</span></span>

<span data-ttu-id="dfbbb-124">**True** , wenn die Funktion erfolgreich ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="dfbbb-124">**TRUE** if the function is successful; otherwise, **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfbbb-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfbbb-125">Requirements</span></span>



| <span data-ttu-id="dfbbb-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dfbbb-126">Requirement</span></span> | <span data-ttu-id="dfbbb-127">Wert</span><span class="sxs-lookup"><span data-stu-id="dfbbb-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfbbb-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dfbbb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dfbbb-129">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfbbb-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dfbbb-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dfbbb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dfbbb-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfbbb-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dfbbb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="dfbbb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfbbb-133"><dt>Advapi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfbbb-133"><dt>Advapi32.dll</dt></span></span> </dl> |



 

 
