---
description: Ruft Systeminformationen ab.
ms.assetid: 57c066e3-080f-4ecc-b56e-877f0569e901
title: IShellDispatch2. getsysteminformation-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 624c7383d458f20a13f0e2249ec302181fc4a7ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863139"
---
# <a name="ishelldispatch2getsysteminformation-method"></a><span data-ttu-id="880cb-103">IShellDispatch2. getsysteminformation-Methode</span><span class="sxs-lookup"><span data-stu-id="880cb-103">IShellDispatch2.GetSystemInformation method</span></span>

<span data-ttu-id="880cb-104">Ruft Systeminformationen ab.</span><span class="sxs-lookup"><span data-stu-id="880cb-104">Retrieves system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="880cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="880cb-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.GetSystemInformation(
  sName
)
```


```VB

IShellDispatch2.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="880cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="880cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="880cb-107">*sname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="880cb-107">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="880cb-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="880cb-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="880cb-109">Eine **Zeichenfolge** , die die angeforderten Systeminformationen angibt.</span><span class="sxs-lookup"><span data-stu-id="880cb-109">A **String** that specifies the system information that is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="880cb-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="880cb-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="880cb-111">JScript</span><span class="sxs-lookup"><span data-stu-id="880cb-111">JScript</span></span>

<span data-ttu-id="880cb-112">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="880cb-112">Type: **Variant**</span></span>

<span data-ttu-id="880cb-113">Gibt den Wert der angeforderten Systeminformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="880cb-113">Returns the value of the requested system information.</span></span> <span data-ttu-id="880cb-114">Der Rückgabetyp hängt davon ab, welche Systeminformationen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="880cb-114">The return type depends on which system information is requested.</span></span> <span data-ttu-id="880cb-115">Weitere Informationen finden Sie im Abschnitt Hinweise.</span><span class="sxs-lookup"><span data-stu-id="880cb-115">See the Remarks section for details.</span></span>

### <a name="vb"></a><span data-ttu-id="880cb-116">VB</span><span class="sxs-lookup"><span data-stu-id="880cb-116">VB</span></span>

<span data-ttu-id="880cb-117">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="880cb-117">Type: **Variant**</span></span>

<span data-ttu-id="880cb-118">Gibt den Wert der angeforderten Systeminformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="880cb-118">Returns the value of the requested system information.</span></span> <span data-ttu-id="880cb-119">Der Rückgabetyp hängt davon ab, welche Systeminformationen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="880cb-119">The return type depends on which system information is requested.</span></span> <span data-ttu-id="880cb-120">Weitere Informationen finden Sie im Abschnitt Hinweise.</span><span class="sxs-lookup"><span data-stu-id="880cb-120">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="880cb-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="880cb-121">Remarks</span></span>

