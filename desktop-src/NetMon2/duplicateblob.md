---
description: Die duplicateblob-Funktion kopiert ein bestimmtes Blob.
ms.assetid: d2478f53-328c-4799-890c-7849ce1f22e9
title: Duplicateblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DuplicateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: df0fc00f0bd51e89da432e6f3b0143ce6092cedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359415"
---
# <a name="duplicateblob-function"></a><span data-ttu-id="ff4ba-103">Duplicateblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="ff4ba-103">DuplicateBlob function</span></span>

<span data-ttu-id="ff4ba-104">Die **duplicateblob** -Funktion kopiert ein bestimmtes Blob.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-104">The **DuplicateBlob** function copies a specific BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff4ba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff4ba-105">Syntax</span></span>


```C++
DWORD DuplicateBlob(
  _In_  HBLOB hSrcBlob,
  _Out_ HBLOB *hBlobThatWillBeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="ff4ba-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff4ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff4ba-107">*hsrcblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff4ba-107">*hSrcBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff4ba-108">Handle für das BLOB, das kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-108">Handle to the BLOB that is copied.</span></span>

</dd> <dt>

<span data-ttu-id="ff4ba-109">*hblobthatwillbecreated* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ff4ba-109">*hBlobThatWillBeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff4ba-110">Handle für das doppelte BLOB.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-110">Handle to the duplicate BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff4ba-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff4ba-111">Return value</span></span>

<span data-ttu-id="ff4ba-112">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ff4ba-113">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="ff4ba-113">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff4ba-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff4ba-114">Requirements</span></span>



| <span data-ttu-id="ff4ba-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff4ba-115">Requirement</span></span> | <span data-ttu-id="ff4ba-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ff4ba-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff4ba-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff4ba-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ff4ba-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff4ba-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ff4ba-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff4ba-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ff4ba-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff4ba-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ff4ba-121">Header</span><span class="sxs-lookup"><span data-stu-id="ff4ba-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff4ba-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff4ba-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="ff4ba-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ff4ba-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="ff4ba-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff4ba-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="ff4ba-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ff4ba-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff4ba-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff4ba-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff4ba-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff4ba-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff4ba-128">CreateBlob</span><span class="sxs-lookup"><span data-stu-id="ff4ba-128">CreateBlob</span></span>](createblob.md)
</dt> <dt>

[<span data-ttu-id="ff4ba-129">Destroyblob</span><span class="sxs-lookup"><span data-stu-id="ff4ba-129">DestroyBlob</span></span>](destroyblob.md)
</dt> </dl>

 

 




