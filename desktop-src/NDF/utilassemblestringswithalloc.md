---
title: Utilassemlestringswithzuc-Funktion (ndattributils. h)
description: Ordnet eine Zeichenfolge zu und formatiert Sie mithilfe von Zeichen folgen, die in der Zeichen folgen Tabelle angegeben sind Diese Funktion verwendet StringCchPrintf, um die formatierte Zeichenfolge zu erstellen.
ms.assetid: eedc2874-b949-4cc2-ba7c-ebf1924f1156
keywords:
- Utilassemlestringswithzuweisung-Funktion NDF
topic_type:
- apiref
api_name:
- UtilAssembleStringsWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dae121b1d5f2d968f696190c64828be91adc71da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743881"
---
# <a name="utilassemblestringswithalloc-function"></a><span data-ttu-id="9324e-105">Utilassemlestringswithzuweisung-Funktion</span><span class="sxs-lookup"><span data-stu-id="9324e-105">UtilAssembleStringsWithAlloc function</span></span>

<span data-ttu-id="9324e-106">Die **utilassemlestringswithzuweisung** -Funktion ordnet eine Zeichenfolge zu und formatiert Sie mithilfe von Zeichen folgen, die von der Zeichen folgen Tabelle bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9324e-106">The **UtilAssembleStringsWithAlloc** function allocates a string and formats it using strings provided by the string table.</span></span> <span data-ttu-id="9324e-107">Diese Funktion verwendet [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) , um die formatierte Zeichenfolge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9324e-107">This function uses [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) to create the formatted string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9324e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9324e-108">Syntax</span></span>


```C++
HRESULT UtilAssembleStringsWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR InputFormat,
  _In_  LPCWSTR InputString,
  _In_  BOOLEAN AdditionalArgument,
  _In_  ULONG   AdditionalValue
);
```



## <a name="parameters"></a><span data-ttu-id="9324e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9324e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9324e-110">*Puffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9324e-110">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9324e-111">Typ: \**LPWSTR \** _</span><span class="sxs-lookup"><span data-stu-id="9324e-111">Type: \**LPWSTR\** _</span></span>

<span data-ttu-id="9324e-112">Der Speicherort, an dem die neu zugewiesene Zeichenfolge platziert wird.</span><span class="sxs-lookup"><span data-stu-id="9324e-112">The location where the newly allocated string will be placed.</span></span> <span data-ttu-id="9324e-113">Wenn die Zeichenfolge nicht mehr benötigt wird, muss Sie mit [_ *CoTaskMemFree* \*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9324e-113">When the string is no longer needed, it must be released with [_ *CoTaskMemFree*\*](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> <dt>

<span data-ttu-id="9324e-114">*Buffermax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9324e-114">*BufferMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9324e-115">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="9324e-115">Type: **UINT**</span></span>

<span data-ttu-id="9324e-116">Die maximale Anzahl von Zeichen, die in der durch den *Puffer* zugeordneten Zeichenfolge zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="9324e-116">The maximum number of characters allowed in the string allocated by *Buffer*.</span></span> <span data-ttu-id="9324e-117">Wenn die resultierende formatierte Zeichenfolge länger als die angegebene Anzahl von Zeichen ist, wird Sie abgeschnitten und mit Null beendet.</span><span class="sxs-lookup"><span data-stu-id="9324e-117">If the resulting formatted string is longer than the number of characters specified, it is truncated and null-terminated.</span></span>

> [!Note]  
> <span data-ttu-id="9324e-118">Dieser Parameter darf nicht auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9324e-118">This parameter may not be set to zero.</span></span>

 

</dd> <dt>

<span data-ttu-id="9324e-119">*Input Format* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9324e-119">*InputFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9324e-120">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="9324e-120">Type: **LPCWSTR**</span></span>

<span data-ttu-id="9324e-121">Zeichen folgen Ressource aus der Zeichen folgen Tabelle, die einen an [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)übergebenen Format Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="9324e-121">String resource out of the string table representing a format parameter passed to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa).</span></span> <span data-ttu-id="9324e-122">Sie wird mit [**makeintresource**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)erstellt.</span><span class="sxs-lookup"><span data-stu-id="9324e-122">It is constructed using [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span></span>

<span data-ttu-id="9324e-123">Das Format der Ressourcen Zeichenfolge muss entweder einen Format Parameter angeben, der eine Breite Zeichenfolge annimmt, oder einen Format Parameter, der eine Zeichenfolge ohne Vorzeichen und eine Breite Zeichenfolge annimmt.</span><span class="sxs-lookup"><span data-stu-id="9324e-123">The resource string format must specify either a format parameter taking a wide string, or a format parameter taking an unsigned long and a wide string.</span></span>

</dd> <dt>

<span data-ttu-id="9324e-124">*Input String* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9324e-124">*InputString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9324e-125">Typ: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="9324e-125">Type: **LPCWSTR**</span></span>

<span data-ttu-id="9324e-126">Zeichen folgen Ressource aus der Zeichen folgen Tabelle, die ein an [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) übergebener Argument anstelle der breiten Zeichenfolge im Format-Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="9324e-126">String resource out of the string table representing an argument passed to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) in place of the wide string in the format parameter.</span></span> <span data-ttu-id="9324e-127">Sie wird mit [**makeintresource**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)erstellt.</span><span class="sxs-lookup"><span data-stu-id="9324e-127">It is constructed using [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea).</span></span>