<span data-ttu-id="880cb-122">Diese Methode wird implementiert und über die [**Shell. getsysteminformation**](./shell-getsysteminformation.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="880cb-122">This method is implemented and accessed through the [**Shell.GetSystemInformation**](./shell-getsysteminformation.md) method.</span></span>

<span data-ttu-id="880cb-123">Diese Methode kann verwendet werden, um viele System Informationswerte anzufordern.</span><span class="sxs-lookup"><span data-stu-id="880cb-123">This method can be used to request many system information values.</span></span> <span data-ttu-id="880cb-124">In der folgenden Tabelle wird der *sname* -Wert, der zum Anfordern der Informationen verwendet wird, und der zugehörige Typ des zurückgegebenen Werts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="880cb-124">The following table gives the *sName* value that is used to request the information and the associated type of the returned value.</span></span>



<span data-ttu-id="880cb-125">*sName*</span><span class="sxs-lookup"><span data-stu-id="880cb-125">*sName*</span></span>

<span data-ttu-id="880cb-126">Rückgabetyp</span><span class="sxs-lookup"><span data-stu-id="880cb-126">Return type</span></span>

<span data-ttu-id="880cb-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="880cb-127">Description</span></span>

<span data-ttu-id="880cb-128">Director Service Available</span><span class="sxs-lookup"><span data-stu-id="880cb-128">DirectoryServiceAvailable</span></span>

<span data-ttu-id="880cb-129">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="880cb-129">**Boolean**</span></span>

<span data-ttu-id="880cb-130">Auf " **true** " festgelegt, wenn der Verzeichnisdienst verfügbar ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="880cb-130">Set to **true** if the directory service is available; otherwise, **false**.</span></span>

<span data-ttu-id="880cb-131">DoubleClickTime</span><span class="sxs-lookup"><span data-stu-id="880cb-131">DoubleClickTime</span></span>

<span data-ttu-id="880cb-132">**Integer**</span><span class="sxs-lookup"><span data-stu-id="880cb-132">**Integer**</span></span>

<span data-ttu-id="880cb-133">Die Doppelklick Zeit in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="880cb-133">The double-click time, in milliseconds.</span></span>

<span data-ttu-id="880cb-134">ProcessorLevel</span><span class="sxs-lookup"><span data-stu-id="880cb-134">ProcessorLevel</span></span>

<span data-ttu-id="880cb-135">**Integer**</span><span class="sxs-lookup"><span data-stu-id="880cb-135">**Integer**</span></span>

<span data-ttu-id="880cb-136">**Windows Vista und** höher.</span><span class="sxs-lookup"><span data-stu-id="880cb-136">**Windows Vista and later**.</span></span> <span data-ttu-id="880cb-137">Die Prozessor Ebene.</span><span class="sxs-lookup"><span data-stu-id="880cb-137">The processor level.</span></span> <span data-ttu-id="880cb-138">Gibt 3, 4 oder 5 für Prozessoren der x386-, x486-und Pentium-Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="880cb-138">Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</span></span>

<span data-ttu-id="880cb-139">ProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="880cb-139">ProcessorSpeed</span></span>

<span data-ttu-id="880cb-140">**Integer**</span><span class="sxs-lookup"><span data-stu-id="880cb-140">**Integer**</span></span>

<span data-ttu-id="880cb-141">Die Prozessorgeschwindigkeit in Megahertz (MHz).</span><span class="sxs-lookup"><span data-stu-id="880cb-141">The processor speed, in megahertz (MHz).</span></span>

<span data-ttu-id="880cb-142">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="880cb-142">ProcessorArchitecture</span></span>

<span data-ttu-id="880cb-143">**Integer**</span><span class="sxs-lookup"><span data-stu-id="880cb-143">**Integer**</span></span>

<span data-ttu-id="880cb-144">Die Prozessorarchitektur.</span><span class="sxs-lookup"><span data-stu-id="880cb-144">The processor architecture.</span></span> <span data-ttu-id="880cb-145">Weitere Informationen finden Sie in der Erörterung des **wprocessorarchitecture** -Members der [**System \_ Info**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="880cb-145">For details, see the discussion of the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span>

<span data-ttu-id="880cb-146">Physicalmemoryinstalliert</span><span class="sxs-lookup"><span data-stu-id="880cb-146">PhysicalMemoryInstalled</span></span>

<span data-ttu-id="880cb-147">**Integer**</span><span class="sxs-lookup"><span data-stu-id="880cb-147">**Integer**</span></span>

<span data-ttu-id="880cb-148">Die Menge des installierten physischen Speichers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="880cb-148">The amount of physical memory installed, in bytes.</span></span>

<span data-ttu-id="880cb-149">Folgendes gilt nur für Windows XP.</span><span class="sxs-lookup"><span data-stu-id="880cb-149">The following are valid only on Windows XP.</span></span>

<span data-ttu-id="880cb-150">ISOS \_ Professional</span><span class="sxs-lookup"><span data-stu-id="880cb-150">IsOS\_Professional</span></span>

<span data-ttu-id="880cb-151">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="880cb-151">**Boolean**</span></span>

<span data-ttu-id="880cb-152">Auf " **true** " festgelegt, wenn das Betriebssystem Windows XP Professional Edition ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="880cb-152">Set to **true** if the operating system is Windows XP Professional Edition; otherwise, **false**.</span></span>

<span data-ttu-id="880cb-153">ISOS \_ persönlich</span><span class="sxs-lookup"><span data-stu-id="880cb-153">IsOS\_Personal</span></span>

<span data-ttu-id="880cb-154">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="880cb-154">**Boolean**</span></span>

<span data-ttu-id="880cb-155">Auf " **true** " festgelegt, wenn das Betriebssystem Windows XP Home Edition ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="880cb-155">Set to **true** if the operating system is Windows XP Home Edition; otherwise, **false**.</span></span>

<span data-ttu-id="880cb-156">Folgendes gilt nur für Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="880cb-156">The following is valid only on Windows XP and later.</span></span>

<span data-ttu-id="880cb-157">ISOS- \_ domainmember</span><span class="sxs-lookup"><span data-stu-id="880cb-157">IsOS\_DomainMember</span></span>

<span data-ttu-id="880cb-158">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="880cb-158">**Boolean**</span></span>

<span data-ttu-id="880cb-159">Auf " **true** " festgelegt, wenn der Computer Mitglied einer Domäne ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="880cb-159">Set to **true** if the computer is a member of a domain; otherwise, **false**.</span></span>



 

<span data-ttu-id="880cb-160">Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.</span><span class="sxs-lookup"><span data-stu-id="880cb-160">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="880cb-161">Beispiele</span><span class="sxs-lookup"><span data-stu-id="880cb-161">Examples</span></span>

<span data-ttu-id="880cb-162">In den folgenden Beispielen wird die Verwendung von **getsysteminformation** für JScript und VBScript veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="880cb-162">The following examples show the use of **GetSystemInformation** for JScript and VBScript.</span></span>

<span data-ttu-id="880cb-163">JScript</span><span class="sxs-lookup"><span data-stu-id="880cb-163">JScript:</span></span>


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



<span data-ttu-id="880cb-164">VBScript</span><span class="sxs-lookup"><span data-stu-id="880cb-164">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="880cb-165">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="880cb-165">Requirements</span></span>



| <span data-ttu-id="880cb-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="880cb-166">Requirement</span></span> | <span data-ttu-id="880cb-167">Wert</span><span class="sxs-lookup"><span data-stu-id="880cb-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="880cb-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="880cb-168">Minimum supported client</span></span><br/> | <span data-ttu-id="880cb-169">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="880cb-169">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="880cb-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="880cb-170">Minimum supported server</span></span><br/> | <span data-ttu-id="880cb-171">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="880cb-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="880cb-172">Header</span><span class="sxs-lookup"><span data-stu-id="880cb-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="880cb-173"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="880cb-173"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="880cb-174">IDL</span><span class="sxs-lookup"><span data-stu-id="880cb-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="880cb-175"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="880cb-175"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="880cb-176">DLL</span><span class="sxs-lookup"><span data-stu-id="880cb-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="880cb-177"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="880cb-177"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
