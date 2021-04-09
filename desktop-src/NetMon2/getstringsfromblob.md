---
description: Verwendet sequenzielle Aufrufe, um alle Zeichen folgen innerhalb der angegebenen Bereiche abzurufen.
ms.assetid: 4e819975-84a5-4b73-9a19-792d3607da9c
title: Getstringsfromblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringsFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 25fbc149a663ef68d1588218937568401f414ef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958707"
---
# <a name="getstringsfromblob-function"></a><span data-ttu-id="6d47e-103">Getstringsfromblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="6d47e-103">GetStringsFromBlob function</span></span>

<span data-ttu-id="6d47e-104">Die **getstringsfromblob** -Funktion verwendet sequenzielle Aufrufe, um alle Zeichen folgen innerhalb der angegebenen Bereiche abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6d47e-104">The **GetStringsFromBlob** function uses sequential calls to retrieve all of the strings within specified ranges.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d47e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d47e-105">Syntax</span></span>


```C++
DWORD GetStringsFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pRequestedOwnerName,
  _In_  const char  *pRequestedCategoryName,
  _In_  const char  *pRequestedTagName,
  _Out_ const char  **ppReturnedOwnerName,
  _Out_ const char  **ppReturnedCategoryName,
  _Out_ const char  **ppReturnedTagName,
  _Out_ const char  **ppReturnedString,
  _Out_       DWORD *pRestartKey
);
```



## <a name="parameters"></a><span data-ttu-id="6d47e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d47e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d47e-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d47e-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d47e-108">Ein Handle für das BLOB.</span><span class="sxs-lookup"><span data-stu-id="6d47e-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="6d47e-109">*prequestedownername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d47e-109">*pRequestedOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d47e-110">Ein Zeiger auf den Besitzer Abschnitt, von dem die Zeichenfolge abgeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d47e-110">A pointer to the Owner section to get the string from.</span></span>

</dd> <dt>

<span data-ttu-id="6d47e-111">*prequestedcategoryname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d47e-111">*pRequestedCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d47e-112">Ein Zeiger auf den Kategorieabschnitt, von dem die Zeichenfolge abgeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d47e-112">A pointer to the Category section to get the string from.</span></span>

</dd> <dt>

<span data-ttu-id="6d47e-113">*prequestedtagname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d47e-113">*pRequestedTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d47e-114">Ein Zeiger auf das-Tag für die angeforderte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6d47e-114">A pointer to the tag for the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="6d47e-115">*ppreturnetdownername* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6d47e-115">*ppReturnedOwnerName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d47e-116">Ein Zeiger auf die Variable, auf die verweist, wenn der **Besitzer** Name zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6d47e-116">A pointer to the variable that points to where the **Owner** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="6d47e-117">*ppreturnedcategoryname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6d47e-117">*ppReturnedCategoryName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d47e-118">Ein Zeiger auf die Variable, die auf den Speicherort verweist, an dem der **Kategoriename** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6d47e-118">A pointer to the variable that points to where the **Category** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="6d47e-119">*ppreturnedtagname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6d47e-119">*ppReturnedTagName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d47e-120">Ein Zeiger auf die Variable, auf die zeigt, wo der **Tagname** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6d47e-120">A pointer to the variable that points to where the **Tag** name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="6d47e-121">*ppreturnedstring* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6d47e-121">*ppReturnedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d47e-122">Ein Zeiger auf die Variable, auf die zeigt, wo der Zeichen folgen Name zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6d47e-122">A pointer to the variable that points to where the string name will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="6d47e-123">*prestartkey* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6d47e-123">*pRestartKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d47e-124">Ein Zeiger auf die Variable, in der die Neustart Taste angegeben und zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6d47e-124">A pointer to the variable where the restart key will be specified and returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d47e-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d47e-125">Return value</span></span>

<span data-ttu-id="6d47e-126">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6d47e-126">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6d47e-127">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der das Problem angibt.</span><span class="sxs-lookup"><span data-stu-id="6d47e-127">If the function is unsuccessful, the return value is a NMERR value that indicates the problem.</span></span>

<span data-ttu-id="6d47e-128">Wenn eine angegebene Kombination aus **Besitzer**, **Kategorie** und **Taginformationen** nicht vorhanden ist, ist der Rückgabewert **nmerr \_ BLOB \_ Entry \_ \_ nicht \_ vorhanden**.</span><span class="sxs-lookup"><span data-stu-id="6d47e-128">If a specified combination of **Owner**, **Category**, and **Tag** information does not exist, the return value is **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**.</span></span>

<span data-ttu-id="6d47e-129">Wenn das BLOB vollständig innerhalb der ursprünglich angegebenen Begrenzungen durchlaufen wird, gibt die Funktion den **nmerr- \_ \_ blobeintrag ist \_ \_ nicht \_ vorhanden** und der *prestartkey* -Parameter auf 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="6d47e-129">When the BLOB is traversed completely within the bounds initially specified, the function returns **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**, and the *pRestartKey* parameter points to zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d47e-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d47e-130">Remarks</span></span>

