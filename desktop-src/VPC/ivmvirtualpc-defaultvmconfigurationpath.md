---
title: IVMVirtualPC DefaultVMConfigurationPath-Eigenschaft (VPCCOMInterfaces.h)
description: Standardverzeichnis, das nach verfügbaren Konfigurationsdateien für virtuelle Computer durchsucht werden soll.
ms.assetid: 9ae63198-e3f6-4dcb-8edb-85adfbbdca26
keywords:
- DefaultVMConfigurationPath-Eigenschaft Virtueller PC
- DefaultVMConfigurationPath-Eigenschaft Virtueller PC, IVMVirtualPC-Schnittstelle
- IVMVirtualPC-Schnittstelle Virtueller PC, DefaultVMConfigurationPath-Eigenschaft
topic_type:
- apiref
api_name:
- IVMVirtualPC.DefaultVMConfigurationPath
- IVMVirtualPC.get_DefaultVMConfigurationPath
- IVMVirtualPC.put_DefaultVMConfigurationPath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09f6370dfb868ec386e05f361240a74412f13a7d
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387636"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a><span data-ttu-id="77ea7-106">IVMVirtualPC::D efaultVMConfigurationPath (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="77ea7-106">IVMVirtualPC::DefaultVMConfigurationPath property</span></span>

<span data-ttu-id="77ea7-107">\[Der virtuelle Windows-PC kann ab diesem Windows 8.</span><span class="sxs-lookup"><span data-stu-id="77ea7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="77ea7-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]</span><span class="sxs-lookup"><span data-stu-id="77ea7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="77ea7-109">Ruft das Standardverzeichnis ab, das nach verfügbaren Konfigurationsdateien für virtuelle Computer durchsucht werden soll, und legt es fest.</span><span class="sxs-lookup"><span data-stu-id="77ea7-109">Retrieves and sets the default directory to be searched for available virtual machine configuration files.</span></span>

<span data-ttu-id="77ea7-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="77ea7-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="77ea7-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="77ea7-111">Syntax</span></span>


```C++
HRESULT put_DefaultVMConfigurationPath(
  [in]          BSTR configurationPath
);

HRESULT get_DefaultVMConfigurationPath(
  [out, retval] BSTR *configurationPath
);
```



## <a name="property-value"></a><span data-ttu-id="77ea7-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="77ea7-112">Property value</span></span>

<span data-ttu-id="77ea7-113">Gibt den Verzeichnispfad für die Standardkonfigurationsdateien des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="77ea7-113">Specifies the directory path for the default virtual machine configuration files.</span></span> <span data-ttu-id="77ea7-114">In der Pfadzeichenfolge kann ein zurücker Schrägstrich ( ) unmittelbar vor dem beendenden \\ NULL-Zeichen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="77ea7-114">In the path string, a backslash (\\) may appear immediately before the terminating null character.</span></span>

## <a name="error-codes"></a><span data-ttu-id="77ea7-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="77ea7-115">Error codes</span></span>



