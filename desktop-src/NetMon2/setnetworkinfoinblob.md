---
description: Die setnetworkinfoinblob-Funktion füllt die networkinfo-Struktur im BLOB auf.
ms.assetid: 1a511c26-2fa7-4fe4-a5a9-23188c59bc34
title: Setnetworkinfoinblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNetworkInfoInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a0019bfaf802b5d4dc80d73e75affa3c50d95de1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353599"
---
# <a name="setnetworkinfoinblob-function"></a><span data-ttu-id="38865-103">Setnetworkinfoinblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="38865-103">SetNetworkInfoInBlob function</span></span>

<span data-ttu-id="38865-104">Die **setnetworkinfoinblob** -Funktion füllt die **networkinfo** -Struktur im BLOB auf.</span><span class="sxs-lookup"><span data-stu-id="38865-104">The **SetNetworkInfoInBlob** function fills in the **NETWORKINFO** structure in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="38865-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="38865-105">Syntax</span></span>


```C++
DWORD SetNetworkInfoInBlob(
  _In_ HBLOB         hBlob,
  _In_ LPNETWORKINFO lpNetworkInfo
);
```



## <a name="parameters"></a><span data-ttu-id="38865-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="38865-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38865-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38865-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38865-108">Handle für ein BLOB.</span><span class="sxs-lookup"><span data-stu-id="38865-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="38865-109">*lpnetworkinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38865-109">*lpNetworkInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38865-110">Ein Zeiger auf die vom Benutzer zugewiesene [networkinfo](networkinfo.md) -Struktur, die die Funktion ausfüllt.</span><span class="sxs-lookup"><span data-stu-id="38865-110">Pointer to the user-allocated [NETWORKINFO](networkinfo.md) structure that the function fills in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38865-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38865-111">Return value</span></span>

<span data-ttu-id="38865-112">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="38865-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="38865-113">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="38865-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="38865-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38865-114">Requirements</span></span>



| <span data-ttu-id="38865-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38865-115">Requirement</span></span> | <span data-ttu-id="38865-116">Wert</span><span class="sxs-lookup"><span data-stu-id="38865-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38865-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="38865-117">Minimum supported client</span></span><br/> | <span data-ttu-id="38865-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38865-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="38865-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="38865-119">Minimum supported server</span></span><br/> | <span data-ttu-id="38865-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38865-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="38865-121">Header</span><span class="sxs-lookup"><span data-stu-id="38865-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="38865-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="38865-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="38865-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="38865-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="38865-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38865-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="38865-125">DLL</span><span class="sxs-lookup"><span data-stu-id="38865-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38865-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38865-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38865-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38865-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38865-128">Getnetworkinfofromblob</span><span class="sxs-lookup"><span data-stu-id="38865-128">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="38865-129">Setboolinblob</span><span class="sxs-lookup"><span data-stu-id="38865-129">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="38865-130">Setclassidinblob</span><span class="sxs-lookup"><span data-stu-id="38865-130">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="38865-131">Setdwordinblob</span><span class="sxs-lookup"><span data-stu-id="38865-131">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="38865-132">Setmacaddressinblob</span><span class="sxs-lookup"><span data-stu-id="38865-132">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="38865-133">Setnppaddressfilterinblob</span><span class="sxs-lookup"><span data-stu-id="38865-133">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="38865-134">Setnpppatternfilterinblob</span><span class="sxs-lookup"><span data-stu-id="38865-134">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="38865-135">Setnpptriggerinblob</span><span class="sxs-lookup"><span data-stu-id="38865-135">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="38865-136">Setstringinblob</span><span class="sxs-lookup"><span data-stu-id="38865-136">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