<span data-ttu-id="6d47e-131">Beim ersten Aufrufen der **getstringsfromblob** -Funktion verweist der *prestartkey* -Parameter auf eine Variable, die den Wert 0 (null) enthält.</span><span class="sxs-lookup"><span data-stu-id="6d47e-131">On the initial call to the **GetStringsFromBlob** function, the *pRestartKey* parameter points to a variable that contains the value zero.</span></span> <span data-ttu-id="6d47e-132">Die *vorangefragten* Parameter können nur verwendet werden, wenn die Neustart Taste 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="6d47e-132">The *pRequested* parameters can be used only when the restart key is zero.</span></span> <span data-ttu-id="6d47e-133">In nachfolgenden Aufrufen, wenn *prestartkey* Werte ungleich NULL aufweist, werden die *vorangefragten* Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6d47e-133">In subsequent calls, when *pRestartKey* has nonzero values, the *pRequested* parameters are ignored.</span></span> <span data-ttu-id="6d47e-134">Beim ersten-Befehl können alle auf **null** zeigen, wodurch die Abfrage so eingerichtet wird, dass jeder Eintrag im BLOB zurückgegeben wird (einer pro nachfolgenden-Rückruf).</span><span class="sxs-lookup"><span data-stu-id="6d47e-134">On the initial call, all may point to **NULL**, which sets up the query to return every entry in the BLOB, one per subsequent call.</span></span>

<span data-ttu-id="6d47e-135">Durch die Angabe eines Besitzers werden die Zeichen folgen beschränkt, die nur an diesen Besitzer zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="6d47e-135">Specifying an owner limits the strings returned to just that owner.</span></span> <span data-ttu-id="6d47e-136">Eine ähnliche Einschränkung gilt für Kategorien und Tags, mit der zusätzlichen Einschränkung: Wenn eine Kategorie angegeben wird, muss auch ein Besitzer angegeben werden, und wenn ein Tag angegeben wird, muss eine Kategorie (und somit ein Besitzer) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6d47e-136">A similar limitation is true for categories and tags, with the additional caveat that if a category is specified, an owner must also be specified and if a tag is specified, a category (and therefore an owner) must be specified.</span></span>

<span data-ttu-id="6d47e-137">Beim ersten Aufrufen von **getstringsfromblob** verweist *prestartkey* auf einen neuen Wert, der beim nächsten Aufrufen der-Funktion angegeben werden muss, um den nächsten Wert abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6d47e-137">When the initial call to **GetStringsFromBlob** returns, *pRestartKey* points to a new value, which should be specified on the next call to the function to get the next value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d47e-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d47e-138">Requirements</span></span>



| <span data-ttu-id="6d47e-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d47e-139">Requirement</span></span> | <span data-ttu-id="6d47e-140">Wert</span><span class="sxs-lookup"><span data-stu-id="6d47e-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d47e-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d47e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6d47e-142">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d47e-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6d47e-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d47e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6d47e-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d47e-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6d47e-145">Header</span><span class="sxs-lookup"><span data-stu-id="6d47e-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d47e-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d47e-146"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="6d47e-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6d47e-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d47e-148"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d47e-148"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="6d47e-149">DLL</span><span class="sxs-lookup"><span data-stu-id="6d47e-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d47e-150"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d47e-150"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d47e-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d47e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d47e-152">Setstringinblob</span><span class="sxs-lookup"><span data-stu-id="6d47e-152">SetStringInBlob</span></span>](setstringinblob.md)
</dt> <dt>

[<span data-ttu-id="6d47e-153">Getboolfromblob</span><span class="sxs-lookup"><span data-stu-id="6d47e-153">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="6d47e-154">Getclassidfromblob</span><span class="sxs-lookup"><span data-stu-id="6d47e-154">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="6d47e-155">Getdwordfromblob</span><span class="sxs-lookup"><span data-stu-id="6d47e-155">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="6d47e-156">Getmacaddressfromblob</span><span class="sxs-lookup"><span data-stu-id="6d47e-156">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="6d47e-157">Getnetworkinfofromblob</span><span class="sxs-lookup"><span data-stu-id="6d47e-157">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="6d47e-158">Getnppaddressfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="6d47e-158">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="6d47e-159">Getnpppatternfilterfromblob</span><span class="sxs-lookup"><span data-stu-id="6d47e-159">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="6d47e-160">Getnpptriggerfromblob</span><span class="sxs-lookup"><span data-stu-id="6d47e-160">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="6d47e-161">Getstringfromblob</span><span class="sxs-lookup"><span data-stu-id="6d47e-161">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> </dl>

 

 




