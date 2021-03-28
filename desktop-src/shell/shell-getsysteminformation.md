---
description: Ruft Systeminformationen ab.
ms.assetid: 94C10DD6-FE49-4dd4-AEED-69B73A75EDEF
title: Shell. getsysteminformation-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 2ad7a865ba6ac5b62bc8a9b5ac105c0ef166d574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980625"
---
# <a name="shellgetsysteminformation-method"></a><span data-ttu-id="7730f-103">Shell. getsysteminformation-Methode</span><span class="sxs-lookup"><span data-stu-id="7730f-103">Shell.GetSystemInformation method</span></span>

<span data-ttu-id="7730f-104">Ruft Systeminformationen ab.</span><span class="sxs-lookup"><span data-stu-id="7730f-104">Retrieves system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="7730f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7730f-105">Syntax</span></span>


```JScript
retVal = Shell.GetSystemInformation(
  sName
)
```


```VB

Shell.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="7730f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7730f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7730f-107">*sname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7730f-107">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7730f-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="7730f-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="7730f-109">Eine **Zeichenfolge** , die die angeforderten Systeminformationen angibt.</span><span class="sxs-lookup"><span data-stu-id="7730f-109">A **String** that specifies the system information that is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7730f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7730f-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="7730f-111">JScript</span><span class="sxs-lookup"><span data-stu-id="7730f-111">JScript</span></span>

<span data-ttu-id="7730f-112">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="7730f-112">Type: **Variant**</span></span>

<span data-ttu-id="7730f-113">Gibt den Wert der angeforderten Systeminformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="7730f-113">Returns the value of the requested system information.</span></span> <span data-ttu-id="7730f-114">Der Rückgabetyp hängt davon ab, welche Systeminformationen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="7730f-114">The return type depends on which system information is requested.</span></span> <span data-ttu-id="7730f-115">Weitere Informationen finden Sie im Abschnitt Hinweise.</span><span class="sxs-lookup"><span data-stu-id="7730f-115">See the Remarks section for details.</span></span>

### <a name="vb"></a><span data-ttu-id="7730f-116">VB</span><span class="sxs-lookup"><span data-stu-id="7730f-116">VB</span></span>

<span data-ttu-id="7730f-117">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="7730f-117">Type: **Variant**</span></span>

<span data-ttu-id="7730f-118">Gibt den Wert der angeforderten Systeminformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="7730f-118">Returns the value of the requested system information.</span></span> <span data-ttu-id="7730f-119">Der Rückgabetyp hängt davon ab, welche Systeminformationen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="7730f-119">The return type depends on which system information is requested.</span></span> <span data-ttu-id="7730f-120">Weitere Informationen finden Sie im Abschnitt Hinweise.</span><span class="sxs-lookup"><span data-stu-id="7730f-120">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="7730f-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7730f-121">Remarks</span></span>

<span data-ttu-id="7730f-122">Diese Methode kann verwendet werden, um viele System Informationswerte anzufordern.</span><span class="sxs-lookup"><span data-stu-id="7730f-122">This method can be used to request many system information values.</span></span> <span data-ttu-id="7730f-123">In der folgenden Tabelle wird der *sname* -Wert, der zum Anfordern der Informationen verwendet wird, und der zugehörige Typ des zurückgegebenen Werts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7730f-123">The following table gives the *sName* value that is used to request the information and the associated type of the returned value.</span></span>



<span data-ttu-id="7730f-124">*sName*</span><span class="sxs-lookup"><span data-stu-id="7730f-124">*sName*</span></span>

<span data-ttu-id="7730f-125">Rückgabetyp</span><span class="sxs-lookup"><span data-stu-id="7730f-125">Return type</span></span>

<span data-ttu-id="7730f-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7730f-126">Description</span></span>

<span data-ttu-id="7730f-127">Director Service Available</span><span class="sxs-lookup"><span data-stu-id="7730f-127">DirectoryServiceAvailable</span></span>

<span data-ttu-id="7730f-128">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="7730f-128">**Boolean**</span></span>

<span data-ttu-id="7730f-129">Auf " **true** " festgelegt, wenn der Verzeichnisdienst verfügbar ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="7730f-129">Set to **true** if the directory service is available; otherwise, **false**.</span></span>

<span data-ttu-id="7730f-130">DoubleClickTime</span><span class="sxs-lookup"><span data-stu-id="7730f-130">DoubleClickTime</span></span>

<span data-ttu-id="7730f-131">**Integer**</span><span class="sxs-lookup"><span data-stu-id="7730f-131">**Integer**</span></span>

<span data-ttu-id="7730f-132">Die Doppelklick Zeit in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="7730f-132">The double-click time, in milliseconds.</span></span>

<span data-ttu-id="7730f-133">ProcessorLevel</span><span class="sxs-lookup"><span data-stu-id="7730f-133">ProcessorLevel</span></span>

<span data-ttu-id="7730f-134">**Integer**</span><span class="sxs-lookup"><span data-stu-id="7730f-134">**Integer**</span></span>

<span data-ttu-id="7730f-135">**Windows Vista und** höher.</span><span class="sxs-lookup"><span data-stu-id="7730f-135">**Windows Vista and later**.</span></span> <span data-ttu-id="7730f-136">Die Prozessor Ebene.</span><span class="sxs-lookup"><span data-stu-id="7730f-136">The processor level.</span></span> <span data-ttu-id="7730f-137">Gibt 3, 4 oder 5 für Prozessoren der x386-, x486-und Pentium-Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="7730f-137">Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</span></span>

<span data-ttu-id="7730f-138">ProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="7730f-138">ProcessorSpeed</span></span>

<span data-ttu-id="7730f-139">**Integer**</span><span class="sxs-lookup"><span data-stu-id="7730f-139">**Integer**</span></span>

<span data-ttu-id="7730f-140">Die Prozessorgeschwindigkeit in Megahertz (MHz).</span><span class="sxs-lookup"><span data-stu-id="7730f-140">The processor speed, in megahertz (MHz).</span></span>

<span data-ttu-id="7730f-141">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="7730f-141">ProcessorArchitecture</span></span>

<span data-ttu-id="7730f-142">**Integer**</span><span class="sxs-lookup"><span data-stu-id="7730f-142">**Integer**</span></span>

<span data-ttu-id="7730f-143">Die Prozessorarchitektur.</span><span class="sxs-lookup"><span data-stu-id="7730f-143">The processor architecture.</span></span> <span data-ttu-id="7730f-144">Weitere Informationen finden Sie in der Erörterung des **wprocessorarchitecture** -Members der [**System \_ Info**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7730f-144">For details, see the discussion of the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span>

<span data-ttu-id="7730f-145">Physicalmemoryinstalliert</span><span class="sxs-lookup"><span data-stu-id="7730f-145">PhysicalMemoryInstalled</span></span>

<span data-ttu-id="7730f-146">**Integer**</span><span class="sxs-lookup"><span data-stu-id="7730f-146">**Integer**</span></span>

<span data-ttu-id="7730f-147">Die Menge des installierten physischen Speichers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="7730f-147">The amount of physical memory installed, in bytes.</span></span>

<span data-ttu-id="7730f-148">Folgendes gilt nur für Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7730f-148">The following are valid only on Windows XP.</span></span>

<span data-ttu-id="7730f-149">ISOS \_ Professional</span><span class="sxs-lookup"><span data-stu-id="7730f-149">IsOS\_Professional</span></span>

<span data-ttu-id="7730f-150">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="7730f-150">**Boolean**</span></span>

<span data-ttu-id="7730f-151">Auf " **true** " festgelegt, wenn das Betriebssystem Windows XP Professional Edition ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="7730f-151">Set to **true** if the operating system is Windows XP Professional Edition; otherwise, **false**.</span></span>

<span data-ttu-id="7730f-152">ISOS \_ persönlich</span><span class="sxs-lookup"><span data-stu-id="7730f-152">IsOS\_Personal</span></span>

<span data-ttu-id="7730f-153">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="7730f-153">**Boolean**</span></span>

<span data-ttu-id="7730f-154">Auf " **true** " festgelegt, wenn das Betriebssystem Windows XP Home Edition ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="7730f-154">Set to **true** if the operating system is Windows XP Home Edition; otherwise, **false**.</span></span>

<span data-ttu-id="7730f-155">Folgendes gilt nur für Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="7730f-155">The following is valid only on Windows XP and later.</span></span>

<span data-ttu-id="7730f-156">ISOS- \_ domainmember</span><span class="sxs-lookup"><span data-stu-id="7730f-156">IsOS\_DomainMember</span></span>

<span data-ttu-id="7730f-157">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="7730f-157">**Boolean**</span></span>

<span data-ttu-id="7730f-158">Auf " **true** " festgelegt, wenn der Computer Mitglied einer Domäne ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="7730f-158">Set to **true** if the computer is a member of a domain; otherwise, **false**.</span></span>



 

<span data-ttu-id="7730f-159">Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7730f-159">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="7730f-160">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7730f-160">Examples</span></span>

<span data-ttu-id="7730f-161">In den folgenden Beispielen wird die Verwendung von **getsysteminformation** für JScript und VBScript veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="7730f-161">The following examples show the use of **GetSystemInformation** for JScript and VBScript.</span></span>

<span data-ttu-id="7730f-162">JScript</span><span class="sxs-lookup"><span data-stu-id="7730f-162">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnGetSystemInformationJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;

        vReturn = objShell.GetSystemInformation("ProcessorLevel");
        document.write(vReturn);
    }
</script>
```



<span data-ttu-id="7730f-163">VBScript</span><span class="sxs-lookup"><span data-stu-id="7730f-163">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnGetSystemInformationVB()
        dim objShell
        dim vReturn

        set objShell = CreateObject("shell.application")

        vReturn = objShell.GetSystemInformation("ProcessorLevel")
        document.write(vReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="7730f-164">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7730f-164">Requirements</span></span>



| <span data-ttu-id="7730f-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7730f-165">Requirement</span></span> | <span data-ttu-id="7730f-166">Wert</span><span class="sxs-lookup"><span data-stu-id="7730f-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7730f-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7730f-167">Minimum supported client</span></span><br/> | <span data-ttu-id="7730f-168">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7730f-168">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7730f-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7730f-169">Minimum supported server</span></span><br/> | <span data-ttu-id="7730f-170">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7730f-170">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7730f-171">Header</span><span class="sxs-lookup"><span data-stu-id="7730f-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="7730f-172"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7730f-172"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="7730f-173">IDL</span><span class="sxs-lookup"><span data-stu-id="7730f-173">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7730f-174"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7730f-174"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="7730f-175">DLL</span><span class="sxs-lookup"><span data-stu-id="7730f-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7730f-176"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="7730f-176"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
