---
description: Die Funktion getnetworkinfofromblob ruft Netzwerkinformationen aus einem angegebenen BLOB ab.
ms.assetid: 217c33f4-e548-4072-9edd-ded61e6cd743
title: Getnetworkinfofromblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNetworkInfoFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 2f8b15dce010febdc952c2527a9f4ad31054fa3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350993"
---
# <a name="getnetworkinfofromblob-function"></a><span data-ttu-id="08847-103">Getnetworkinfofromblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="08847-103">GetNetworkInfoFromBlob function</span></span>

<span data-ttu-id="08847-104">Die Funktion **getnetworkinfofromblob** ruft Netzwerkinformationen aus einem angegebenen BLOB ab.</span><span class="sxs-lookup"><span data-stu-id="08847-104">The **GetNetworkInfoFromBlob** function retrieves network information from a given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="08847-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="08847-105">Syntax</span></span>


```C++
DWORD GetNetworkInfoFromBlob(
  _In_    HBLOB         hBlob,
  _Inout_ LPNETWORKINFO lpNetworkInfo
);
```



## <a name="parameters"></a><span data-ttu-id="08847-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="08847-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08847-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08847-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08847-108">Handle für ein BLOB.</span><span class="sxs-lookup"><span data-stu-id="08847-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="08847-109">*lpnetworkinfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="08847-109">*lpNetworkInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="08847-110">Ein Zeiger auf die vom Benutzer zugeordnete [networkinfo](networkinfo.md) -Struktur, die ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="08847-110">A pointer to the user-allocated [NETWORKINFO](networkinfo.md) structure that is filled in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08847-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08847-111">Return value</span></span>

<span data-ttu-id="08847-112">Wenn die **getnetworkinfofromblob** -Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="08847-112">If the **GetNetworkInfoFromBlob** function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="08847-113">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="08847-113">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="08847-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08847-114">Remarks</span></span>

<span data-ttu-id="08847-115">Die Netzwerkinformationen werden im Abschnitt BLOB **networkinfo** der Kategorie BLOB-NPP- **Besitzer** gespeichert.</span><span class="sxs-lookup"><span data-stu-id="08847-115">The network information is stored in the BLOB **NetworkInfo** section of the BLOB NPP **Owner** category.</span></span>

## <a name="requirements"></a><span data-ttu-id="08847-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08847-116">Requirements</span></span>



| <span data-ttu-id="08847-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08847-117">Requirement</span></span> | <span data-ttu-id="08847-118">Wert</span><span class="sxs-lookup"><span data-stu-id="08847-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08847-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08847-119">Minimum supported client</span></span><br/> | <span data-ttu-id="08847-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08847-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="08847-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08847-121">Minimum supported server</span></span><br/> | <span data-ttu-id="08847-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="08847-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="08847-123">Header</span><span class="sxs-lookup"><span data-stu-id="08847-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="08847-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="08847-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="08847-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="08847-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="08847-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08847-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="08847-127">DLL</span><span class="sxs-lookup"><span data-stu-id="08847-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08847-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08847-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08847-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08847-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08847-130">Setnetworkinfoinblob</span><span class="sxs-lookup"><span data-stu-id="08847-130">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="08847-131">Getboolfromblob</span><span class="sxs-lookup"><span data-stu-id="08847-131">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="08847-132">Getclassidfromblob</span><span class="sxs-lookup"><span data-stu-id="08847-132">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="08847-133">Getdwordfromblob</span><span class="sxs-lookup"><span data-stu-id="08847-133">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="08847-134">Getmacaddressfromblob</span><span class="sxs-lookup"><span data-stu-id="08847-134">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="08847-135">Getnppaddressfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="08847-135">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="08847-136">Getnpppatternfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="08847-136">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="08847-137">Getnpptriggerfromblob</span><span class="sxs-lookup"><span data-stu-id="08847-137">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="08847-138">Getstringfromblob</span><span class="sxs-lookup"><span data-stu-id="08847-138">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="08847-139">Getstringsfromblob</span><span class="sxs-lookup"><span data-stu-id="08847-139">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