</dd> <dt>

<span data-ttu-id="9324e-128">*Additionalargument* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9324e-128">*AdditionalArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9324e-129">Typ: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9324e-129">Type: **BOOLEAN**</span></span>

<span data-ttu-id="9324e-130">True, wenn *additionalvalue* als erstes Formatierungs Argument an [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)übergeben werden soll. andernfalls false (und nur die durch *InputString* identifizierte Ressourcen Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="9324e-130">True if *AdditionalValue* should be passed in as the first formatting argument to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa); otherwise, false (and only the resource string identified by *InputString* will be passed).</span></span>

</dd> <dt>

<span data-ttu-id="9324e-131">*Additionalvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9324e-131">*AdditionalValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9324e-132">Typ: **ulong**</span><span class="sxs-lookup"><span data-stu-id="9324e-132">Type: **ULONG**</span></span>

<span data-ttu-id="9324e-133">Der Wert, der als erstes Formatierungs Argument an [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) übergeben werden soll, wenn *additionalargument* auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9324e-133">The value to pass as the first formatting argument to [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) if *AdditionalArgument* is true.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9324e-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9324e-134">Return value</span></span>

<span data-ttu-id="9324e-135">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9324e-135">Type: **HRESULT**</span></span>

<span data-ttu-id="9324e-136">Mögliche Rückgabewerte sind u. a. die folgenden.</span><span class="sxs-lookup"><span data-stu-id="9324e-136">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="9324e-137">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9324e-137">Return code</span></span>                                                                                  | <span data-ttu-id="9324e-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9324e-138">Description</span></span>                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="9324e-139"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9324e-139"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="9324e-140">Der Vorgang wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9324e-140">The operation succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="9324e-141"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="9324e-141"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="9324e-142">Mindestens ein Parameter wurde nicht ordnungsgemäß bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="9324e-142">One or more parameters has not been provided correctly.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9324e-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9324e-143">Requirements</span></span>



| <span data-ttu-id="9324e-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9324e-144">Requirement</span></span> | <span data-ttu-id="9324e-145">Wert</span><span class="sxs-lookup"><span data-stu-id="9324e-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="9324e-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9324e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9324e-147">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9324e-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9324e-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9324e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9324e-149">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9324e-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9324e-150">Header</span><span class="sxs-lookup"><span data-stu-id="9324e-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="9324e-151"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="9324e-151"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9324e-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9324e-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9324e-153">**Utilstringcopywithzuzuweisung**</span><span class="sxs-lookup"><span data-stu-id="9324e-153">**UtilStringCopyWithAlloc**</span></span>](utilstringcopywithalloc.md)
</dt> <dt>

[<span data-ttu-id="9324e-154">**Utilloadstringwithzuordc**</span><span class="sxs-lookup"><span data-stu-id="9324e-154">**UtilLoadStringWithAlloc**</span></span>](utilloadstringwithalloc.md)
</dt> <dt>

[<span data-ttu-id="9324e-155">**StringCchPrintf**</span><span class="sxs-lookup"><span data-stu-id="9324e-155">**StringCchPrintf**</span></span>](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)
</dt> <dt>

[<span data-ttu-id="9324e-156">**Makeintresource**</span><span class="sxs-lookup"><span data-stu-id="9324e-156">**MAKEINTRESOURCE**</span></span>](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)
</dt> <dt>

[<span data-ttu-id="9324e-157">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="9324e-157">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