| <span data-ttu-id="77ea7-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="77ea7-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="77ea7-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="77ea7-117">Meaning</span></span>                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="77ea7-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="77ea7-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="77ea7-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="77ea7-119">The operation was successful.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="77ea7-120"><dt>E \_ ZEIGER 0X80004003</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="77ea7-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="77ea7-121">Der *configurationPath-Parameter* ist **NULL.**</span><span class="sxs-lookup"><span data-stu-id="77ea7-121">The *configurationPath* parameter is **NULL**.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="77ea7-122"><dt>HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)</dt> <dt>0X80070002</dt></span><span class="sxs-lookup"><span data-stu-id="77ea7-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="77ea7-123">Das vom configurationPath-Parameter angegebene Verzeichnis kann vom *System nicht finden.*</span><span class="sxs-lookup"><span data-stu-id="77ea7-123">The system cannot find the directory specified by the *configurationPath* parameter.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="77ea7-124"><dt>HRESULT \_ FROM \_ WIN32(ERROR \_ PATH NOT \_ \_ FOUND)</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="77ea7-124"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="77ea7-125">Das System kann den durch den *configurationPath-Parameter angegebenen Pfad nicht* finden.</span><span class="sxs-lookup"><span data-stu-id="77ea7-125">The system cannot find the path specified by the *configurationPath* parameter.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="77ea7-126"><dt>HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="77ea7-126"><dt>HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="77ea7-127">Der *parameter configurationPath* enthält ein ungültiges Zeichen (eines der folgenden Zeichen: " \* ?<>/ \| ":").</span><span class="sxs-lookup"><span data-stu-id="77ea7-127">The *configurationPath* parameter contains an invalid character (one of the following: "\*?<>/\|":").</span></span><br/>                                   |
| <dl> <span data-ttu-id="77ea7-128"><dt>HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="77ea7-128"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="77ea7-129">Der *configurationPath-Parameter* gibt einen leeren oder relativen Pfad an.</span><span class="sxs-lookup"><span data-stu-id="77ea7-129">The *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="77ea7-130">Ein absoluter Pfad ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="77ea7-130">An absolute path is required.</span></span><br/>                                          |
| <dl> <span data-ttu-id="77ea7-131"><dt>HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="77ea7-131"><dt>HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="77ea7-132">Der vom *configurationPath-Parameter angegebene Pfad* ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="77ea7-132">The path specified by the *configurationPath* parameter is too long.</span></span> <span data-ttu-id="77ea7-133">Die Länge des Pfads muss kleiner als **MAX \_ PATH** (260) Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="77ea7-133">The length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="77ea7-134"><dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="77ea7-134"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="77ea7-135">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="77ea7-135">An unexpected error has occurred.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="77ea7-136"><dt>VM \_ E \_ \_ HARDWAREVIRTUALISIERUNG \_ DEAKTIVIERT</dt> <dt>0XA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="77ea7-136"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="77ea7-137">Der Prozessor unterstützt keine HAV-Erweiterungen (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="77ea7-137">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                          |



## <a name="remarks"></a><span data-ttu-id="77ea7-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="77ea7-138">Remarks</span></span>

<span data-ttu-id="77ea7-139">Standardmäßig ist dieser Eigenschaftswert auf das folgende Verzeichnis festgelegt: "%LocalAppData% \\ Microsoft Windows Virtual PC Virtual Machines \\ \\ \\ ".</span><span class="sxs-lookup"><span data-stu-id="77ea7-139">By default, this property value is set to the following directory: "%LocalAppData%\\Microsoft\\Windows Virtual PC\\Virtual Machines\\".</span></span>

## <a name="requirements"></a><span data-ttu-id="77ea7-140">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="77ea7-140">Requirements</span></span>



| <span data-ttu-id="77ea7-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77ea7-141">Requirement</span></span> | <span data-ttu-id="77ea7-142">Wert</span><span class="sxs-lookup"><span data-stu-id="77ea7-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="77ea7-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77ea7-143">Minimum supported client</span></span><br/> | <span data-ttu-id="77ea7-144">Nur Windows \[ 7-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77ea7-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="77ea7-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77ea7-145">Minimum supported server</span></span><br/> | <span data-ttu-id="77ea7-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="77ea7-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="77ea7-147">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="77ea7-147">End of client support</span></span><br/>    | <span data-ttu-id="77ea7-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="77ea7-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="77ea7-149">Produkt</span><span class="sxs-lookup"><span data-stu-id="77ea7-149">Product</span></span><br/>                  | <span data-ttu-id="77ea7-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="77ea7-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="77ea7-151">Header</span><span class="sxs-lookup"><span data-stu-id="77ea7-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="77ea7-152"><dt>VPCCOMInterfaces.h</dt></span><span class="sxs-lookup"><span data-stu-id="77ea7-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="77ea7-153">IID</span><span class="sxs-lookup"><span data-stu-id="77ea7-153">IID</span></span><br/>                      | <span data-ttu-id="77ea7-154">IID \_ IVMVirtualPC ist als 236ba0d9-a24a-4292-a132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="77ea7-154">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="77ea7-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77ea7-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77ea7-156">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="77ea7-156">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

