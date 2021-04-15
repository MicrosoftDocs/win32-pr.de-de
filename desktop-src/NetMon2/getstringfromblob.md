---
description: Gibt eine Zeichenfolge an einer angegebenen Position innerhalb eines Blobs zurück.
ms.assetid: 5930a30b-f0ed-4d5b-a0ba-6cead55c2fcd
title: Getstringfromblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 475600fb6128b5dbbaf9333f8c550351831f0a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484323"
---
# <a name="getstringfromblob-function"></a><span data-ttu-id="57fa6-103">Getstringfromblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="57fa6-103">GetStringFromBlob function</span></span>

<span data-ttu-id="57fa6-104">Die **getstringfromblob** -Funktion gibt eine Zeichenfolge zurück, die sich an einer bestimmten Position innerhalb eines BLOB befindet.</span><span class="sxs-lookup"><span data-stu-id="57fa6-104">The **GetStringFromBlob** function returns a string located at a given position within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="57fa6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="57fa6-105">Syntax</span></span>


```C++
DWORD GetStringFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_ const char  **ppString
);
```



## <a name="parameters"></a><span data-ttu-id="57fa6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="57fa6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57fa6-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57fa6-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57fa6-108">Ein Handle für das BLOB.</span><span class="sxs-lookup"><span data-stu-id="57fa6-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="57fa6-109">*pownername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57fa6-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57fa6-110">Ein BLOB- **Besitzer** Abschnitt, in dem sich die Zeichenfolge befindet.</span><span class="sxs-lookup"><span data-stu-id="57fa6-110">A BLOB **Owner** section where the string is located.</span></span>

</dd> <dt>

<span data-ttu-id="57fa6-111">*pcategoryname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57fa6-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57fa6-112">Ein Abschnitt der BLOB- **Kategorie** , in dem sich die Zeichenfolge befindet.</span><span class="sxs-lookup"><span data-stu-id="57fa6-112">A BLOB **Category** section where the string is located.</span></span>

</dd> <dt>

<span data-ttu-id="57fa6-113">*ptagname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57fa6-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57fa6-114">Das **Tag** der angeforderten Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="57fa6-114">The **Tag** of the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="57fa6-115">*ppString* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="57fa6-115">*ppString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57fa6-116">Ein Zeiger auf eine Variable, die auf die zurückgegebene Zeichenfolge zeigt.</span><span class="sxs-lookup"><span data-stu-id="57fa6-116">A pointer to a variable that points to the returned string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57fa6-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57fa6-117">Return value</span></span>

<span data-ttu-id="57fa6-118">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="57fa6-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="57fa6-119">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="57fa6-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

<span data-ttu-id="57fa6-120">Wenn die angegebenen **Besitzer**-, **Kategorie**-oder **Tagdaten** nicht vorhanden sind, gibt die Funktion den **nmerr- \_ \_ blobeintrag \_ \_ nicht \_ vorhanden**.</span><span class="sxs-lookup"><span data-stu-id="57fa6-120">If the specified **Owner**, **Category**, or **Tag** data does not exist, the function returns **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**.</span></span>

## <a name="requirements"></a><span data-ttu-id="57fa6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57fa6-121">Requirements</span></span>



| <span data-ttu-id="57fa6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57fa6-122">Requirement</span></span> | <span data-ttu-id="57fa6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="57fa6-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57fa6-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57fa6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="57fa6-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57fa6-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="57fa6-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57fa6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="57fa6-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57fa6-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="57fa6-128">Header</span><span class="sxs-lookup"><span data-stu-id="57fa6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="57fa6-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="57fa6-129"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="57fa6-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="57fa6-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="57fa6-131"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57fa6-131"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="57fa6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="57fa6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57fa6-133"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57fa6-133"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57fa6-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57fa6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57fa6-135">Setstringinblob</span><span class="sxs-lookup"><span data-stu-id="57fa6-135">SetStringInBlob</span></span>](setstringinblob.md)
</dt> <dt>

[<span data-ttu-id="57fa6-136">Getboolfromblob</span><span class="sxs-lookup"><span data-stu-id="57fa6-136">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="57fa6-137">Getclassidfromblob</span><span class="sxs-lookup"><span data-stu-id="57fa6-137">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="57fa6-138">Getdwordfromblob</span><span class="sxs-lookup"><span data-stu-id="57fa6-138">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="57fa6-139">Getmacaddressfromblob</span><span class="sxs-lookup"><span data-stu-id="57fa6-139">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="57fa6-140">Getnetworkinfofromblob</span><span class="sxs-lookup"><span data-stu-id="57fa6-140">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="57fa6-141">Getnppaddressfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="57fa6-141">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="57fa6-142">Getnpppatternfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="57fa6-142">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="57fa6-143">Getnpptriggerfromblob</span><span class="sxs-lookup"><span data-stu-id="57fa6-143">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="57fa6-144">Getstringsfromblob</span><span class="sxs-lookup"><span data-stu-id="57fa6-144">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




