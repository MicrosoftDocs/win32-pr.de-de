---
title: Ivmvirtualpc SearchPath-Eigenschaft (vpccominterfaces. h)
description: Dateisystem Pfade, die verwendet werden, um Dateien zu suchen, die mit Windows Virtual PC verknüpft sind.
ms.assetid: 2a2deee5-7e6b-4b90-8ce9-0b0dbeef0f30
keywords:
- SearchPath-Eigenschaft virtueller PC
- SearchPath-Eigenschaft Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, SearchPath (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMVirtualPC.SearchPaths
- IVMVirtualPC.get_SearchPaths
- IVMVirtualPC.put_SearchPaths
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287eb07bc9205f9b6f0851bd8809f9a49dcf3242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739745"
---
# <a name="ivmvirtualpcsearchpaths-property"></a><span data-ttu-id="3e181-106">Ivmvirtualpc:: SearchPath (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3e181-106">IVMVirtualPC::SearchPaths property</span></span>

<span data-ttu-id="3e181-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3e181-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3e181-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3e181-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3e181-109">Ruft die Dateisystem Pfade ab und legt Sie fest, die verwendet werden, um Dateien zu suchen, die mit Windows Virtual PC verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="3e181-109">Retrieves and sets the file system paths that are used to find files associated with Windows Virtual PC.</span></span>

<span data-ttu-id="3e181-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3e181-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e181-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e181-111">Syntax</span></span>


```C++
HRESULT put_SearchPaths(
  [in]          VARIANT searchPaths
);

HRESULT get_SearchPaths(
  [out, retval] VARIANT *searchPaths
);
```



## <a name="property-value"></a><span data-ttu-id="3e181-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3e181-112">Property value</span></span>

<span data-ttu-id="3e181-113">Gibt ein SAFEARRAY an, das für jeden Eintrag einen Dateisystempfad enthält.</span><span class="sxs-lookup"><span data-stu-id="3e181-113">Specifies a safearray containing a file system path for each entry.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3e181-114">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3e181-114">Error codes</span></span>



| <span data-ttu-id="3e181-115">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="3e181-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="3e181-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3e181-116">Meaning</span></span>                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e181-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3e181-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="3e181-118">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e181-118">The operation was successful.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="3e181-119"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3e181-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="3e181-120">Der-Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="3e181-120">The parameter is **NULL**.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="3e181-121"><dt>E \_ InvalidArg</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="3e181-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="3e181-122">Der *SearchPath* -Parameter ist ungültig und konnte nicht in ein Array von Pfaden analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="3e181-122">The *searchPaths* parameter is not valid and could not be parsed into an array of paths.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3e181-123"><dt>HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="3e181-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="3e181-124">Das System kann ein im *SearchPath* -Parameter angegebenes Verzeichnis nicht finden.</span><span class="sxs-lookup"><span data-stu-id="3e181-124">The system cannot find a directory specified in the *searchPaths* parameter.</span></span><br/>                                                |
| <dl> <span data-ttu-id="3e181-125"><dt>HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="3e181-125"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="3e181-126">Das System kann keinen durch den *SearchPath* -Parameter angegebenen Pfad finden.</span><span class="sxs-lookup"><span data-stu-id="3e181-126">The system cannot find a path specified by the *searchPaths* parameter.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="3e181-127"><dt>HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="3e181-127"><dt>HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="3e181-128">Ein im *SearchPath* -Parameter angegebener Pfad enthält ungültige Zeichen.</span><span class="sxs-lookup"><span data-stu-id="3e181-128">A path specified in the *searchPaths* parameter contains illegal characters.</span></span> <span data-ttu-id="3e181-129">Ungültige Zeichen sind " \* ? <>/ \| ": ".</span><span class="sxs-lookup"><span data-stu-id="3e181-129">The illegal characters are "\*?<>/\|":".</span></span><br/> |
| <dl> <span data-ttu-id="3e181-130"><dt>HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="3e181-130"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="3e181-131">Ein im *SearchPath* -Parameter enthaltener Pfad gibt einen leeren oder relativen Pfad an.</span><span class="sxs-lookup"><span data-stu-id="3e181-131">A path contained in the *searchPaths* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="3e181-132">Ein absoluter Pfad ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3e181-132">An absolute path is required.</span></span><br/>          |
| <dl> <span data-ttu-id="3e181-133"><dt>HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="3e181-133"><dt>HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="3e181-134">Der im *SearchPath* -Parameter angegebene Pfad ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="3e181-134">The path specified in the *searchPaths* parameter is too long.</span></span> <span data-ttu-id="3e181-135">Die Länge des Pfads muss weniger als 260 Zeichen umfassen.</span><span class="sxs-lookup"><span data-stu-id="3e181-135">The length of the path must be less than 260 characters.</span></span><br/>     |
| <dl> <span data-ttu-id="3e181-136"><dt>VM \_ E \_ Pref \_ nicht \_ gefunden</dt> <dt>0xa0040300</dt></span><span class="sxs-lookup"><span data-stu-id="3e181-136"><dt>VM\_E\_PREF\_NOT\_FOUND</dt> <dt>0xA0040300</dt></span></span> </dl>                       | <span data-ttu-id="3e181-137">Die Einstellung wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="3e181-137">The preference was not found.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="3e181-138"><dt>VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="3e181-138"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="3e181-139">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="3e181-139">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                        |
| <dl> <span data-ttu-id="3e181-140"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3e181-140"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="3e181-141">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="3e181-141">An unexpected error has occurred.</span></span><br/>                                                                                           |



## <a name="requirements"></a><span data-ttu-id="3e181-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e181-142">Requirements</span></span>



| <span data-ttu-id="3e181-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e181-143">Requirement</span></span> | <span data-ttu-id="3e181-144">Wert</span><span class="sxs-lookup"><span data-stu-id="3e181-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e181-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e181-145">Minimum supported client</span></span><br/> | <span data-ttu-id="3e181-146">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e181-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e181-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e181-147">Minimum supported server</span></span><br/> | <span data-ttu-id="3e181-148">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3e181-148">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3e181-149">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="3e181-149">End of client support</span></span><br/>    | <span data-ttu-id="3e181-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3e181-150">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3e181-151">Produkt</span><span class="sxs-lookup"><span data-stu-id="3e181-151">Product</span></span><br/>                  | <span data-ttu-id="3e181-152">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3e181-152">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3e181-153">Header</span><span class="sxs-lookup"><span data-stu-id="3e181-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e181-154"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e181-154"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3e181-155">IID</span><span class="sxs-lookup"><span data-stu-id="3e181-155">IID</span></span><br/>                      | <span data-ttu-id="3e181-156">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="3e181-156">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="3e181-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e181-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e181-158">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="3e181-158">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

