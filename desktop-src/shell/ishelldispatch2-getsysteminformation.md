---
description: 'IShellDispatch2.GetSystemInformation-Methode: Ruft Systeminformationen ab.'
ms.assetid: 57c066e3-080f-4ecc-b56e-877f0569e901
title: IShellDispatch2.GetSystemInformation-Methode (Shldisp.h)
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
ms.openlocfilehash: a81ac091dc1905c1cbcd2c41575c907ce957e60c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117108"
---
# <a name="ishelldispatch2getsysteminformation-method"></a><span data-ttu-id="b0653-103">IShellDispatch2.GetSystemInformation-Methode</span><span class="sxs-lookup"><span data-stu-id="b0653-103">IShellDispatch2.GetSystemInformation method</span></span>

<span data-ttu-id="b0653-104">Ruft Systeminformationen ab.</span><span class="sxs-lookup"><span data-stu-id="b0653-104">Retrieves system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0653-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0653-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="b0653-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0653-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0653-107">*sName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b0653-107">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0653-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="b0653-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="b0653-109">Eine **Zeichenfolge,** die die angeforderten Systeminformationen angibt.</span><span class="sxs-lookup"><span data-stu-id="b0653-109">A **String** that specifies the system information that is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0653-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0653-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b0653-111">JScript</span><span class="sxs-lookup"><span data-stu-id="b0653-111">JScript</span></span>

<span data-ttu-id="b0653-112">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="b0653-112">Type: **Variant**</span></span>

<span data-ttu-id="b0653-113">Gibt den Wert der angeforderten Systeminformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="b0653-113">Returns the value of the requested system information.</span></span> <span data-ttu-id="b0653-114">Der Rückgabetyp hängt davon ab, welche Systeminformationen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="b0653-114">The return type depends on which system information is requested.</span></span> <span data-ttu-id="b0653-115">Weitere Informationen finden Sie im Abschnitt Hinweise.</span><span class="sxs-lookup"><span data-stu-id="b0653-115">See the Remarks section for details.</span></span>

### <a name="vb"></a><span data-ttu-id="b0653-116">VB</span><span class="sxs-lookup"><span data-stu-id="b0653-116">VB</span></span>

<span data-ttu-id="b0653-117">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="b0653-117">Type: **Variant**</span></span>

<span data-ttu-id="b0653-118">Gibt den Wert der angeforderten Systeminformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="b0653-118">Returns the value of the requested system information.</span></span> <span data-ttu-id="b0653-119">Der Rückgabetyp hängt davon ab, welche Systeminformationen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="b0653-119">The return type depends on which system information is requested.</span></span> <span data-ttu-id="b0653-120">Weitere Informationen finden Sie im Abschnitt Hinweise.</span><span class="sxs-lookup"><span data-stu-id="b0653-120">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0653-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0653-121">Remarks</span></span>

