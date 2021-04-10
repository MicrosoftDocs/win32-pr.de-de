---
description: Die Funktion getnppaddressfilterfromblob füllt den angegebenen Adress Filter mit Informationen aus, die im BLOB gespeichert sind.
ms.assetid: b34e0e52-1b2a-4d61-b60c-f1b19ff8ff38
title: Getnppaddressfilterfromblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPAddressFilterFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 944821620123d63f654e286a77018232c79981e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960637"
---
# <a name="getnppaddressfilterfromblob-function"></a><span data-ttu-id="95073-103">Getnppaddressfilterfromblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="95073-103">GetNPPAddressFilterFromBlob function</span></span>

<span data-ttu-id="95073-104">Die Funktion **getnppaddressfilterfromblob** füllt den angegebenen Adress Filter mit Informationen aus, die im BLOB gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="95073-104">The **GetNPPAddressFilterFromBlob** function fills in the given address filter with information stored in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="95073-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="95073-105">Syntax</span></span>


```C++
DWORD GetNPPAddressFilterFromBlob(
  _In_    HBLOB          hBlob,
  _Inout_ LPADDRESSTABLE pAddressTable,
  _Out_   HBLOB          hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="95073-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="95073-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95073-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95073-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95073-108">Handle für ein BLOB.</span><span class="sxs-lookup"><span data-stu-id="95073-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="95073-109">*padresssstable* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="95073-109">*pAddressTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="95073-110">Zeiger auf die vom Benutzer zugeordnete Adress Tabelle.</span><span class="sxs-lookup"><span data-stu-id="95073-110">Pointer to the user-allocated address table.</span></span>

</dd> <dt>

<span data-ttu-id="95073-111">*herrorblob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="95073-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95073-112">Handle für ein fehlerblob, das angibt, wo der Fehler im ursprünglichen BLOB aufgetreten ist (falls vorhanden).</span><span class="sxs-lookup"><span data-stu-id="95073-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95073-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95073-113">Return value</span></span>

<span data-ttu-id="95073-114">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="95073-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="95073-115">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="95073-115">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="95073-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95073-116">Remarks</span></span>

<span data-ttu-id="95073-117">Die Adressinformationen werden im **Konfigurations** Abschnitt der BLOB-NPP- **Besitzer** Kategorie gespeichert.</span><span class="sxs-lookup"><span data-stu-id="95073-117">The address information is stored in the **Config** section of the BLOB NPP **Owner** category.</span></span>

## <a name="requirements"></a><span data-ttu-id="95073-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95073-118">Requirements</span></span>



| <span data-ttu-id="95073-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95073-119">Requirement</span></span> | <span data-ttu-id="95073-120">Wert</span><span class="sxs-lookup"><span data-stu-id="95073-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95073-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95073-121">Minimum supported client</span></span><br/> | <span data-ttu-id="95073-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95073-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="95073-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95073-123">Minimum supported server</span></span><br/> | <span data-ttu-id="95073-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95073-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="95073-125">Header</span><span class="sxs-lookup"><span data-stu-id="95073-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="95073-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="95073-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="95073-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="95073-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="95073-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95073-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="95073-129">DLL</span><span class="sxs-lookup"><span data-stu-id="95073-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95073-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95073-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95073-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95073-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95073-132">Setnppaddressfilterinblob</span><span class="sxs-lookup"><span data-stu-id="95073-132">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="95073-133">Getboolfromblob</span><span class="sxs-lookup"><span data-stu-id="95073-133">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="95073-134">Getclassidfromblob</span><span class="sxs-lookup"><span data-stu-id="95073-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="95073-135">Getdwordfromblob</span><span class="sxs-lookup"><span data-stu-id="95073-135">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="95073-136">Getmacaddressfromblob</span><span class="sxs-lookup"><span data-stu-id="95073-136">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="95073-137">Getnetworkinfofromblob</span><span class="sxs-lookup"><span data-stu-id="95073-137">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="95073-138">Getnpppatternfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="95073-138">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="95073-139">Getnpptriggerfromblob</span><span class="sxs-lookup"><span data-stu-id="95073-139">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="95073-140">Getstringfromblob</span><span class="sxs-lookup"><span data-stu-id="95073-140">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="95073-141">Getstringsfromblob</span><span class="sxs-lookup"><span data-stu-id="95073-141">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




