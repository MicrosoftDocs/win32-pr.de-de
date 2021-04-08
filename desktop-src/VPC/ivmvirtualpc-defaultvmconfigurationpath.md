---
title: Ivmvirtualpc defaultvmconfigurationpath-Eigenschaft (vpccominterfaces. h)
description: Standardverzeichnis, das nach verfügbaren Konfigurationsdateien für virtuelle Maschinen durchsucht werden soll.
ms.assetid: 9ae63198-e3f6-4dcb-8edb-85adfbbdca26
keywords:
- Defaultvmconfigurationpath-Eigenschaft virtueller PC
- Defaultvmconfigurationpath-Eigenschaft Virtual PC, ivmvirtualpc-Schnittstelle
- Ivmvirtualpc Interface Virtual PC, defaultvmconfigurationpath (Eigenschaft)
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
ms.openlocfilehash: e13fc2323cb15bdbeb8c42e61810a376e49b3988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742729"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a><span data-ttu-id="4218c-106">Ivmvirtualpc::D efaultvmconfigurationpath-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4218c-106">IVMVirtualPC::DefaultVMConfigurationPath property</span></span>

<span data-ttu-id="4218c-107">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4218c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4218c-108">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4218c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4218c-109">Ruft das Standardverzeichnis ab, das nach verfügbaren Konfigurationsdateien für virtuelle Maschinen gesucht werden soll, und legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="4218c-109">Retrieves and sets the default directory to be searched for available virtual machine configuration files.</span></span>

<span data-ttu-id="4218c-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4218c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4218c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="4218c-111">Syntax</span></span>


```C++
HRESULT put_DefaultVMConfigurationPath(
  [in]          BSTR configurationPath
);

HRESULT get_DefaultVMConfigurationPath(
  [out, retval] BSTR *configurationPath
);
```



## <a name="property-value"></a><span data-ttu-id="4218c-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4218c-112">Property value</span></span>

<span data-ttu-id="4218c-113">Gibt den Verzeichnispfad für die Standard Konfigurationsdateien der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="4218c-113">Specifies the directory path for the default virtual machine configuration files.</span></span> <span data-ttu-id="4218c-114">In der Pfad Zeichenfolge wird ein umgekehrter Schrägstrich ( \) möglicherweise direkt vor dem abschließenden NULL-Zeichen angezeigt).</span><span class="sxs-lookup"><span data-stu-id="4218c-114">In the path string, a backslash (\) may appear immediately before the terminating null character.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4218c-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="4218c-115">Error codes</span></span>



| <span data-ttu-id="4218c-116">Name/Wert</span><span class="sxs-lookup"><span data-stu-id="4218c-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="4218c-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4218c-117">Meaning</span></span>                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4218c-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4218c-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="4218c-119">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="4218c-119">The operation was successful.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="4218c-120"><dt>E \_ Zeiger</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4218c-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="4218c-121">Der *ConfigurationPath* -Parameter ist **null**.</span><span class="sxs-lookup"><span data-stu-id="4218c-121">The *configurationPath* parameter is **NULL**.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="4218c-122"><dt>HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="4218c-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="4218c-123">Das System kann das vom *ConfigurationPath* -Parameter angegebene Verzeichnis nicht finden.</span><span class="sxs-lookup"><span data-stu-id="4218c-123">The system cannot find the directory specified by the *configurationPath* parameter.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="4218c-124"><dt>HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="4218c-124"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="4218c-125">Das System kann den vom *ConfigurationPath* -Parameter angegebenen Pfad nicht finden.</span><span class="sxs-lookup"><span data-stu-id="4218c-125">The system cannot find the path specified by the *configurationPath* parameter.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="4218c-126"><dt>HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="4218c-126"><dt>HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="4218c-127">Der *ConfigurationPath* -Parameter enthält ein ungültiges Zeichen (eines der folgenden Zeichen: " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="4218c-127">The *configurationPath* parameter contains an invalid character (one of the following: "\*?<>/\|":").</span></span><br/>                                   |
| <dl> <span data-ttu-id="4218c-128"><dt>HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="4218c-128"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="4218c-129">Der *ConfigurationPath* -Parameter gibt einen leeren oder relativen Pfad an.</span><span class="sxs-lookup"><span data-stu-id="4218c-129">The *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="4218c-130">Ein absoluter Pfad ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4218c-130">An absolute path is required.</span></span><br/>                                          |
| <dl> <span data-ttu-id="4218c-131"><dt>HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="4218c-131"><dt>HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="4218c-132">Der vom *ConfigurationPath* -Parameter angegebene Pfad ist zu lang.</span><span class="sxs-lookup"><span data-stu-id="4218c-132">The path specified by the *configurationPath* parameter is too long.</span></span> <span data-ttu-id="4218c-133">Die Länge des Pfads muss kleiner als der **Maximale \_ Pfad** (260) sein.</span><span class="sxs-lookup"><span data-stu-id="4218c-133">The length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="4218c-134"><dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4218c-134"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="4218c-135">Ein unerwarteter Fehler ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="4218c-135">An unexpected error has occurred.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="4218c-136"><dt>VM \_ E \_ \_ Hardwarevirtualisierung \_ deaktiviert</dt> <dt>0xa0040951</dt></span><span class="sxs-lookup"><span data-stu-id="4218c-136"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="4218c-137">Der Prozessor bietet keine Unterstützung für hav-Erweiterungen (Hardware Beschleunigung Virtualization).</span><span class="sxs-lookup"><span data-stu-id="4218c-137">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                          |



## <a name="remarks"></a><span data-ttu-id="4218c-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4218c-138">Remarks</span></span>

<span data-ttu-id="4218c-139">Standardmäßig ist dieser Eigenschafts Wert auf das folgende Verzeichnis festgelegt: "% LocalAppData% \\ Microsoft \\ Windows Virtual PC \\ Virtual Machines \\ ".</span><span class="sxs-lookup"><span data-stu-id="4218c-139">By default, this property value is set to the following directory: "%LocalAppData%\\Microsoft\\Windows Virtual PC\\Virtual Machines\\".</span></span>

## <a name="requirements"></a><span data-ttu-id="4218c-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4218c-140">Requirements</span></span>



| <span data-ttu-id="4218c-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4218c-141">Requirement</span></span> | <span data-ttu-id="4218c-142">Wert</span><span class="sxs-lookup"><span data-stu-id="4218c-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4218c-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4218c-143">Minimum supported client</span></span><br/> | <span data-ttu-id="4218c-144">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4218c-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4218c-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4218c-145">Minimum supported server</span></span><br/> | <span data-ttu-id="4218c-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4218c-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4218c-147">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="4218c-147">End of client support</span></span><br/>    | <span data-ttu-id="4218c-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4218c-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4218c-149">Produkt</span><span class="sxs-lookup"><span data-stu-id="4218c-149">Product</span></span><br/>                  | <span data-ttu-id="4218c-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4218c-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4218c-151">Header</span><span class="sxs-lookup"><span data-stu-id="4218c-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="4218c-152"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4218c-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4218c-153">IID</span><span class="sxs-lookup"><span data-stu-id="4218c-153">IID</span></span><br/>                      | <span data-ttu-id="4218c-154">IID \_ ivmvirtualpc ist als 236ba0d9-a24a-4292-A132-27c1421dfd01 definiert.</span><span class="sxs-lookup"><span data-stu-id="4218c-154">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="4218c-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4218c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4218c-156">**Ivmvirtualpc**</span><span class="sxs-lookup"><span data-stu-id="4218c-156">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