<span data-ttu-id="b0653-122">Diese Methode wird implementiert und über die [**Shell.GetSystemInformation-Methode**](./shell-getsysteminformation.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b0653-122">This method is implemented and accessed through the [**Shell.GetSystemInformation**](./shell-getsysteminformation.md) method.</span></span>

<span data-ttu-id="b0653-123">Diese Methode kann verwendet werden, um viele Systeminformationswerte an fordern.</span><span class="sxs-lookup"><span data-stu-id="b0653-123">This method can be used to request many system information values.</span></span> <span data-ttu-id="b0653-124">Die folgende Tabelle enthält den *sName-Wert,* der zum Anfordern der Informationen verwendet wird, und den zugeordneten Typ des zurückgegebenen Werts.</span><span class="sxs-lookup"><span data-stu-id="b0653-124">The following table gives the *sName* value that is used to request the information and the associated type of the returned value.</span></span>



<span data-ttu-id="b0653-125">*sName*</span><span class="sxs-lookup"><span data-stu-id="b0653-125">*sName*</span></span>

<span data-ttu-id="b0653-126">Rückgabetyp</span><span class="sxs-lookup"><span data-stu-id="b0653-126">Return type</span></span>

<span data-ttu-id="b0653-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b0653-127">Description</span></span>

<span data-ttu-id="b0653-128">DirectoryServiceAvailable</span><span class="sxs-lookup"><span data-stu-id="b0653-128">DirectoryServiceAvailable</span></span>

<span data-ttu-id="b0653-129">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="b0653-129">**Boolean**</span></span>

<span data-ttu-id="b0653-130">Legen Sie auf **TRUE fest,** wenn der Verzeichnisdienst verfügbar ist. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="b0653-130">Set to **true** if the directory service is available; otherwise, **false**.</span></span>

<span data-ttu-id="b0653-131">DoubleClickTime</span><span class="sxs-lookup"><span data-stu-id="b0653-131">DoubleClickTime</span></span>

<span data-ttu-id="b0653-132">**Integer**</span><span class="sxs-lookup"><span data-stu-id="b0653-132">**Integer**</span></span>

<span data-ttu-id="b0653-133">Die Doppelklickzeit in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="b0653-133">The double-click time, in milliseconds.</span></span>

<span data-ttu-id="b0653-134">ProcessorLevel</span><span class="sxs-lookup"><span data-stu-id="b0653-134">ProcessorLevel</span></span>

<span data-ttu-id="b0653-135">**Integer**</span><span class="sxs-lookup"><span data-stu-id="b0653-135">**Integer**</span></span>

<span data-ttu-id="b0653-136">**Windows Vista und höher.**</span><span class="sxs-lookup"><span data-stu-id="b0653-136">**Windows Vista and later**.</span></span> <span data-ttu-id="b0653-137">Die Prozessorebene.</span><span class="sxs-lookup"><span data-stu-id="b0653-137">The processor level.</span></span> <span data-ttu-id="b0653-138">Gibt für Prozessoren auf x386-, x486- und Pentium-Ebene 3, 4 oder 5 zurück.</span><span class="sxs-lookup"><span data-stu-id="b0653-138">Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</span></span>

<span data-ttu-id="b0653-139">ProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="b0653-139">ProcessorSpeed</span></span>

<span data-ttu-id="b0653-140">**Integer**</span><span class="sxs-lookup"><span data-stu-id="b0653-140">**Integer**</span></span>

<span data-ttu-id="b0653-141">Die Prozessorgeschwindigkeit in Megahertz (MHz).</span><span class="sxs-lookup"><span data-stu-id="b0653-141">The processor speed, in megahertz (MHz).</span></span>

<span data-ttu-id="b0653-142">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="b0653-142">ProcessorArchitecture</span></span>

<span data-ttu-id="b0653-143">**Integer**</span><span class="sxs-lookup"><span data-stu-id="b0653-143">**Integer**</span></span>

<span data-ttu-id="b0653-144">Die Prozessorarchitektur.</span><span class="sxs-lookup"><span data-stu-id="b0653-144">The processor architecture.</span></span> <span data-ttu-id="b0653-145">Weitere Informationen finden Sie in der Erläuterung des **wProcessorArchitecture-Elements** der [**SYSTEM \_ INFO-Struktur.**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info)</span><span class="sxs-lookup"><span data-stu-id="b0653-145">For details, see the discussion of the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span>

<span data-ttu-id="b0653-146">PhysicalMemoryInstalled</span><span class="sxs-lookup"><span data-stu-id="b0653-146">PhysicalMemoryInstalled</span></span>

<span data-ttu-id="b0653-147">**Integer**</span><span class="sxs-lookup"><span data-stu-id="b0653-147">**Integer**</span></span>

<span data-ttu-id="b0653-148">Die Menge des installierten physischen Arbeitsspeichers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="b0653-148">The amount of physical memory installed, in bytes.</span></span>

<span data-ttu-id="b0653-149">Die folgenden Sind nur unter Windows XP gültig.</span><span class="sxs-lookup"><span data-stu-id="b0653-149">The following are valid only on Windows XP.</span></span>

<span data-ttu-id="b0653-150">IsOS \_ Professional</span><span class="sxs-lookup"><span data-stu-id="b0653-150">IsOS\_Professional</span></span>

<span data-ttu-id="b0653-151">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="b0653-151">**Boolean**</span></span>

<span data-ttu-id="b0653-152">Legen Sie diese Einstellung auf **TRUE** fest, wenn das Betriebssystem Windows XP Professional Edition ist. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="b0653-152">Set to **true** if the operating system is Windows XP Professional Edition; otherwise, **false**.</span></span>

<span data-ttu-id="b0653-153">IsOS \_ Personal</span><span class="sxs-lookup"><span data-stu-id="b0653-153">IsOS\_Personal</span></span>

<span data-ttu-id="b0653-154">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="b0653-154">**Boolean**</span></span>

<span data-ttu-id="b0653-155">Legen Sie diese Einstellung auf **TRUE** fest, wenn das Betriebssystem Windows XP Home Edition ist. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="b0653-155">Set to **true** if the operating system is Windows XP Home Edition; otherwise, **false**.</span></span>

<span data-ttu-id="b0653-156">Folgendes ist nur unter Windows XP und höher gültig.</span><span class="sxs-lookup"><span data-stu-id="b0653-156">The following is valid only on Windows XP and later.</span></span>

<span data-ttu-id="b0653-157">IsOS \_ DomainMember</span><span class="sxs-lookup"><span data-stu-id="b0653-157">IsOS\_DomainMember</span></span>

<span data-ttu-id="b0653-158">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="b0653-158">**Boolean**</span></span>

<span data-ttu-id="b0653-159">Wird auf **TRUE** festgelegt, wenn der Computer Mitglied einer Domäne ist. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="b0653-159">Set to **true** if the computer is a member of a domain; otherwise, **false**.</span></span>



 

<span data-ttu-id="b0653-160">Diese Methode ist derzeit in Microsoft Visual Basic nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b0653-160">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="b0653-161">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0653-161">Examples</span></span>

<span data-ttu-id="b0653-162">Die folgenden Beispiele zeigen die Verwendung von **GetSystemInformation** für JScript und VBScript.</span><span class="sxs-lookup"><span data-stu-id="b0653-162">The following examples show the use of **GetSystemInformation** for JScript and VBScript.</span></span>

<span data-ttu-id="b0653-163">Jscript:</span><span class="sxs-lookup"><span data-stu-id="b0653-163">JScript:</span></span>


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



<span data-ttu-id="b0653-164">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="b0653-164">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b0653-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0653-165">Requirements</span></span>



| <span data-ttu-id="b0653-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0653-166">Requirement</span></span> | <span data-ttu-id="b0653-167">Wert</span><span class="sxs-lookup"><span data-stu-id="b0653-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0653-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0653-168">Minimum supported client</span></span><br/> | <span data-ttu-id="b0653-169">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0653-169">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0653-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0653-170">Minimum supported server</span></span><br/> | <span data-ttu-id="b0653-171">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0653-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b0653-172">Header</span><span class="sxs-lookup"><span data-stu-id="b0653-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0653-173"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="b0653-173"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="b0653-174">Idl</span><span class="sxs-lookup"><span data-stu-id="b0653-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b0653-175"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="b0653-175"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="b0653-176">DLL</span><span class="sxs-lookup"><span data-stu-id="b0653-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0653-177"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="b0653-177"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
